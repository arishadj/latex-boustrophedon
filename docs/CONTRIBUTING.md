# Contributing

Thank you for helping improve Boustrophedon.

## Development Setup

Use XeLaTeX for development and testing:

```powershell
latex -interaction=nonstopmode -halt-on-error boustrophedon.ins
xelatex -interaction=nonstopmode -halt-on-error boustrophedon.dtx
xelatex -interaction=nonstopmode -halt-on-error -output-directory=examples examples/boustrophedon_demos.tex
xelatex -interaction=nonstopmode -halt-on-error -output-directory=examples examples/boustrophedon_template.tex
```

## Before Opening a Pull Request

- Keep changes focused.
- Update `README.md` when public behavior changes.
- Add or update a demo section when adding a feature.
- Rebuild the demo/template PDFs when release artifacts are expected.
- Review the log for LaTeX errors and missing glyph warnings.

## Coding Style

- Prefer existing `expl3` patterns already used in `boustrophedon.sty`.
- Keep user-facing keys documented.
- Preserve backward-compatible aliases unless there is a release note explaining removal.

## Reporting Issues

Please include:

- LaTeX engine and version.
- Operating system.
- Minimal `.tex` example.
- Relevant log excerpt.
- Expected output and actual output.
