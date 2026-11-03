# FEPS PGR LaTeX Training

Introductory LaTeX training materials for postgraduate researchers in the Faculty of Engineering and Physical Sciences (FEPS), University of Southampton.

This repository contains slides for four sessions and three downloadable template projects. The sessions introduce scientific document preparation, from a first LaTeX document to reports, bibliographies, mathematical writing, presentations, and diagrams.

## Session slides

| Session | Topics | Slides |
| --- | --- | --- |
| **1. Introduction** | What LaTeX is; Overleaf and local compilation; document structure; basic document and text formatting; lists; comments; common compilation errors. | [Session 1 (PDF)](FEPS_PGR_LaTeX_Training_Session_1.pdf) |
| **2. Document Structure, Formatting and Figures** | Organising larger documents; loading and creating packages; inserting, resizing, and positioning figures; subfigures; labels and cross-references. | [Session 2 (PDF)](FEPS_PGR_LaTeX_Training_Session_2.pdf) |
| **3. Tables, Bibliography and Mathematics** | Tables with `tabular`, `table`, and `booktabs`; bibliography management with `biblatex`; citations; inline and display mathematics; numbered and aligned equations. | [Session 3 (PDF)](FEPS_PGR_LaTeX_Training_Session_3.pdf) |
| **4. Beamer and TikZ** | Planning a presentation; Beamer frames, blocks, columns, themes, and overlays; figures and equations in slides; TikZ coordinates, nodes, arrows, and flowcharts. | [Session 4 (PDF)](FEPS_PGR_LaTeX_Training_Session_4.pdf) |

## Downloadable templates

Each ZIP contains editable source files and a compiled example PDF.

| Template | Contents | Download |
| --- | --- | --- |
| **Article** | A report-style article with separate section files, figures, a table, mathematics, custom macros, and a bibliography with examples of different entry types. | [article_template.zip](article_template.zip) |
| **Beamer** | An unofficial Southampton-style presentation with blocks, columns, figures, a table, equations, TikZ diagrams, overlays, and references. | [beamer_template.zip](beamer_template.zip) |
| **Simple bibliography** | A small `biblatex` example demonstrating author-year citations, a missing citation key, and a citation alias such as “Paper I”. | [simple_bibliography_template.zip](simple_bibliography_template.zip) |

## Getting started in Overleaf

1. Download the ZIP for the template you want to use. On the ZIP's GitHub file page, use **Download raw file** if the download does not start automatically.
2. Sign in to [Overleaf](https://www.overleaf.com/) and choose **New Project > Existing project (.zip)**. Upload the template ZIP as a separate project.
3. Click **Recompile**, then replace the example title, author, text, figures, and references with your own material. All three templates use **`biblatex` with Biber**; Overleaf normally runs the required bibliography steps automatically.

Overleaf uses **pdfLaTeX** by default and normally detects the main document automatically. If the wrong file is compiled, select the main document listed below under **Settings > Compiler > Main document**.

| Template | Main document | Included example PDF |
| --- | --- | --- |
| Article | `main_article_template.tex` | `main_article_template.pdf` |
| Beamer | `slides_beamer_template.tex` | `slides_beamer_template.pdf` |
| Simple bibliography | `main.tex` | `simple_bibliography_template.pdf` |

The included PDFs are previews. View or download the newly compiled output after making changes.

See Overleaf's [project upload guide](https://docs.overleaf.com/managing-projects-and-files/uploading-a-project) and [main document guide](https://docs.overleaf.com/getting-started/recompiling-your-project/the-main-document) for further help.

## Compiling locally

Extract a template ZIP and open a terminal inside the extracted template folder. Use a LaTeX installation that provides pdfLaTeX, Biber, and the packages loaded by the template.

For the article template, run:

```bash
pdflatex main_article_template.tex
biber main_article_template
pdflatex main_article_template.tex
pdflatex main_article_template.tex
```

For the Beamer template, replace `main_article_template` with `slides_beamer_template`. For the simple bibliography template, replace it with `main`. The Biber command takes the filename **without** the `.tex` extension.

Keep the accompanying `.sty`, `.bib`, section, and image files in their existing relative locations. The article requires `mymacros.sty`; the Beamer template requires `Sotonstyle.sty` and `frontpage_bg.png`.

## Notes on the teaching examples

- **An expected citation warning:** the simple bibliography template cites `smith2025`, which is deliberately absent from `references.bib`. This demonstrates an undefined citation. To resolve it, add the corresponding entry or remove or correct the citation.
- **Illustrative references:** some bibliography entries are fictional examples. Replace them with accurate source details before using a template for your own work.
- **Printing the bibliography:** the article template uses `\nocite{*}` to display every entry in `references.bib`. Remove that command if you want to list only cited entries.
- **Cross-references:** if a figure, table, or equation reference displays `??`, check its label and compile again. For unresolved citations, also check the citation key and run Biber.

## Credits

- **Session 1 and Session 2 slides:** Daniel Roberts, University of Southampton.
- **Session 3 and Session 4 slides:** Edisy Chan, University of Southampton.
- **Article, Beamer, and simple bibliography templates:** Edisy Chan, University of Southampton.

## Further resources

- [Overleaf: Learn LaTeX](https://www.overleaf.com/learn)
- [Bibliography management with biblatex](https://www.overleaf.com/learn/latex/Bibliography_management_with_biblatex)
- [Beamer](https://www.overleaf.com/learn/latex/Beamer)
- [TikZ](https://www.overleaf.com/learn/latex/TikZ_package)
- [Comprehensive TeX Archive Network (CTAN)](https://ctan.org/)
