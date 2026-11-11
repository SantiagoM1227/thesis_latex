# Build and reconstruction verification

| Check | Result |
| --- | --- |
| XeLaTeX → BibTeX → XeLaTeX → XeLaTeX | All commands returned 0 |
| Missing font characters | 0 |
| Unresolved citations or references | 0 |
| Duplicate labels | 0 |
| Image files referenced by source | All present |
| BibTeX keys referenced by source | All present |
| Text extending outside PDF page bounds | None detected |
| Original PDF pages | 97 |
| Rebuilt PDF pages | 96 |
| Pixel-identical to original | **No** |

The thesis contains seven chapter sources, two appendix sources, 260 numbered native equations, 21 figure environments, nine editable numerical tables, 38 acronym entries, 71 glossary entries and 37 symbol entries. An English three-word-sequence diagnostic covered 98.7% of the sequences in 150 substantive original prose blocks; no block scored below 72%. This is a diagnostic and does not prove textual or mathematical identity.

All rebuilt pages were rendered and visually inspected in contact sheets, with additional inspection of representative equation-heavy pages, figures and slide diagrams. Compilation warnings about underfull boxes or Beamer's explicit frame fitting are retained in the log. The thesis has one 0.114 pt horizontal overfull-box report; it is below one display pixel at common viewing scales.

The source organization is conventional LaTeX: the main document inputs chapter/section files, figures are loaded with `\includegraphics` from `images/`, and the bibliography is generated from `references.bib`. Compilation does not require the original PDF.

**Remaining differences:** text and mathematics reflow, kerning and typography differ, figure positions and line/page breaks change, and the bibliography uses standard BibTeX formatting. These are reconstructed source files, not the lost original authoring files. The earlier pixel-identity claim does not apply to this structured version.

The compiled PDF SHA-256 is `266b0ccd335bd39f6837092629eb9358bc27f82ec2670fd5dad14bc5d34bee40`.
