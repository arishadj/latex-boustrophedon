# Publishing Workflow

This is the step-by-step workflow for Boustrophedon releases.

## 1. Prepare Repository

Create a GitHub repository named `boustrophedon` or `latex-boustrophedon`.

Recommended top-level layout:

```text
boustrophedon/
  boustrophedon.sty
  README.md
  LICENSE
  CHANGELOG.md
  boustrophedon.dtx
  boustrophedon.ins
  boustrophedon.pdf
  examples/
    boustrophedon_template.tex
    boustrophedon_template.pdf
    boustrophedon_demos.tex
    boustrophedon_demos.pdf
  docs/
    RELEASE_NOTES_v1.1.0.md
    TEST_MATRIX.md
    CTAN.md
```

## 2. Build Locally

```powershell
latex -interaction=nonstopmode -halt-on-error boustrophedon.ins
xelatex -interaction=nonstopmode -halt-on-error boustrophedon.dtx
xelatex -interaction=nonstopmode -halt-on-error -output-directory=examples examples/boustrophedon_demos.tex
xelatex -interaction=nonstopmode -halt-on-error -output-directory=examples examples/boustrophedon_template.tex
```

Review the generated PDFs before tagging.

## 3. Commit

Commit only source, docs, and intended PDFs. Do not commit `*.aux`, `*.log`, or `*.synctex.gz`.

Suggested commit message:

```text
Release Boustrophedon v1.1.0
```

## 4. Tag

```powershell
git push origin main
git tag -a v1.1.0 -m "Boustrophedon v1.1.0"
git push origin v1.1.0
```

## 5. Create GitHub Release

Use `RELEASE_NOTES_v1.1.0.md` as the release body.

Attach or verify a GitHub release bundle containing:

- `boustrophedon.sty`
- `README.md`
- `LICENSE`
- `NOTICE`
- `CHANGELOG.md`
- `boustrophedon.dtx`
- `boustrophedon.ins`
- `boustrophedon.pdf`
- examples and PDFs

## 6. After GitHub Release

Open a fresh clone/download of the release archive and compile the examples once more. This catches missing files before wider publication.

## 7. Prepare CTAN Upload

Prepare a separate CTAN archive without generated package files. Include the
compiled example PDFs so CTAN can preserve the demonstrated output:

```text
boustrophedon/
  README.md
  LICENSE
  NOTICE
  CHANGELOG.md
  boustrophedon.dtx
  boustrophedon.ins
  boustrophedon.pdf
  examples/
    boustrophedon_demos.tex
    boustrophedon_demos.pdf
    boustrophedon_template.tex
    boustrophedon_template.pdf
```

Test the CTAN archive from a fresh temporary directory before uploading.
