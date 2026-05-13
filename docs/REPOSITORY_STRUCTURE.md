# Recommended Repository Structure

For GitHub, this structure is cleaner than keeping every file flat at the root.

```text
boustrophidon/
  README.md
  LICENSE
  CHANGELOG.md
  VERSION
  CITATION.cff
  boustrophidon.sty
  examples/
    boustrophidon_template.tex
    boustrophidon_template.pdf
    boustrophidon_demos.tex
    boustrophidon_demos.pdf
  docs/
    RELEASE_NOTES_v1.0.0.md
    MANIFEST.md
    TEST_MATRIX.md
    PUBLISHING.md
    CTAN.md
    PACKAGE_METADATA.md
    RELEASE_CHECKLIST.md
    CONTRIBUTING.md
    SECURITY.md
```

For the first release, a flat archive is acceptable. For a maintained public repository, moving examples and operational docs into folders will make the project easier to scan.

## Suggested First GitHub Commit

```text
Initial Boustrophidon v1.0.0 release
```

## Suggested Release Tag

```text
v1.0.0
```
