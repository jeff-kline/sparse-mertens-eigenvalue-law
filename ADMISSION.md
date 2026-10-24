# Admission record

**Current state:** ADMITTED

**Version:** 0.1.0

**Tag:** `v0.1.0` → `268da17857ccc57de08f4b0a87481f23b31751cc`

**Standard:** [A Public Standard for This Work](https://jeff-kline.github.io/posts/research-program/index.html)

Current verdict: ADMITTED (2026-10-24)

**Version DOI:** [`10.5281/zenodo.23621017`](https://doi.org/10.5281/zenodo.23621017) · **Concept DOI:** `10.5281/zenodo.23621016` · **Record:** <https://zenodo.org/records/23621017>

Admission is a project release decision. It is not peer review, a correctness
certificate, or proof of global novelty.

**Scope set by the author.** On 2026-10-23: nothing public; a private GitHub
repository was authorized and created. On 2026-10-24 the author accepted the
named P1 residuals and authorized freezing this candidate for the release
sequence: public visibility and Zenodo enablement (author actions), then the
tag `v0.1.0` and the GitHub Release. Each step is taken only on the author's
explicit authorization. The author then authorized the admission bundle
(site entry and admitted-state metadata) on 2026-10-24.

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

**P1 gate:** PARTIAL (narrowed 2026-10-24; no source read contains or implies the principal result). The residuals are named. A tag is acceptable
under the standard only if the author accepts them; **the author accepted
these named residuals on 2026-10-24.**

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
| Predecessor mirror | PASS | Modelled on `sparse-mertens-singular-spectrum` v0.1.0: README layout and status lines, CFF, CORRECTIONS, VERIFICATION, ADMISSION, Makefile, checker, GPL-3.0-only, noreply identity |
| Admitted status | PASS | README, `CITATION.cff`, the living paper, `CORRECTIONS.md` and this file carry the admitted status and version DOI; the tagged snapshot keeps its candidate wording |
| Metadata | PASS | Title, author, version 0.1.0 and status agree across the README, PDF title page and metadata, `CITATION.cff`, the Zenodo record and this file |
| Adversarial check | PASS | Three process-separated AI lanes; all must-fix items resolved. AI reviews, not peer review; no independent human expert has examined the proofs |

**A1 gate:** PASS. Any material claim edit reopens this gate.

## R1 — release and stewardship

| Check | Status | Evidence or residual |
|---|---|---|
| Reproduction | PASS | `VERIFICATION.md`: clean build from `git archive` of the tagged commit reproduces the archived PDF (SHA-256 `e22b7e98…c0b2`) |
| Artifact integrity | PASS | Deterministic PDF (fixed `SOURCE_DATE_EPOCH`); `MANIFEST.sha256` |
| Hygiene | PASS | Tracked tree scanned for local paths and placeholders. README rendered with `gh api markdown` (GFM), last on 2026-10-24: 63 inline and 3 display math elements, matching the source, and no `$` outside math |
| Stewardship | PASS | `CORRECTIONS.md` |
| Immutable semantic tag | PASS | Annotated `v0.1.0` (object `f90acdb`) → `268da17`; tagger is the GitHub noreply identity |
| Public permanent archive with provider byte identity | PASS | Two pinned GitHub `zipball/v0.1.0` downloads and two Zenodo downloads are byte-identical: 454,000 bytes, SHA-256 `097a7877657197292d6b90bd5716b5ec89a44b197180878f72c5fdd26598a499`; Zenodo MD5 `292469d3af99d368af2bd23af0f986e4` |
| DOI resolves; living repository identifies the version | PASS | `doi.org/10.5281/zenodo.23621017` redirects to the Zenodo record; README, `CITATION.cff`, and the living paper carry the version DOI |
| Archive metadata matches repository | PASS | Title, creator Kline, Jeffery, version v0.1.0, publication date 2026-10-24, license `gpl-3.0`, resource type software, related identifier the `v0.1.0` tree |
| Machine-readable citation | PASS | `CITATION.cff` with version DOI, concept DOI and `date-released: 2026-10-24` |

**R1 gate:** PASS.

**Admission verdict:** ADMITTED (2026-10-24), with the named P1 residuals
accepted by the author. AI reviews only; no independent human expert has
examined the proofs.

## External actions

| Action | Owner | Status |
|---|---|---|
| Local candidate commit | root agent | done: `b8683d2` (candidate), `c816db9` (records); frozen for tagging at `268da17` on 2026-10-24 |
| Private GitHub repository and push | author authorization | done 2026-10-23: `jeff-kline/sparse-mertens-eigenvalue-law` (private); `main` pushed at `c816db9` |
| Make the repository public; enable secret scanning and push protection | author authorization | done 2026-10-24 |
| Enable the repository in Zenodo before the Release | author, in the Zenodo portal | done 2026-10-24; Zenodo release webhook present |
| Annotated tag `v0.1.0`, push, GitHub Release | author authorization | done 2026-10-24; Release "Version 0.1.0" published 15:18 UTC |
| Public-site listing | author authorization (admission bundle) | done 2026-10-24: landing entry at <https://jeff-kline.github.io/> (site commit `0e7f7f5`), Pages build and live HTML checked for title, blurb, repository link, and version DOI |
| Living-metadata update (this commit) | author authorization (admission bundle) | done 2026-10-24, pushed after the site listing was verified live |

## Archive verification

- Route: Zenodo GitHub integration; no manual deposit.
- Pinned before the GitHub Release: GitHub API `zipball/v0.1.0`, downloaded
  twice, identical, 454,000 bytes, SHA-256 `097a7877657197292d6b90bd5716b5ec89a44b197180878f72c5fdd26598a499`.
- Zenodo file `sparse-mertens-eigenvalue-law-v0.1.0.zip`, downloaded twice:
  identical to the pinned zipball. The zipball's contents equal the tagged
  tree, and every file passes its `MANIFEST.sha256`.
- Separate determinism check: `git archive --format=zip
  --prefix=sparse-mertens-eigenvalue-law-v0.1.0/ v0.1.0`, generated twice,
  identical, 453,136 bytes, SHA-256 `d84f91b0e793d20ea0486b69cdd7aeb6fa506f9b8e15054c19b1aa2277093713`. This is a different file from
  the provider zipball and is not compared with it.
- Mechanical audit at the archived state, on the unchanged tagged tree:
  11 pass, 0 warnings, 0 fail.
- Tagged commit reproduced from a clean `git archive` extraction: PDF SHA-256
  `e22b7e98fb0c6c3b7cf093ef430891615bd4230b1da59aeae1bd157fcaa3c0b2`,
  `make check` PASS, 29 manifest entries OK.
- The tagged tree keeps its “release candidate” wording and has no DOI. The
  living paper was rebuilt with the DOI on its title page, so the living PDF
  differs from the archived one.
