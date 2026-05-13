# Boustrophedon v1.1.0 Release Notes

Boustrophedon v1.1.0 adopts the corrected package spelling throughout the
project and adds a documented-source distribution suitable for long-term
publication workflows.

## Highlights

- Added `boustrophedon.dtx` documented source.
- Added `boustrophedon.ins` docstrip installer.
- Added `boustrophedon.pdf` package manual generated from the documented source.
- Added GitHub issue templates for bug reports and feature requests.
- Renamed package, commands, examples, documentation, and metadata to
  `boustrophedon`.
- Refreshed release documentation for GitHub and CTAN-oriented publication.

## Notes

- The primary package file is now `boustrophedon.sty`.
- The primary command is now `\boustrophedon[<keys>]{<text>}`.
- The generated `boustrophedon.sty` is produced from `boustrophedon.dtx`.
- XeLaTeX or LuaLaTeX remains recommended, especially for Greek Unicode input.

## Build Checks

- `latex -interaction=nonstopmode -halt-on-error boustrophedon.ins`
- `xelatex -interaction=nonstopmode -halt-on-error boustrophedon.dtx`
- `xelatex -interaction=nonstopmode -halt-on-error -output-directory=examples examples/boustrophedon_demos.tex`
- `xelatex -interaction=nonstopmode -halt-on-error -output-directory=examples examples/boustrophedon_template.tex`

## GitHub Release Contents

- `boustrophedon.dtx`
- `boustrophedon.ins`
- `boustrophedon.sty`
- `boustrophedon.pdf`
- `README.md`
- `LICENSE`
- `NOTICE`
- `CHANGELOG.md`
- `examples/boustrophedon_demos.tex`
- `examples/boustrophedon_demos.pdf`
- `examples/boustrophedon_template.tex`
- `examples/boustrophedon_template.pdf`
- Release support documents in `docs/`.

## CTAN Upload Contents

The CTAN upload archive should include:

- `README.md`
- `LICENSE`
- `NOTICE`
- `CHANGELOG.md`
- `boustrophedon.dtx`
- `boustrophedon.ins`
- `boustrophedon.pdf`
- `examples/boustrophedon_demos.tex`
- `examples/boustrophedon_template.tex`

It should not include generated `boustrophedon.sty` or generated example PDFs.
