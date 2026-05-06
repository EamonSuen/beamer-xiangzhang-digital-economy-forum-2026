# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project

Chinese academic Beamer presentation for "数字化转型的投资结构优化效应" (Digital Transformation Investment Structure Optimization). Built with XeLaTeX + ctex + biblatex.

## Build

```bash
latexmk -xelatex -outdir=output main.tex
```

Output PDF: `output/main.pdf`. Only clean aux files when the user explicitly asks:
```bash
latexmk -c -outdir=output main.tex
```

## Font configuration

The font root is set in `main.tex` as `\FontRoot`. It points to a local clone of https://github.com/Haixing-Hu/latex-chinese-fonts. If the presentation fails to compile on a new machine, update this path.

## File structure

- `main.tex` — entry point: packages, theme, fonts, metadata, section order. Edit only for global config.
- `sections/01_intro.tex` through `sections/05_conclusion.tex` — presentation body, organized for a 20-minute talk.
- `sections/00_slide_gallery.tex` — reference gallery of Beamer styles/layouts. Not production content; use as a pattern library.
- `sections/99_appendix.tex` — backup slides and Q&A prep (commented out by default).
- `tables/*.tex` — reusable regression table fragments (`\input` into slides).
- `figures/paper/` — paper figures (event study plots, trend charts, framework diagram).
- `references.bib` — bibliography.

## Editing conventions

- Keep frames focused: one claim, result, figure, or table per slide.
- Use the custom tcolorbox environments for academic emphasis: `regressionbox`, `findingbox`, `methodbox`, `robustbox`, `policybox`, `cautionbox`.
- For new slides, look at `sections/00_slide_gallery.tex` for applicable layout patterns, then adapt to the user's content.
- Use `\input{tables/...}` for table fragments, `\includegraphics` for figures (paths relative to project root).
- Citations via `\cite`, `\textcite`, or `\parencite` with biblatex authoryear style.
- When slides are overfull, prefer splitting frames or using `columns` over shrinking text.

## Safety

- Never run recursive deletion, `git clean`, `git reset --hard`, `rm -rf`, or similar commands.
- Do not edit generated files (`.aux`, `.bbl`, `.log`, `.pdf`, etc.) in `output/`.
- Before overwriting a file, check `git status --short` to avoid clobbering user work.
