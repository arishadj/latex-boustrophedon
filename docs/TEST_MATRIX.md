# Test Matrix

Use this checklist before tagging a release.

## Compile Tests

| File | Engine | Expected result | Status |
| --- | --- | --- | --- |
| `boustrophidon_demos.tex` | XeLaTeX | PDF builds, 6 pages | Passed 2026-05-13 |
| `boustrophidon_template.tex` | XeLaTeX | PDF builds, 1 page | Passed 2026-05-13 |

## Feature Tests

| Feature | Demo section | Expected behavior |
| --- | --- | --- |
| Default `Type=Any` wrapping | 1 | Alternating mirrored lines after automatic wrapping |
| Explicit line breaks | 2, 2b | `\\` creates separate alternating lines |
| Archaic rendering | 3, 3b, 5, 10 | Archaic glyph mapping and reverse lines work |
| Classical rendering | 4, 4b, 4c, 6, 7, 8, 9 | Classical glyph mapping and reverse lines work |
| `LineWidth` | 4b | Explicit width changes wrapping target |
| `ObscureLetters` | 8, 8b, 8c | Koppa/digamma handling can be enabled or disabled |
| `resetDirection` | 11 | Page mode continues; Paragraph mode resets |
| `inLine=True` | 12 | Only bracketed spans are transformed |
| `Type=Classical,inLine=True` | 12 | Bracketed span renders with Classical glyphs |

## Log Review

Acceptable:

- Overfull boxes caused by displayed verbatim input examples.
- MiKTeX update notices.

Not acceptable:

- `! LaTeX Error`
- `Fatal error`
- `Undefined control sequence`
- `Missing character` for supported demo inputs
