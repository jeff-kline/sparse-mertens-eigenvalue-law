# Verification record — version 0.1.0

Recorded 2026-10-23; updated 2026-10-24 for the release.

## What is verified here

This record covers artifact consistency and reproducibility: the document
builds deterministically, its labels, citations and log are clean, and every
tracked file matches the manifest. It does not verify proofs. The proof audit,
source comparisons, and their dispositions are in `audit/LEDGER.md` and
`audit/reports/`.

No theorem in the paper rests on a numerical computation. Exploratory
finite-section and counting computations made while the result was being
developed are not part of the release evidence and are not reproduced here.

## Environment

| Tool | Version |
|---|---|
| pdfTeX | 3.141592653-2.6-1.40.22 (TeX Live 2021, MacPorts 2021.58693_2) |
| Python (checker, isolated `.venv`) | 3.9.6; standard library only |
| Poppler `pdfinfo` / `pdftotext` | 26.07.0 |
| OS | macOS (Darwin 25.6.0) |

The Makefile fixes `SOURCE_DATE_EPOCH=1792713600` (2026-10-23 00:00 UTC) and
`FORCE_SOURCE_DATE=1`, so the PDF creation date and identifiers are fixed.

## Commands and outputs

```sh
python3 -m venv .venv
make paper    # four pdfLaTeX passes, enough for a clean checkout to settle
make check
shasum -a 256 paper/main.pdf
shasum -a 256 -c MANIFEST.sha256
```

`make check` output (living copy, 2026-10-24):

```json
{
  "status": "PASS",
  "pages": 21,
  "source_files": 11,
  "labels": 62,
  "references": 115,
  "bibliography_entries": 13,
  "cited_entries": 13,
  "python": "3.9.6",
  "isolated": true,
  "errors": [],
  "scope": "Artifact consistency only; not proof or priority certification"
}
```

Reading copy in the archived release (tag `v0.1.0`):

```text
paper/main.pdf  21 pages
SHA-256 e22b7e98fb0c6c3b7cf093ef430891615bd4230b1da59aeae1bd157fcaa3c0b2
```

Living copy, rebuilt after archiving with the version DOI on its title page
(the only source change is the title-page status line and PDF subject):

```text
paper/main.pdf  21 pages
SHA-256 68e6f24f67a43a28366472868da07518be00ab425d053fa1f71175d99cded183
```

The checker fails on any of the following:

- duplicate or missing labels;
- missing bibliography keys or missing inputs;
- placeholder markers or local-path and workflow markers;
- TeX errors, overfull boxes, undefined or multiply defined references, or
  rerun warnings;
- unresolved `??` in the PDF text;
- a missing title-page author or version line.

## Fonts

The paper uses the TeX installation's default Computer Modern Type 1 fonts,
all embedded and subset. No font package is loaded.

## Clean-checkout reproduction

On 2026-10-24, `git archive` of the tagged commit `268da17` was extracted to
a fresh directory. The documented sequence (`python3 -m venv .venv`,
`make paper`, `make check`) reproduced the archived reading copy above, byte
for byte, and every manifest entry checked. Earlier candidates were
reproduced the same way (`audit/LEDGER.md`).
