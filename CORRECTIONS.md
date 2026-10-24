# Corrections, withdrawals, and supersession

This repository keeps a visible record of material corrections to released
claims and artifacts.

## Policy

- Minor typographical or navigational fixes may be made on the living default
  branch without changing an archived release.
- A change to a theorem statement, hypothesis, proof dependency, citation that
  affects priority or scope, or verification artifact creates a new version.
  The earlier tag and permanent archive remain unchanged and identifiable.
- A material error that invalidates a principal claim will be marked
  prominently in the README and in this file. The affected release will not be
  deleted or silently replaced.
- A withdrawn result remains findable with the reason, date, affected
  versions, and any replacement or correction linked here.
- Public tags and archived files are immutable. Corrections are made in a new
  commit and, when material, a new tagged release.
- If earlier work is found that anticipates a result here, the novelty
  statements will be narrowed and the source credited in a new version.

Once the repository is public, suspected errors may be reported through its
issue tracker:
<https://github.com/jeff-kline/sparse-mertens-eigenvalue-law/issues>.

## Relation to earlier releases

This paper continues
[*The singular spectrum of a sparse Mertens matrix*](https://doi.org/10.5281/zenodo.23004980),
version 0.1.0. That release remains correct as stated. It identified each
fixed eigenvalue of the kernels `K` and `L` as a limit of finite singular
values; this paper adds their decay as the index grows. It reproves that
release's Theorem 4.3 (paper Proposition 6.1) so that it can be read on its
own.

## Version history

### 0.1.0 — release candidate

- Release preparation began 2026-10-23 from a local prose draft. The
  pre-release defects found by internal reviews and their dispositions are in
  `audit/REVIEW-HISTORY.md`.
- The candidate has no DOI or permanent archive, and no public repository.
- Prepublication changes during release preparation, before any tag: the
  preamble follows the predecessor (default fonts, no list package); author,
  version line, credit to Kline (2019), and a role-of-AI paragraph were added;
  three bibliography entries now cite journal versions; the audit findings in
  `audit/LEDGER.md` led to small wording changes in §4.3, §7.1 and Remark A.5,
  and a one-line proof in §7.1. No theorem statement changed.
