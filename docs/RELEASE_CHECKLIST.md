# Release Checklist

Use this checklist for each release pass.

## Files

- [ ] `boustrophedon.sty` version/date is correct.
- [ ] `README.md` matches the implemented API.
- [ ] `CHANGELOG.md` includes the release date.
- [ ] `LICENSE` is present.
- [ ] `NOTICE` is present.
- [ ] `VERSION` matches the release being prepared.
- [ ] `boustrophedon.dtx` is present.
- [ ] `boustrophedon.ins` generates `boustrophedon.sty`.
- [ ] `boustrophedon.pdf` builds from `boustrophedon.dtx`.
- [ ] `CITATION.cff` repository URL has been updated.
- [ ] Demo and template PDFs are regenerated from the release folder.
- [ ] No temporary build files are included.

## Compile

- [ ] `latex -interaction=nonstopmode -halt-on-error boustrophedon.ins`
- [ ] `xelatex -interaction=nonstopmode -halt-on-error boustrophedon.dtx`
- [ ] `xelatex -interaction=nonstopmode -halt-on-error -output-directory=examples examples/boustrophedon_demos.tex`
- [ ] `xelatex -interaction=nonstopmode -halt-on-error -output-directory=examples examples/boustrophedon_template.tex`
- [ ] Package manual visually checked.
- [ ] Demo PDF visually checked.
- [ ] Template PDF visually checked.

## GitHub

- [ ] Repository created.
- [ ] Files committed.
- [ ] GitHub topics set.
- [ ] Release tag created for the current `VERSION`.
- [ ] GitHub Release created from the matching release notes.
- [ ] Release zip attached or auto-generated archive verified.

## After Release

- [ ] Download the GitHub release archive.
- [ ] Compile examples from the downloaded archive.
- [ ] Decide whether the next target is CTAN, Overleaf Gallery, or both.
