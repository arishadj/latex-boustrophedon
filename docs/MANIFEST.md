# Manifest

This file describes the Boustrophedon release package.

## Repository and GitHub Release

- `boustrophedon.sty` - LaTeX package file.
- `boustrophedon.dtx` - Documented source for CTAN-style distribution.
- `boustrophedon.ins` - Docstrip installer that generates `boustrophedon.sty`.

## Documentation

- `README.md` - Main user documentation.
- `boustrophedon.pdf` - Package manual generated from `boustrophedon.dtx`.
- `CHANGELOG.md` - Version history.
- `RELEASE_NOTES_v1.1.0.md` - Human-readable release summary.
- `LICENSE` - License declaration.
- `NOTICE` - Package copyright, maintainer, and LPPL status.
- `CONTRIBUTING.md` - Contribution guidelines.
- `SECURITY.md` - Security/contact policy.

## Examples

- `examples/boustrophedon_template.tex` - Minimal starter template.
- `examples/boustrophedon_template.pdf` - Compiled template.
- `examples/boustrophedon_demos.tex` - Full demo/test document.
- `examples/boustrophedon_demos.pdf` - Compiled demo output.

## CTAN Upload

The CTAN upload archive should include the source files and manual, but not
generated package or example output files:

- `README.md`
- `LICENSE`
- `NOTICE`
- `CHANGELOG.md`
- `boustrophedon.dtx`
- `boustrophedon.ins`
- `boustrophedon.pdf`
- `examples/boustrophedon_template.tex`
- `examples/boustrophedon_demos.tex`

Do not include `boustrophedon.sty` in the CTAN upload archive; it is generated
from `boustrophedon.dtx` by `boustrophedon.ins`.

## Release Operations

- `TEST_MATRIX.md` - Manual and compile test checklist.
- `PUBLISHING.md` - Step-by-step GitHub release workflow.
- `CTAN.md` - Notes for future CTAN submission.

## Not Included

The following temporary build files should not be included in release archives:

- `*.aux`
- `*.log`
- `*.out`
- `*.toc`
- `*.idx`
- `*.ilg`
- `*.ind`
- `*.glo`
- `*.gls`
- `*.hd`
- `*.xdv`
- `*.fls`
- `*.fdb_latexmk`
- `*.synctex.gz`
- temporary render images
