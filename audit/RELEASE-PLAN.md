# Release plan — version 0.1.0

Opened 2026-10-23. Standard: [A Public Standard for This Work](https://jeff-kline.github.io/posts/research-program/index.html).
State machine: DRAFT → CANDIDATE → TAGGED → ARCHIVED → ADMITTED. The current
state is in `ADMISSION.md`.

## Scope set by the author (2026-10-23)

"Nothing is public for now." This release preparation therefore stops at a
local CANDIDATE commit. No GitHub repository (private or public), tag,
release, DOI, Zenodo record, or site entry is created without a further,
explicit authorization. R1 cannot close in this scope.

## Principal claim

For the explicit kernel `K` (paper (1)), unconditionally,
`λ_r(K) ~ (6/π²)/(r log r)`, `n(K;s) ~ (6/π²)/(s log(1/s))`, and
`Σ_{r≤R} λ_r(K) ~ (6/π²) log log R`; the same for `L = K − (Ke₁)(Ke₁)*/c₀`.
No rate; no growing-index finite-matrix statement without an extra
operator-norm estimate; no Mertens estimate.

## Gates

- **P1:** the bounded comparison in `audit/PRIOR-ART.md`, plus a delegated
  citation and prior-art lane with a fast-follow scan (GitHub, Zenodo,
  recent arXiv).
- **A1:** after the prose checkpoint, read-only lanes run in parallel:
  claim and prose consistency; an end-to-end proof audit of `paper/main.pdf`
  and its sources; citation and prior art. The root agent disposes of the
  findings in `audit/LEDGER.md`.
- **R1:** reproducibility from a fresh `git archive` of the candidate
  commit, the manifest, and hygiene. Tag, archive and DOI rows stay open by
  scope.

## External actions

| Action | Owner | Status |
|---|---|---|
| Local candidate commit | root agent | planned |
| Private GitHub repository and push | author authorization | not authorized |
| Public visibility, Zenodo enablement | author | not authorized |
| Tag `v0.1.0`, GitHub Release | author authorization | not authorized |
| Site entry | author | not authorized |
