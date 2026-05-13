# Changelog

All notable changes to Boustrophidon are documented here.

## [1.0.0] - 2026-05-13

### Added

- Public command `\boustrophidon[<keys>]{<text>}`.
- Modes `Type=Any`, `Type=Archaic`, and `Type=Classical`.
- Automatic wrapping based on the current `\linewidth`.
- Explicit line breaks with `\\`.
- `LineWidth=Auto|<dimension>` override.
- `start=LTR|RTL` initial direction control.
- `resetDirection=Page|Paragraph`.
- `ObscureLetters=On|Off` for koppa/digamma and related transliteration handling.
- `inLine=True|False` for transforming only bracketed spans inside ordinary text.
- Start/stop API with `\startBoustrophidon[<keys>] ... \stopBoustrophidon`.
- Compatibility aliases for earlier command names.
- Demo and template files with TeXStudio magic comments for XeLaTeX.

### Changed

- README updated to match the actual v1 feature set.
- Demo log cleaned by avoiding known missing glyph inputs in the `ObscureLetters=Off` contrast test.
- Regex punctuation normalization adjusted to avoid noisy endpoint warnings.

### Verified

- `boustrophidon_demos.tex` builds with XeLaTeX.
- `boustrophidon_template.tex` builds with XeLaTeX.
- Inline `Type=Classical` now renders using the Classical epigraphic font instead of plain mirrored Latin text.

## Pre-1.0

- Internal development versions before the stable release.
