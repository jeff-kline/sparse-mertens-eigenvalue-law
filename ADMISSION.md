# Admission record

**Current state:** CANDIDATE (local only)

**Version:** 0.1.0

**Planned tag:** `v0.1.0`

**Standard:** [A Public Standard for This Work](https://jeff-kline.github.io/posts/research-program/index.html)

**Admission verdict:** NOT YET ADMITTED

Admission is a project release decision. It is not peer review, a correctness
certificate, or proof of global novelty.

**Scope set by the author (2026-10-23):** nothing is public for now. A
private GitHub repository was authorized and created on 2026-10-23. No public
visibility, tag, release, DOI, or site entry exists or is planned without a
further explicit authorization.

## Principal claim

For the explicit kernel `K` on the squarefree integers (paper (1)), with
`c₀ = 6/π²`, unconditionally:

- `n(K; s) ~ c₀/(s log(1/s))` as `s → 0+`;
- `λ_r(K) ~ c₀/(r log r)` as `r → ∞`;
- `Σ_{r≤R} λ_r(K) ~ c₀ log log R`;
- the same three statements hold for the positive operator
  `L = K − (Ke₁)(Ke₁)*/c₀`.

No convergence rate, no growing-index statement for the finite matrices
without an additional operator-norm estimate, and no estimate for the
Mertens function is claimed.

## P1 — prior work and credit

| Check | Status | Evidence or residual |
|---|---|---|
| Closest mechanisms and parameter families compared | PARTIAL | `audit/PRIOR-ART.md` compares Hilberdink–Pushnitski (2 papers), Evans–Harris–Lang, Bendikov–Grigor'yan–Pittet–Woess, Bendikov–Grigor'yan–Molchanov, Naimark–Solomyak (Proc. LMS 2000), Hilberdink, and Erdős–Ivić–Pomerance at theorem level; Kigami–Lapidus through a secondary restatement. Open: whether an approximation argument brings Naimark–Solomyak's two-sided estimates to bear (order only, not the constant); Carleson-embedding and Lifshits–Linde-type results at theorem level |
| Obtainable primary sources checked | PARTIAL | Primary texts were read for the sources above and for Hildebrand–Tenenbaum and Gallager (`audit/reports/citation-prior-art-audit.md`). Kigami–Lapidus full text is not obtainable here (closed access; retried 2026-10-24); Naimark–Solomyak, Russ. J. Math. Phys. 2001, abstract only |
| Contribution types distinguished | PASS | README "What is new" (principal result; consequences; representation; supporting general results without priority claim; restatement of the predecessor's Theorem 4.3; arithmetic count not new in method); paper §1.3 and §7 |
| Novelty bounded to searched corpus | PASS | "not found in the sources checked; open comparisons could change this" on the README, paper §7.1 and `audit/PRIOR-ART.md` |
| Inaccessible sources visible | PASS | Named in the README, paper §7 and `audit/PRIOR-ART.md`. MathSciNet and zbMATH NOT PERFORMED |
| Fast-follow scan within 7 days of tagging | PASS for 2026-10-24 | `audit/PRIOR-ART.md` (search log, 2026-10-24) and `audit/LEDGER.md`. Must be repeated if tagging happens after 2026-10-31 |

**P1 gate:** PARTIAL (narrowed 2026-10-24; no source read contains or implies the principal result). The residuals are named. A tag would be acceptable
under the standard only if the author accepts these named residuals.

## A1 — claim and artifact consistency

| Check | Status | Evidence or residual |
|---|---|---|
| Principal claim precise and no broader than proof | PASS | `audit/reports/proof-audit.md` (PASS, end to end) |
| Scope visible near claim | PASS | Theorem 1.1, §1.3 and the README "Evidence and limits" state no rate, limiting operators only, and no Mertens estimate |
| Proof, computation, literature separated | PASS | No theorem rests on computation; README evidence table |
| Credit | PASS | `audit/reports/citation-prior-art-audit.md`; stale preprint entries updated |
| Public prose | PASS | `audit/reports/claim-prose-audit.md`; must-fix items resolved (`audit/LEDGER.md`) |
| What is new | PASS | README section directly after the introduction, separate from "Earlier work" |
| Claims consistency | PASS | One principal result and identical novelty labels on all surfaces (claim lane, item 3) |
| Predecessor mirror | PASS | Modelled on `sparse-mertens-singular-spectrum` v0.1.0: README layout and candidate status line, CFF, CORRECTIONS, VERIFICATION, Makefile, checker, GPL-3.0-only, noreply identity |
| Admitted status | N/A | Not admitted in this scope |
| Metadata | PASS | Title, author, version 0.1.0 and candidate status agree across the README, PDF title page and metadata, `CITATION.cff` and this file |
| Adversarial check | PASS | Three process-separated AI lanes; all must-fix items resolved. AI reviews, not peer review; no independent human expert has examined the proofs |

**A1 gate:** PASS. Any material claim edit reopens this gate.

## R1 — release and stewardship

| Check | Status | Evidence or residual |
|---|---|---|
| Reproduction | PASS | `VERIFICATION.md`: clean build from `git archive` of the candidate commit |
| Artifact integrity | PASS | Deterministic PDF (fixed `SOURCE_DATE_EPOCH`); `MANIFEST.sha256` |
| Hygiene | PASS | Tracked tree scanned for local paths and placeholders. README rendered with `gh api markdown` (GFM) on 2026-10-23: no `$` remains, and all 76 code spans and 8 sections render |
| Stewardship | PASS | `CORRECTIONS.md` |
| Tag | FAIL (out of scope) | not authorized |
| Archive | FAIL (out of scope) | not authorized |
| Citation | FAIL (out of scope) | no DOI; the CFF is candidate-safe (no DOI, no release date, no repository URL) |
| Metadata | FAIL (out of scope) | no archive |

**R1 gate:** open by scope.

## External actions

| Action | Owner | Status |
|---|---|---|
| Local candidate commit | root agent | done: `b8683d2` (candidate), `c816db9` (records) |
| Private GitHub repository and push | author authorization | done 2026-10-23: `jeff-kline/sparse-mertens-eigenvalue-law` (private); `main` pushed at `c816db9` |
| Public visibility; Zenodo enablement | author | not authorized |
| Tag and GitHub Release | author authorization | not authorized |
| Site entry | author | not authorized |
