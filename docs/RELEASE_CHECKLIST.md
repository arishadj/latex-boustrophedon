# Release Checklist

Use this checklist for the actual v1 release pass.

## Files

- [ ] `boustrophidon.sty` version/date is correct.
- [ ] `README.md` matches the implemented API.
- [ ] `CHANGELOG.md` includes the release date.
- [ ] `LICENSE` is present.
- [ ] `VERSION` is `1.0.0`.
- [ ] `CITATION.cff` repository URL has been updated.
- [ ] Demo and template PDFs are regenerated from the release folder.
- [ ] No temporary build files are included.

## Compile

- [ ] `xelatex -interaction=nonstopmode -halt-on-error boustrophidon_demos.tex`
- [ ] `xelatex -interaction=nonstopmode -halt-on-error boustrophidon_template.tex`
- [ ] Demo PDF visually checked.
- [ ] Template PDF visually checked.

## GitHub

- [ ] Repository created.
- [ ] Files committed.
- [ ] GitHub topics set.
- [ ] Release tag `v1.0.0` created.
- [ ] GitHub Release created from `RELEASE_NOTES_v1.0.0.md`.
- [ ] Release zip attached or auto-generated archive verified.

## After Release

- [ ] Download the GitHub release archive.
- [ ] Compile examples from the downloaded archive.
- [ ] Decide whether the next target is CTAN, Overleaf Gallery, or both.
