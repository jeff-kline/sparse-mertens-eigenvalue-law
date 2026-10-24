# Prior-art record (P1)

This is a bounded, theorem-level comparison, not a priority certificate. The
working records it summarizes were kept outside this repository. Local paths
are omitted here.

**Outcome: distinct within the checked scope.** We have not found the
principal result (λ_r(K) ~ (6/π²)/(r log r), with the deflation and the
counting forms) in the sources below. It must not be shortened to "novelty
established". The open comparisons at the end could change this.

## What is compared

The principal result rests on three parts:

* **S1:** the cylinder Gram representation of `K`;
* **S2:** the tree sandwich, which transfers a vertex-mass count to the
  eigenvalue count;
* **S3:** the arithmetic mass count `D(t) ~ 1/(t log(1/t))`.

The defensible claim is the exact asymptotic for this kernel. Whether S2 as
a general method merits a separate originality claim is unsettled: the
device is familiar from self-similar spectral asymptotics. S3 is classical
in technique and is not claimed as new.

## Comparisons

| Source (version read) | Location | Mapping attempted | Verdict |
|---|---|---|---|
| Hilberdink–Pushnitski, *Spectral asymptotics for a family of LCM matrices*, arXiv:2110.14323v1 | Thm 1.1 (p. 2); §1.3 product formula; §4.2 Wiener–Ikehara | (i) `K`'s entries are `ν_{max}` on ancestor pairs, with ν depending on `P⁺`; there is no product `∏_p e_p(j_p,k_p)`. (ii) In `L²(⊗_p Bernoulli)` the cylinder indicators are product vectors, but `T` is a *sum* of product rank-ones, not a tensor product. (iii) `Σ_r λ_r^{1+σ} ≍ log(1/σ)`, a logarithmic singularity rather than a pole | Does not apply. Power laws κ n^{−ρ} versus a law with a logarithmic factor. Their κ ≠ 1 at ρ = ½ (eq. (1.5)) contrasts with the diagonal constant here |
| Hilberdink–Pushnitski, *… arithmetical matrices and connection to Beurling primes*, arXiv:2401.06892v1 | Abstract, §§1–2, §4 (Wiener–Ikehara), §5 | Same as above; the Beurling connection needs a product-eigenvalue formula, which was not found for `K` | Does not apply |
| Evans–Harris–Lang, *The approximation numbers of Hardy-type operators on trees*, arXiv:math/0003215v1 | Abstract (∗); §2 standing hypothesis of finite vertex degree; metric tree with length measure | The synthesis map `V` is a discrete Hardy operator from vertices to tree ends. (∗) with finite `∫\|uv\|` forces `a_n = O(1/n)`, while `a_n(V) ~ (n log n)^{−1/2}` | The theorem does not apply directly, and no representation can satisfy its hypotheses with a finite integral. Infinite degree is **not** an invariant obstruction (see the binary representation below) |
| Bendikov–Grigor'yan–Pittet–Woess, *Isotropic Markov semigroups on ultra-metric spaces*, arXiv:1304.6271 | Thm 3.8 (eigenfunctions `1_C/μ(C) − 1_B/μ(B)`); compact balls imply finite degree | `T = M_w − 𝓛`, where `w(ω) = Σ_{d on the path} ν_d` and `𝓛 = Σ_B ν(B)(M_{1_B} − Π_B)` is diagonal in that basis. `h = 3·1_{A_2} − 1` is not an eigenvector: on `A_2`, `Th − 2ν_2` lies in `2·[1/12, 5/48]` or `2·[1/24, 7/144]` according as the next selected prime is 3 or 5 (corrected 2026-10-23 from `[1/12, 1/10]` and `[1/24, 1/21]`, which used tail ratios 1/5 and 1/7 as tail sums; the intervals remain disjoint) | Their diagonalization does not apply. This does not rule out every hierarchical Schrödinger theorem |
| Hilberdink, *Singular values of multiplicative Toeplitz matrices*, LAMA 65 (2017) 813–829 (accepted manuscript) | Abstract; Thm 2.2 | Fixed-index Gram limits for `f(i/j)1[j\|i]`; nothing on `r → ∞` | Prior art for the predecessor's device, not for this law |
| Kigami–Lapidus, CMP 158 (1993) 93–125 | **Full text not retrieved** (2026-10-23: Project Euclid and a repository alternate returned HTML; 2026-10-24: Project Euclid, Springer, Kyoto and Göttingen returned HTML, a bot challenge or a paywall; Unpaywall reports closed access) | Recursive counting plus a renewal theorem for self-similar sets; here the tree is non-stationary and countably branching, and the transfer uses vertex counts | Device familiar; the theorem comparison is open |
| Erdős–Ivić–Pomerance, Glasnik Mat. 21(41) (1986) 283–300 | Thms 1–4 | Sums over the largest prime factor through `Ψ` and ρ; the same technique as S3 | S3 not new in method. A search-snippet attribution of `Σ 1/(n log P(n)) = e^γ log log x + B` to this paper was **not** found in its text and is unverified |
| Naimark–Solomyak, *Eigenvalue estimates for the weighted Laplacian on metric trees*, Proc. LMS (3) 80 (2000) 690–724 (author-hosted copy; read 2026-10-24) | §1 (weight `V ∈ L¹_loc(G)`, eq. (1.1)); Thms 4.1, 4.6 (bounded branching and the edge condition (4.8)); Cor. 4.7 (p. 713); §8 (regular trees, renewal theorem) | A Hardy-type realization needs a weight whose mass on the subtree below each edge `k` equals `ν_k`. Because the children's cylinders cover each cylinder up to a null set, the mass on each edge would be `ν_k − Σ_children ν_c = 0`: the mass of `ν` lies on the ends of the tree, not in `L¹` on the edges | Hypotheses fail for a direct application. Even where they hold, Cor. 4.7 gives two-sided Schatten/weak-Schatten quasi-norm equivalences with unspecified constants, not an asymptotic with a constant. Whether an approximation argument gives two-sided bounds for `T` is open |
| Bendikov–Grigor'yan–Molchanov, arXiv:1811.05210 (read 2026-10-24) | §2.1 (p. 6): `(X,d)` "is not compact and … proper", homogeneous; Thm 2.1 (p. 10) | Their spectral results are essential self-adjointness, discrete spectrum when `V → +∞`, the essential spectrum when `V → 0`, and a bound for the number of negative eigenvalues. Our space is compact with inhomogeneous masses, and `T` is itself the compact positive object | Hypotheses fail; no eigenvalue-asymptotic statement for an operator like `T` |
| Kigami–Lapidus, as restated in Gu–Qiu, arXiv:2507.14858, Thm 2.1 (secondary; read 2026-10-24) | Thm 2.1 | Finitely many contractions, p.c.f. self-similar set; counting function `C x^{d_S/2}` (non-lattice) or with a log-periodic factor (lattice) | On the restatement the hypotheses fail: the arithmetic tree is non-stationary and countably branching, and the law has a logarithmic factor. Primary text still not read |
| Solomyak, *On the spectrum of the Laplacian on regular metric trees*, Waves Random Media 14 (2004) S155–S171 | Abstract and theorem list | Regular (stationary, symmetric) trees only | Not applicable |
| arXiv:2502.09489 (Redheffer singular vectors; abstract read 2026-10-24) | Abstract | The top singular vector of the finite Redheffer matrix | Not applicable: no eigenvalue decay for a limiting kernel |
| Pinsky, arXiv:1606.02965 | Abstract only | A probabilistic model of smooth integers (geometric exponents) | No spectral content |

## Exact binary-tree representation

Reveal the primes one at a time. The cylinders `B` of this binary filtration
are fixed by the selection bits up to some prime `p`. Each `A_d` is such a
cylinder with `p = P⁺(d)` and last bit 1, and

```text
T = Σ_B c_B ν(B)⁻¹ R_{1_B},   c_B = ν(B) if B = Ω or its last revealed prime is selected, else 0.
```

So dyadic or martingale Carleson-embedding results and bounded-degree
weighted-tree results are legitimate comparisons. Whether any of them gives
the exact constant, only two-sided bounds, or neither is **open**.

## Search log

Searches were run on 2026-10-23. Each is listed with its query and outcome.

| Index | Query | Outcome |
|---|---|---|
| arXiv API | `all:"largest prime factor" AND all:eigenvalues` (sorted by date) | 1 irrelevant hit |
| arXiv API | `all:"largest prime factor" AND (eigenvalue OR spectrum OR operator)` over http | empty response: **NOT PERFORMED** |
| arXiv API | `all:Mertens AND all:"singular values"` | empty; possibly rate-limited, treated as **NOT PERFORMED** |
| arXiv API | `all:squarefree AND all:"compact operator"` | empty; treated as **NOT PERFORMED** |
| arXiv API | `all:"arithmetical matrices" AND all:asymptotics` | the two Hilberdink–Pushnitski papers |
| GitHub | `gh search repos "mertens matrix"` | only the author's own repository |
| GitHub | `gh search repos "squarefree tree spectrum"` | none |
| GitHub | `gh search code "sparse-mertens-singular-spectrum"` | none returned; code search may need scoped authentication, so **NOT PERFORMED** as evidence |
| Zenodo API | `"sparse mertens"`, most recent | 3 records, all by the author |
| Zenodo API | `"largest prime factor" eigenvalue kernel` | 23,829 noisy hits; none of the top 8 relevant |
| Web | Hardy operators on trees, approximation numbers | Evans–Harris–Lang; Naimark–Solomyak (snippets only) |
| Web | squarefree tree `n/P(n)` operator spectrum | no source; "The coprime quantum chain" (arXiv:1701.02317), a multiplicative Möbius operator with a different structure |
| Web | hierarchical kernels, common prefix | Bendikov et al.; arXiv:1811.05210 found |
| Web | "sparse Mertens" follow-ups, 2026 | none; the Redheffer singular-vector paper arXiv:2502.09489 was not read |
| Web | `1/(n log n)` eigenvalues with Dickman/squarefree | no match |

### Fast-follow scan and bounded pass, 2026-10-24

A process-separated AI literature agent ran these searches; the full log
(32 entries) is kept with the working records.

| Index | Query | Outcome |
|---|---|---|
| GitHub | `gh search repos` "Mertens matrix", "sparse-mertens", "squarefree eigenvalue", Redheffer | only the author's repositories; Redheffer hits are optics code, a 2015 repository, and a Lean repository on the determinant identity (description only) |
| GitHub | `gh search code` "Mertens matrix", "squarefree eigenvalue", Redheffer, "sparse-mertens" | no relevant hit; "sparse-mertens" returned none, apparently because the author's repositories are not code-indexed, so this is not evidence of absence |
| arXiv API | Redheffer with singular values, eigenvalue or spectrum; "Mertens matrix"; squarefree with eigenvalue and kernel; "largest prime factor" with eigenvalue, spectrum or operator; Dickman with eigenvalue; arithmetical/LCM matrices with eigenvalue | nothing relevant in 2026; the newest arithmetical-matrix paper, arXiv:2601.16626 (finite generalized eigenvalues of LCM/GCD and MAX/MIN matrices), is unrelated to a limiting kernel |
| Web | Naimark–Solomyak; Kigami–Lapidus; Lifshits–Linde (summation and Volterra operators); Schatten-class dyadic Carleson embeddings | as in the comparison table; Lifshits–Linde and Carleson results seen as snippets only, with no tree singular-value asymptotics |
| Semantic Scholar API | Kigami–Lapidus title | HTTP 429: **NOT PERFORMED** |

**NOT PERFORMED:** MathSciNet, zbMATH, Google Scholar citation lists.
A further fast-follow scan before tagging is required by the release
standard. Its results are appended to `audit/LEDGER.md`.

## Open comparisons

Updated 2026-10-24. Bendikov–Grigor'yan–Molchanov and Naimark–Solomyak
(Proc. LMS 2000) are now compared at theorem level (table above).

1. Whether an approximation argument brings the Naimark–Solomyak
   estimates to bear on `T`. At most this would give two-sided bounds of
   the right order, not the constant.
2. Weighted dyadic/martingale Carleson embeddings and Lifshits–Linde-type
   summation operators at theorem level (snippets only so far).
3. Kigami–Lapidus: primary full text (secondary restatement read).
4. Naimark–Solomyak, Russ. J. Math. Phys. 8 (2001): abstract only.
5. MathSciNet, zbMATH and Google Scholar: not performed.
