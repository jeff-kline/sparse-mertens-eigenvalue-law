# Claim and public-prose audit — 2026-10-23

Auditor: a process-separated AI agent (Sonnet), read-only. The report was
returned through the agent interface and saved here by the root agent. Its
wording is preserved; only the layout is tightened. Local paths are omitted.

## Verdict: PARTIAL

The claim, constants, asymptotics, limitations, prior-work credit and
novelty qualification agree across surfaces. Four items must be fixed, all
about dangling references or implied public status.

`git status` showed no commits, with untracked candidate files. The standard
was fetched, but the fetch tool returned only a condensed summary. Judged
against it: the abstract, repository summary and paper must state the same
result; model agreement is not peer review; narrowing a novelty claim is a
visible correction.

## Checks that pass

- **1. What is new.** It follows the Introduction and is separate from
  "Earlier work". The principal bullet states hypotheses and conclusion, not
  only method. Restatements are marked (Prop 6.1 = predecessor Thm 4.3). Paper
  finite.tex agrees. related.tex and PRIOR-ART.md agree that the arithmetic
  count is not new in method.
- **2. Introduction and abstract.** The README Introduction tracks the
  abstract closely: same object, result, deflation, proof outline, and "no
  rate / no Mertens estimate". It is not a generic essay.
- **3. Consistency.** Title, author, version 0.1.0, and 6/π² = c0 with δ_k
  agree. The three asymptotics take the same form on every surface. The
  novelty statement is "not found in sources checked, not worldwide". The
  principal result count is one on every surface.
- **4. Section numbers.** Every README section number checks against
  main.aux, and REVIEW-HISTORY references are consistent with the source.
  Remark A.5's exact number was not checked against the aux.
- **7. README math.** README has zero `$` characters, so the GitHub
  inline-math pitfalls do not apply.
- **6. Status.** No wording implies a DOI or admission for this release. The
  only DOI is the predecessor's.
- **PDF.** The rendered abstract and title block match main.tex, and the PDF
  is newer than all sources.

## Must fix

1. README points to `MANIFEST.sha256` and `VERIFICATION.md`, which do not
   exist yet. Create them before the freeze or delete the references.
2. ADMISSION.md and RELEASE-PLAN.md cite "paper (1.1)" for K. The PDF numbers
   that equation (1). Use "paper (1)".
3. CITATION.cff gives `repository-code` and `url` for a repository that does
   not exist and is not authorized. Remove both keys until authorized, and
   mark the file as a candidate.
4. CORRECTIONS.md invites reports at a public issue-tracker URL that does not
   exist. Precede it with "Once the repository is public,".

## Optional

- **Undefined terms.** `L` and "rank-one deflation" appear in the README
  without the formula. "Cylinder sets", "mass", "Schatten class", "profile
  condition", "regular variation" and the eigenvalue ordering are also
  undefined before use.
- **Abstract coverage.** The abstract and README Introduction state two of
  the three asymptotics. This is consistent; no change is recommended.
- **Process language.** It appears only in audit records and the AI-role
  disclosure, which are allowed. The CORRECTIONS.md lines could optionally be
  softened.
- **Evidence level.** "Proved on paper, conditional on the cited classical
  estimates" is honest; keep it.
- **Dates.** README has no date line, and the CFF has no date-released.
  Neither is wrong.
- **tmp/.** It should be excluded from the freeze.
- **Pending items.** The pending fast-follow scan and the open comparisons
  are stated consistently.
