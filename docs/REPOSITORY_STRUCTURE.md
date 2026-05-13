# Recommended Repository Structure

For GitHub, this structure is cleaner than keeping every file flat at the root.

```text
boustrophedon/
  README.md
  LICENSE
  CHANGELOG.md
  VERSION
  CITATION.cff
  boustrophedon.sty
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
    MANIFEST.md
    TEST_MATRIX.md
    PUBLISHING.md
    CTAN.md
    PACKAGE_METADATA.md
    RELEASE_CHECKLIST.md
    CONTRIBUTING.md
    SECURITY.md
```

For GitHub, keep examples and operational docs in folders so the project is easy to scan. For CTAN, keep the archive layout consistent with `docs/CTAN.md`.

## Suggested GitHub Commit

```text
Release Boustrophedon v1.1.0
```

## Suggested Release Tag

```text
v1.1.0
```
