# Slides: structured LaTeX source

## Compile

Select **XeLaTeX**, set `main.tex` as the main document, and compile. On Overleaf, the normal build handles BibTeX automatically.

For a local TeX Live or MiKTeX installation:

```sh
xelatex -interaction=nonstopmode -halt-on-error main.tex
bibtex main
xelatex -interaction=nonstopmode -halt-on-error main.tex
xelatex -interaction=nonstopmode -halt-on-error main.tex
```

Alternatively use `./build.sh`, `build.bat` on Windows, or `latexmk main.tex`. The included `main.bbl` is a generated bibliography; edit `references.bib` and rerun BibTeX when changing entries. The included `compiled.pdf` is the verified build.

## Structure

- `main.tex`: main Beamer document and ordered section inputs.
- `sections/`: context and physics, data and representation, latent propagators, results and uncertainty, conclusions, and references.
- `appendices/`: representation/operator-theory backup frames and data/training/diagnostic backup frames.
- `frontmatter/title_frame.tex`: editable title frame and institutional logos.
- `references.bib`: 29 structured BibTeX references used in the presentation.
- `images/`: context-named raster figures and vector diagrams.
- `preamble.tex`: Beamer typography, colors, blocks, page design and citations.
- `fonts/`: local font assets used by the source.

- `verification/`: compilation results, source checks and comparison notes.
- `tex-text.tec`: local XeTeX punctuation mapping used by fontspec.

The presentation has 46 actual Beamer `frame` environments, grouped by topic rather than exported page files. Formulae, prose, bullets, tables and citations are editable LaTeX. Existing scientific plots and recovered vector diagrams are assets in `images/`.

## Edit the project

Edit the chapter or section files directly. Image commands use `\includegraphics` with meaningful names such as `fno_longitudinal_reconstruction.png`, `gno_longitudinal_slices.png`, and `transformer_window_study.png`. Replace an image file in `images/` and recompile to update that figure.

Citations use meaningful keys such as `\cite{ghribi2026updates}` in the thesis or `\parencite{vaswani2017attention}` in the slides. Add or change bibliographic metadata in `references.bib`, then run the build sequence above.

The PNG plots retain their original embedded pixel data. Where the original PDF stored a vector diagram, its reusable vector figure is supplied as a context-named PDF in `images/`. The underlying plotting notebooks and original TikZ source are not contained in the supplied PDFs.

## Comparison with the supplied PDF

This version prioritizes the requested conventional editable source structure. It was manually reconstructed from the printed content, including the numbered mathematical expressions and tables. The original high-level source files were unavailable.

The rebuilt output is **not pixel-identical** to the supplied PDF. Native text and mathematics reflow, and kerning, figure placement, line/page breaks, some styling and bibliography formatting differ. See `verification/REPORT.md` for the actual output page count and the completed checks. Compilation success and structural completeness must not be interpreted as a visual-identity result.
