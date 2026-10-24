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
| Kigami–Lapidus, CMP 158 (1993) 93–125 | **Full text not retrieved** (Project Euclid and a repository alternate returned HTML) | Recursive counting plus a renewal theorem for self-similar sets; here the tree is non-stationary and countably branching, and the transfer uses vertex counts | Device familiar; the theorem comparison is open |
| Erdős–Ivić–Pomerance, Glasnik Mat. 21(41) (1986) 283–300 | Thms 1–4 | Sums over the largest prime factor through `Ψ` and ρ; the same technique as S3 | S3 not new in method. A search-snippet attribution of `Σ 1/(n log P(n)) = e^γ log log x + B` to this paper was **not** found in its text and is unverified |
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

**NOT PERFORMED:** MathSciNet, zbMATH, Google Scholar citation lists.
A further fast-follow scan before tagging is required by the release
standard. Its results are appended to `audit/LEDGER.md`.

## Open comparisons

1. Weighted dyadic/martingale Carleson embeddings and singular values of
   weighted bounded-degree tree operators, applied to the binary
   representation.
2. Bendikov–Grigor'yan–Molchanov, arXiv:1811.05210 (hierarchical
   Schrödinger operators); its §§1–2.2 were read in an earlier review, and
   a theorem-level comparison was not done.
3. Kigami–Lapidus: full text.
4. Naimark–Solomyak: not read.
