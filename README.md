# The eigenvalue decay of the limiting kernel of a sparse Mertens matrix

Jeffery Kline

**Version 0.1.0 — release candidate, not yet archived.** No DOI exists for
this version yet. It is prepared for release under the project's
[public research standard](https://jeff-kline.github.io/posts/research-program/index.html).
Admission under that standard is a release decision, not peer review or a
correctness certificate.

The paper is [paper/main.pdf](paper/main.pdf); its source is
[paper/main.tex](paper/main.tex). This is a sequel to
[*The singular spectrum of a sparse Mertens matrix*](https://doi.org/10.5281/zenodo.23004980)
(version 0.1.0, 2026).

## Introduction

Arrange the squarefree integers (no prime square divides them) as a tree:
the root is 1, and the parent of $d > 1$ is $d/P^+(d)$, where $P^+(d)$ is
the largest prime factor of $d$. On this tree define the symmetric kernel
$K$ whose entry at an ancestor $j$ and a descendant $k$ is
$\mu(k/j)\,\delta_k$, where $\mu$ is the Möbius function and

```math
\delta_k=\frac{6}{\pi^2}\cdot\frac{1}{k}\prod_{p\le P^+(k)}\frac{p}{p+1}.
```

Entries at pairs that are not ancestor and descendant are zero. This kernel
is the limit of the normalized Gram matrices $C_n^{\mathsf T}C_n/n$ of the
inverses $C_n=A_n^{-1}$ of sparse $(0,1)$ matrices; replacing the first row
of $A_n$ by ones gives a matrix $B_n$ with determinant
$M(n)=\mu(1)+\cdots+\mu(n)$. The predecessor release identified each fixed
eigenvalue of $K$ as a limit of finite singular values. This paper
determines how the eigenvalues decay: $K$ is positive and compact, and

```math
\lambda_r(K)\sim\frac{6/\pi^2}{r\log r}\qquad(r\to\infty);
```

equivalently, the number of eigenvalues above $s$ is asymptotic to
$(6/\pi^2)/(s\log(1/s))$ as $s\to0$. The same law holds for the rank-one
deflation

```math
L=K-\frac{(Ke_1)(Ke_1)^{\mathsf T}}{6/\pi^2},
```

whose eigenvalues give, index by index, the limits of the rescaled lower
singular values of $B_n$ other than the smallest.

The proof removes the Möbius signs by a diagonal change of signs, realizes
the kernel as a Gram matrix of nested cylinder sets for a random set of
primes, and shows that the eigenvalue count is asymptotic to the number of
cylinders of mass above the threshold. That number is evaluated with
Mertens' theorem and the Dickman function $\rho$; the constant comes from
the classical identity $\int_0^\infty\rho(v)\,dv=e^\gamma$. No convergence
rate is obtained, and no estimate for the Mertens function follows.

## What is new

The predecessor release proved that $C_n^{\mathsf T}C_n/n\to K$ in
Hilbert–Schmidt norm and that, for each fixed $r$, the rescaled singular
values of $C_n$ and the lower singular values of $B_n$ converge to
expressions in $\lambda_r(K)$ and $\lambda_r(L)$. It did not describe how
$\lambda_r(K)$ behaves as $r$ grows. New here:

1. **Principal result: the eigenvalue law.** For the explicit kernel $K$,
   unconditionally, $\lambda_r(K)\sim(6/\pi^2)/(r\log r)$ as $r\to\infty$;
   the number of eigenvalues above $s$ is asymptotic to
   $(6/\pi^2)/(s\log(1/s))$ as $s\to0$; and
   $\lambda_1(K)+\cdots+\lambda_R(K)\sim(6/\pi^2)\log\log R$. The same three
   statements hold for the deflated operator $L$, which is positive.
2. **Consequences.** $K$ and $L$ lie in the Schatten class $S_p$ exactly
   when $p>1$; $K$ is not trace class, although $K$ minus its diagonal is.
3. **The cylinder representation.** After conjugation by the diagonal
   matrix of Möbius signs, $K/(6/\pi^2)$ is the Gram matrix of the events
   "the selected primes up to $P^+(d)$ are exactly the prime factors of
   $d$", where each prime $p$ is selected independently with probability
   $1/(p+1)$.
4. **Supporting general results (appendices and Section 3).** For any tree
   of nested sets with disjoint children carrying at most a fixed fraction
   $\theta<1$ of the parent's mass, the associated operator is compact, and
   its eigenvalue count lies between the number of leaves and an inflated
   vertex count of the sets of mass above the threshold. Under vanishing
   child ratios, or a profile condition at index $-1$, and regular variation
   of the mass count, the eigenvalue count is asymptotic to the mass count.
   Stationary non-arithmetic trees satisfy the profile condition. These use
   standard tools (interlacing, a rank-one trace identity, the key renewal
   theorem); no priority is claimed for them.

Not new:

- The finite-matrix convergence (paper Proposition 6.1) is the
  predecessor's Theorem 4.3, reproved so the paper reads on its own.
- The arithmetic count of the cylinder masses (paper Theorem 4.1) is a
  routine application of classical smooth-number estimates and is not
  claimed as new in method.

These statements rest on a bounded comparison recorded in
[audit/PRIOR-ART.md](audit/PRIOR-ART.md). We have not found the principal
result in the sources checked; several comparisons listed there remain open,
so this is not a worldwide novelty claim.

## Earlier work

- **Kline (2019)** introduced the sparse matrix with determinant $M(n)$:
  J. Kline, *A sparser matrix representation of the Mertens function*,
  Linear Algebra Appl. 581 (2019), 354–366.
- **Kline (2026)**, the predecessor release, constructed $K$ and $L$ and
  proved the fixed-index limits.
- **Hilberdink (2017)** developed fixed-index compact Gram limits for
  multiplicative Toeplitz matrices; the predecessor's limit follows that
  pattern.
- **Hilberdink and Pushnitski (2023, and a 2024 preprint)** proved
  power-law eigenvalue asymptotics for LCM-type arithmetic matrices through
  tensor products over primes and a Wiener–Ikehara Tauberian theorem. The
  entries of $K$ are determined by the ancestor relation; no tensor
  factorization of it was found, and its law carries a logarithmic factor.
- **Evans, Harris and Lang (2001)** proved approximation-number asymptotics
  of order $1/n$ for Hardy operators on metric trees of finite degree. The
  synthesis operator here has approximation numbers of order
  $(n\log n)^{-1/2}$, so it is outside that theorem.
- **Bendikov, Grigor'yan, Pittet and Woess (2014)** diagonalized isotropic
  Laplacians on ultrametric spaces; the operator here is not diagonal in the
  corresponding basis.
- **Hildebrand and Tenenbaum (1993)** is the source for the smooth-number
  inputs (the Dickman limit, the uniform Rankin bound, and
  $\int_0^\infty\rho=e^\gamma$).
- **Kigami and Lapidus (1993)** used recursive counting identities and
  renewal theory for self-similar fractals; the appendix on stationary trees
  uses the key renewal theorem in that way.

Open comparisons: weighted Carleson-embedding and bounded-degree tree
results (the operator has an exact binary-tree form, given in Section 7),
hierarchical Schrödinger operators (Bendikov, Grigor'yan and Molchanov), and
the full text of Kigami–Lapidus.

## Evidence and limits

| Claim | Status |
|---|---|
| Theorem 1.1 (eigenvalue law for $K$ and $L$) | proved on paper, from classical inputs |
| Theorem 3.4 and Proposition 3.2 (tree transfer and sandwich) | proved on paper |
| Theorem 4.1 (mass count) | proved on paper, conditional on the cited classical estimates of Hildebrand–Tenenbaum (1993) and Mertens' theorems |
| Proposition 6.1 (finite Gram limit) | proved on paper; restates the predecessor's Theorem 4.3 |
| Corollary 6.2 (growing indices) | proved on paper, conditional on an operator-norm error bound that is not supplied |
| Appendix A (profile transfer) | proved on paper |
| Lower singular values of $B_n$ through $L$ (Introduction) | cited from the predecessor's Theorem 4.6, not reproved here |
| Appendix B (stationary trees) | proved on paper, conditional on the key renewal theorem (Gallager, Theorem 4.7.3) |

- No theorem rests on numerical computation.
- The proofs were checked by process-separated AI reviews. No independent
  human expert has examined them. Agreement among AI checks is evidence
  about a process, not independent validation.
- No rate of convergence or second-order term is proved. The theorem
  concerns the limiting operators; a growing-index statement for the finite
  matrices needs an explicit operator-norm error bound.
- The kernel is positive after a change of signs and the proof uses no
  cancellation in Möbius sums. No new estimate for the Mertens function,
  prime counting, or zero-free regions follows.
- Whether the general transfer holds under regular variation of the mass
  count alone is open (paper Question 7.1).

## Reproduce

Requirements: pdfLaTeX (tested with TeX Live 2021) and Poppler's `pdfinfo` and
`pdftotext`. The checker uses only the Python standard library and must run
from an isolated environment:

```sh
python3 -m venv .venv            # any Python 3.9+ interpreter
make paper                        # four pdfLaTeX passes; fixed SOURCE_DATE_EPOCH
make check                        # labels, citations, TeX log, and PDF text
shasum -a 256 -c MANIFEST.sha256
```

`make check` checks the document's consistency; it does not check proofs.

## Repository contents

- `paper/`: LaTeX source (`main.tex`, `sections/`) and the reading copy
  `main.pdf`.
- `scripts/check_paper.py`: document consistency checker.
- `audit/`: the prior-art record, the proof-review history, and their
  dispositions.
- `ADMISSION.md`, `VERIFICATION.md`, `CORRECTIONS.md`, `CITATION.cff`,
  `MANIFEST.sha256`: release records. `audit/LEDGER.md` lists every audit
  finding and its disposition.

## Role of AI

AI did the derivations, literature search, exposition, and audits under the
author's direction. The author chose the questions and is responsible for the
result and its corrections.

## License

GPL-3.0-only. See [LICENSE](LICENSE).
