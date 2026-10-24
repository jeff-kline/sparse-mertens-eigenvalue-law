# Proof and parameter audit of the release document — 2026-10-23

Auditor: a process-separated AI agent (the same model family as the root
agent), read-only, in a fresh context. It was given the repository and told
to audit `paper/main.tex` and every section end to end, with no expected
verdict. The report was returned through the agent interface and saved here
by the root agent, with its findings preserved. No numerics were run. This
is process evidence, not independent expert review or peer review.

## Verdict: PASS

Every statement in Theorem 1.1 was re-derived from the definitions, through
all its dependencies and both appendices. No proof defect was found: no
errors, no gaps, no missing hypotheses.

## Must fix (process)

**M1.** `paper/main.pdf` was stale. `sections/references.tex` had been edited
after the last build, so the PDF still showed three bibliography entries as
preprints. Mathematical text and statement numbers were unaffected, and all
references, citations and equation references resolved.

## Re-derived (all hold)

**Section 2.**
- Cylinder masses, from 1/(p+1) = (1/p)·p/(p+1).
- Nesting and disjointness.
- Gram entries.
- Child ratios ≤ 1/(q+1) ≤ 1/(P⁺(d)+2) ≤ 1/3.
- Covering up to a null set.
- `{a_d > η} ⊆ {P⁺(d) < 1/η}`, a finite set.
- Sign removal, `K = c₀SV*VS`, and the count scaling.

**Section 3.**
- Proposition 3.1: level operators have norm ≤ θ^ℓ and are compact using
  only D(t) < ∞; norm bound M_θ; cutoff bound.
- The normalized subtree decomposition and norm bound.
- Proposition 3.2: the leaf compression is diagonal; the indicator is
  justified; the unrolling terminates finitely; the rough bounds hold.
- Theorem 3.4: the two-sided bounds; regular variation of index −α; and
  D(t) → ∞.

**Theorem 4.1.**
- The asymptotics of m(p) and the exact weak-count identity.
- p = 2, where the term is 1.
- The small range: the uniform Rankin bound is used only for x ≥ y ≥ 2.
  The bin step uses 1/log p < 1/k and 4(k+1) ≤ 8k. The maximum of f is
  256e^{−2}/L² and the integral is (8/L)e^{−1/(8a)}, with a constant
  independent of a.
- The middle range: the squarefree expansion, with tail ≪ x/B; compact-u
  Dickman only; the cutoff at p⁻ changes counts by ≤ z/p; limits X → ∞ then
  B → ∞; uniform asymptotics; weak convergence of the prime measures to
  dα/α; and the substitution v = 1/α − 1.
- The large range.
- The order of limits, X → ∞ first, then a → 0 and b → 1.
- The constant c₀ζ(2)e^{−γ}e^γ = 1, and the strict/weak squeeze.
- No external input is used beyond its cited statement. The auditor could
  not open Hildebrand–Tenenbaum itself.

**Section 5.**
- Inversion, which traps λ_r with no multiplicity assumption.
- Summation.
- Deflation: `Ke₁ = c₀SV*1`, `L = c₀SV*(I−P)VS ≥ 0`, and
  0 ≤ n(K) − n(L) ≤ 1.
- Corollary 5.1.
- Proposition 5.2: the layer identity, Σ‖b_j‖ < ∞, trace norm 2‖b_j‖, and
  Ky Fan.

**Section 6.**
- The inverse formula, including nonsquarefree coordinates.
- The Gram entries and the rough density.
- Domination and HS convergence.
- Corollary 6.2 via Weyl.
- det B_n = M(n).
- The link from L to B_n is cited from the predecessor and correctly
  attributed.

**Section 7.**
- a_n(V) ~ (n log n)^{−1/2}.
- The binary-filtration identity.
- The ultrametric kernel.
- The non-eigenvector h.
- Proposition B.2 is not a counterexample to Question 7.1.

**Appendix A.**
- Lemma A.1, which needs no trace-class assumption.
- Proposition A.2 and Proposition A.3.
- Theorem A.4, including endpoint atoms, the neighborhood of zero, Darboux
  sums, ∫h_k = 1, and the exceptional class.
- Remarks A.5 and A.6.

**Appendix B.**
- Proposition B.1: the renewal identity with strict inequality, the initial
  atom, and a Riemann-integrable common profile.
- The (3/10, 7/10) example.
- Proposition B.2, with the k = 3 limits 2/3 and 2.
- Remark B.3.

## Optional

- **O1.** related.tex said "least-prime tree"; the tree is defined by deleting
  the largest prime. Use "the tree of Section 2".
- **O2.** profiles.tex "The correct norm inequality is …" reads as leftover
  correction text.
- **O3.** The non-constancy of Th is asserted with "depends, for example".
  A one-line proof: on A₁₀ the path after 2 has mass ≤ (7/6)ν₁₀ < ν₆.
- **O4.** The bin step silently uses 1/log p < 1/k and 4(k+1) ≤ 8k.
- **O5.** The indicator justification could state
  ‖(m_c/m_v)T̂_c‖ ≤ ‖T̂_v − R₁‖ ≤ ‖T̂_v‖.
- **O6.** The abstract and README claim about B_n rests on the predecessor's
  Theorem 4.6; add that dependency to the README evidence table.
