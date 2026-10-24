# Audit ledger

Append-only. Each entry records the scope, the auditor type, the pinned inputs,
the verdict, and the root agent's disposition of every finding. All auditors
are AI agents; separate contexts are process evidence, not independent expert
review or peer review.

## 2026-10-23 — Pre-release reviews (summary)

Internal, same-context reviews of the proof notes and the mathematical
treatment preceded release preparation. They are summarized, with every
defect and disposition, in `audit/REVIEW-HISTORY.md`. They are not counted
as the release's adversarial audit.

## 2026-10-23 — Claim and public-prose lane (A1)

- Auditor: process-separated AI agent (Sonnet), read-only.
- Report: `reports/claim-prose-audit.md`.
- Inputs: the untracked working tree before the first commit (no hashes
  pinned yet; the tree changed afterwards only by the dispositions below).
- Verdict: PARTIAL. Four must-fix items, none affecting a claim.

| Finding | Disposition |
|---|---|
| M1: README cites missing `MANIFEST.sha256` and `VERIFICATION.md` | Accepted. Both are generated at the freeze, before the candidate commit |
| M2: "paper (1.1)" should be "paper (1)" | Fixed in `ADMISSION.md` and `audit/RELEASE-PLAN.md` |
| M3: CFF names a non-existent repository URL | Fixed: `url` and `repository-code` removed until a repository is authorized. Partly declined: the message stays timeless, as in the predecessor, because archive providers import it verbatim. Candidate status is carried by `ADMISSION.md` and the README status line |
| M4: CORRECTIONS links an issue tracker that does not exist | Fixed: "Once the repository is public," |
| O1: README uses `L` without its formula | Fixed: the formula was added to the README Introduction |
| O2–O6: other optional items | No change. `tmp/` is git-ignored |

## 2026-10-23 — Citation and prior-art lane with fast-follow scan (P1)

- Auditor: process-separated AI agent (Sonnet), read-only.
- Report: `reports/citation-prior-art-audit.md`.
- Budget: 25 external operations allotted, 26 used (overrun of 1 recorded).
- Verdict: PARTIAL, with no blockers. The fast-follow scan of 2026-10-23
  found no work on this kernel or law. Several queries are NOT PERFORMED (see
  the report); this is not a certificate.

| Finding | Disposition |
|---|---|
| C1: EHL, BGPW and HP21 cited as preprints, but journal versions exist | Fixed. The root agent re-verified each through Crossref (PLMS 83 (2001) 390–418; Russian Math. Surveys 69 (2014) 589–680, the English translation of Uspekhi 69(4) 3–102; St. Petersburg Math. J. 34 (2023) 463–481) and updated `references.tex`. Theorem and equation numbers are tied to the arXiv versions read. README years were updated to match |
| C2: HT pp. 414, 422, 426, eq. (2.3), Lemma 2.6; BGPW Thm 3.8; EHL finite-degree hypothesis not re-checked in this lane | Verified earlier by the root agent from primary texts. The HT printed pages were inspected as page images: p. 414 has (1.4), the log y removal pointing to III.5.1, and the fixed-u Dickman limit; p. 422 has (2.3) defining E; p. 426 has Lemma 2.6. BGPW Thm 3.8 and EHL §2 ("Each vertex of Γ is of finite degree") were read in the arXiv texts. No change |
| C3: HP24 and BGM journal versions | None found; they are cited as preprints. Not proof that none exists |
| C4: record the scan | Done: this entry and the report |

## 2026-10-23 — Proof and parameter lane, end to end (A1)

- Auditor: process-separated AI agent (same model family as the root agent,
  fresh context), read-only. No numerics.
- Report: `reports/proof-audit.md`.
- Inputs: the untracked tree after the claim-lane fixes. It also covered
  `references.tex` after the bibliography update, so its finding M1 is that
  the PDF was stale.
- Verdict: PASS. No error, gap, or missing hypothesis.

| Finding | Disposition |
|---|---|
| M1: stale PDF | Fixed. Rebuilt with `make paper`; `make check` PASS |
| O1: "least-prime tree" misnomer | Fixed: "The tree of Section 2" |
| O2: leftover correction wording in Remark A.5 | Fixed: "The argument uses only the upper bound …"; the inequality is unchanged |
| O3: non-constancy of Th asserted without proof | Fixed with a one-line proof in §7.1. Recomputing it showed that the interval endpoints in `audit/PRIOR-ART.md` (1/10, 1/21) understated the tails; corrected to 5/48 and 7/144. Disjointness, and hence the conclusion, is unaffected. Labelled *error (documentation)* in `audit/REVIEW-HISTORY.md` D9 |
| O4: implicit inequalities in the bin step | Fixed: stated in §4.3 |
| O5: indicator justification | Not changed; the existing sentence suffices |
| O6: dependency on the predecessor's Theorem 4.6 | Fixed: added to the README evidence table |

After these edits, the 19 formal statements were re-extracted and diffed
against the mathematical baseline. They are unchanged apart from one label
and one section reference.

## 2026-10-23 — Mechanical release audit (R1) and one reversed disposition

- `release_audit.py --state candidate --tag v0.1.0 --require-clean` on commit
  `b8683d2`: 5 pass, 1 warning (tag not yet created, expected), 2 fail.
- Fail 1: `CITATION.cff` is missing `repository-code`. **Disposition: claim-lane
  M3 is partly reversed.** The planned repository URL is restored in `url` and
  `repository-code`, matching the predecessor's candidate CFF. The README
  status line and `ADMISSION.md` state that the repository has not been
  created; the URL is a planned location, not a citation of a published
  version.
- Fail 2: `--require-github-noreply` needs `--publish-base`, and no remote
  exists. Identities were checked directly instead: the author and committer
  of every commit are `Jeff Kline <2778446+jeff-kline@users.noreply.github.com>`.
  This must be rerun with `--publish-base` before any push.
- The script's citation-key check found 0/0 keys, because it does not parse
  the `thebibliography` items under `paper/sections/`. The project checker
  covers this (12/12 cited, 0 missing).
- Clean reproduction: `git archive` of `b8683d2` was extracted to a scratch
  directory, the tracked PDF was deleted, and `python3 -m venv .venv && make
  paper && make check` was run. Result: PASS, 21 pages, PDF SHA-256
  `70912f55d62f6127e7150b64e4ba9afe30bf3fa64b6eba234f8df1c694f5c925`,
  identical to the tracked PDF. A warm repeat build was also identical.
  Manifest: all files OK.

## 2026-10-23 — Private GitHub stage (author-authorized)

- README rendered with `gh api markdown -f mode=gfm`: 0 `math-renderer`
  elements (none intended), 0 `$` characters, 76 code spans, 8 sections.
- Created the private repository `jeff-kline/sparse-mertens-eigenvalue-law` and
  pushed `main` at `c816db9`. Visibility verified PRIVATE; remote
  `refs/heads/main` equals local.
- Commit identities before the push: the author and committer of `b8683d2`
  and `c816db9` are `2778446+jeff-kline@users.noreply.github.com`.
- Not done, and not authorized: public visibility, tag, GitHub Release,
  Zenodo, site entry.
