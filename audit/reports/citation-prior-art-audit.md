# Citation and prior-art audit, with fast-follow scan — 2026-10-23

Auditor: a process-separated AI agent (Sonnet), read-only. The report was
returned through the agent interface and saved here by the root agent, with
its findings preserved. Local paths are omitted.

## Verdict: PARTIAL

There are no blockers. Several locators could not be re-checked in this
lane, and three bibliography entries were stale.

## 1. Citation mechanics

- All 12 bibliography items are cited, and the TeX log has no undefined
  citations.
- Crossref matches:
  - Hilberdink 2017 (LAMA 65(4) 813–829);
  - Kline 2019 (LAA 581, 354–366);
  - Hildebrand–Tenenbaum (JTNB 5(2) 411–484);
  - Kigami–Lapidus (CMP 158, 93–125, doi:10.1007/bf02097233).
- EIP was not re-checked in this lane.
- Published versions exist for three cited preprints:
  - Evans–Harris–Lang: Proc. London Math. Soc. 83(2) (2001) 390–418,
    doi:10.1112/plms/83.2.390.
  - Bendikov–Grigor'yan–Pittet–Woess: Uspekhi Mat. Nauk 69(4) (2014) 3–102,
    doi:10.4213/rm9602.
  - Hilberdink–Pushnitski 2021: St. Petersburg Math. J. 34(3) (2023) 463–481,
    doi:10.1090/spmj/1764.
- No journal version was found for arXiv:2401.06892 or arXiv:1811.05210.
  Crossref returned a related 2021 Springer chapter by the BGM authors, with
  a different title, which was not verified. Not finding a version is not
  proof that none exists.
- **Must fix (low severity):** update the three stale "preprint" entries.

## 2. Attribution placement

- **Confirmed:**
  - HP21 eq. (1.5), the ρ = ½ constant, and the diagonal remark;
  - HP21 Theorem 1.1 is a power law;
  - Gallager Theorem 4.7.3 is the key renewal theorem, at printed p. 202;
  - the BGM abstract (discrete spectrum of Schrödinger perturbations of a
    homogeneous hierarchical Laplacian; CLR- and Bargmann-type asymptotics)
    gives no theorem for this operator, so the paper's hedge is accurate.
- **Not verified in this lane (budget):**
  - BGPW Theorem 3.8;
  - EHL's limit and its finite-degree hypothesis;
  - HT pp. 414, 422, 426, eq. (2.3) and Lemma 2.6.

## 3. Bounded prior art

Nothing accessible gives λ_r ~ c0/(r log r) for this kernel, or the
cylinder-Gram/tree-sandwich mechanism. The bounded wording is appropriate
and should not be strengthened. The Carleson-embedding comparison remains
open: an arXiv query returned 0 hits and no literature was read. The
Kigami–Lapidus gap is adequately disclosed.

## 4. Fast-follow scan (2026-10-23)

| # | Index | Query | Result |
|---|---|---|---|
| 1 | arXiv API (http) | `id_list` of 5 cited IDs | 0 bytes: NOT PERFORMED |
| 2 | arXiv API (https) | same | 5 records |
| 3 | arXiv API | `all:"Mertens" AND (all:"singular values" OR all:"eigenvalue asymptotics")`, by date | 0 hits (valid response) |
| 4 | arXiv API | `all:"Redheffer" AND (all:eigenvalue OR all:"singular value")` | 3 hits (2025 inequality remark, 2025 Redheffer largest singular vector, 2019 unitary analog), titles only; none from 2026 |
| 5 | arXiv API | `all:"largest prime factor" AND (eigenvalue OR "compact operator" OR "singular values")` | 1 irrelevant hit |
| 6 | arXiv API | `(squarefree OR Mobius OR arithmetic) AND "eigenvalue asymptotics" AND tree` | 0 hits |
| 7 | GitHub | `gh search repos "sparse-mertens-singular-spectrum"` | the author's own repository only |
| 8 | GitHub | `gh search repos "mertens eigenvalue kernel squarefree"` | 0 hits |
| 9 | GitHub | `gh search code "sparse-mertens-singular-spectrum"` | `[]`; NOT PERFORMED as evidence (code search may need authentication) |
| 10 | Zenodo API | `"sparse Mertens" OR "singular spectrum of a sparse Mertens"`, most recent | 3 records, all by the author |
| 11 | Crossref (×12) | title and DOI lookups | 3 failed or unusable |

**NOT PERFORMED:**
- broad arXiv queries on "1/(r log r)" laws, "Möbius operator" and
  "ultrametric Gram";
- further Zenodo and GitHub-topic searches;
- MathSciNet, zbMATH and Google Scholar;
- citation tracking of the predecessor DOI beyond rows 7–10.

**Operations:** 26 of 25 allowed, one over budget. Substantive reads: 3.

## Must fix before tagging

1. Update the stale preprint entries (EHL, BGPW, HP21).
2. Verify the HT, BGPW and EHL locators against primary texts.
