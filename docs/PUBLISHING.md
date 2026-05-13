# Publishing Workflow

This is the proposed step-by-step workflow for Boustrophidon v1.

## 1. Prepare Repository

Create a GitHub repository named `boustrophidon` or `latex-boustrophidon`.

Recommended top-level layout:

```text
boustrophidon/
  boustrophidon.sty
  README.md
  LICENSE
  CHANGELOG.md
  examples/
    boustrophidon_template.tex
    boustrophidon_template.pdf
    boustrophidon_demos.tex
    boustrophidon_demos.pdf
  docs/
    RELEASE_NOTES_v1.0.0.md
    TEST_MATRIX.md
    CTAN.md
```

## 2. Build Locally

```powershell
xelatex -interaction=nonstopmode -halt-on-error boustrophidon_demos.tex
xelatex -interaction=nonstopmode -halt-on-error boustrophidon_template.tex
```

Review the generated PDFs before tagging.

## 3. Commit

Commit only source, docs, and intended PDFs. Do not commit `*.aux`, `*.log`, or `*.synctex.gz`.

Suggested commit message:

```text
Release Boustrophidon v1.0.0
```

## 4. Tag

```powershell
git tag -a v1.0.0 -m "Boustrophidon v1.0.0"
git push origin main
git push origin v1.0.0
```

## 5. Create GitHub Release

Use `RELEASE_NOTES_v1.0.0.md` as the release body.

Attach a release zip containing:

- `boustrophidon.sty`
- `README.md`
- `LICENSE`
- `CHANGELOG.md`
- examples and PDFs

## 6. After GitHub Release

Open a fresh clone/download of the release archive and compile the examples once more. This catches missing files before wider publication.
