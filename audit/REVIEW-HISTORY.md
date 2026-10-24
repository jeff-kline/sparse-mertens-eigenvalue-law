# Proof-review history before release preparation

The working notes were kept outside this repository, and local paths are
omitted. Every reviewer was an AI agent. Reviews in the same context are
labelled **internal**; no review below is independent expert review.

## Sequence (all on 2026-10-23)

1. **First derivation.** Two parts:
   * the cylinder Gram representation, the tree sandwich, and the
     arithmetic count;
   * a check of three earlier derivations: Tr K = ∞, K − Δ trace class, and
     the Ky Fan cumulative comparison.

   Finite-section numerics (sections up to index 64,000, 100 eigenvalues)
   and diagonal counts up to 10⁷ were exploratory. None is a premise of any
   theorem.
2. **Internal substantive review (Codex), verdict VERIFIED.** It required
   one endpoint repair and the deletion of an unsupported rate claim.
3. **Revision 2.** Changes:
   * repairs incorporated;
   * a page-cited source check of Hildebrand–Tenenbaum (1993), pp. 414, 422
     and 426;
   * a bounded novelty comparison.
4. **Internal review of revision 2 (Codex).** It found a mis-combined
   smooth-number range, a source error that left the theorem unaffected. It
   also narrowed two novelty exclusions.
5. **Revision 3.** The compact-u Dickman input, with the novelty narrowed.
6. **Strengthening pass.** A fresh-context agent was asked to delete the
   "child ratios → 0" hypothesis:
   * outcome UNRESOLVED;
   * it gave the profile-transfer theorem and the stationary-tree theorem
     (now Appendices A and B);
   * the proposed obstruction is not used, and no counterexample is claimed.
7. **Mathematical treatment v1.** Codex wrote the general tree theorems and
   appendices; this was internally checked.
8. **Prose draft v1.** Prose and organization only. A statement-by-statement
   diff against step 7 showed that all 19 formal statements are unchanged.

## Defects found and their disposition

Each defect has one label: error, gap, missing hypothesis, sharpening, or
documentation.

| # | Defect | Label | Disposition |
|---|---|---|---|
| D1 | Strict versus weak threshold in the mass count | gap | Fixed. An exact weak-count identity is proved and the strict count is squeezed (paper §4.2, §4.5) |
| D2 | A claimed rate `1 − (log log r)/log r` for `r log r · λ_r / c₀` | error | Deleted; no rate is claimed |
| D3 | The prime 2 and the Chebyshev bin bound in the small-prime range | gap | Fixed (paper §4.3) |
| D4 | A monotonicity step in the small-prime bin sum (the summand is unimodal) | gap | Fixed with a maximum-plus-integral bound (paper §4.3) |
| D5 | A Dickman uniformity range stated as `1 ≤ u ≤ y^{1−ε}` by combining Hildebrand–Tenenbaum Thm 1.8 with (1.30) | error (source) | Replaced by uniformity on fixed compact u-intervals, which the proof uses (paper §4.1) |
| D6 | Novelty wording: "infinite degree" as an obstruction; an unread hierarchical-Schrödinger paper characterized from its title | error (novelty statement) | Narrowed; see `audit/PRIOR-ART.md` |
| D7 | A reversed norm inequality in the strengthening report | error (not in the paper) | Paper Remark A.5 states the correct inequality |
| D8 | Proposition B.2 states non-regular variation for index −1 only; its proof gives every index | sharpening | Left as stated |
| D9 | Interval endpoints for `Th` in the prior-art record (1/10, 1/21) used single child ratios instead of tail sums | error (documentation) | Corrected to 5/48 and 7/144 in `audit/PRIOR-ART.md`; the conclusion (disjoint intervals, so h is not an eigenvector) is unchanged. Found when the proof lane's optional item O3 was implemented |
