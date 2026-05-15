# Changelog

All notable changes to Boustrophedon are documented here.

## [1.1.0] - 2026-05-13

### Added

- CTAN-oriented documented source package files:
  - `boustrophedon.dtx`
  - `boustrophedon.ins`
- GitHub issue templates for bug reports and feature requests.
- Manual/documentation build path from `boustrophedon.dtx`.

### Changed

- Project identity corrected to `boustrophedon`.
- Public package file renamed to `boustrophedon.sty`.
- Public command renamed to `\boustrophedon[<keys>]{<text>}`.
- Start/stop API renamed to `\startBoustrophedon[<keys>] ... \stopBoustrophedon`.
- Package metadata updated for the v1.1.0 documented-source distribution.
- Release documentation refreshed for GitHub and CTAN-oriented publication.

## [1.0.0] - 2026-05-13

### Added

- Public command `\boustrophedon[<keys>]{<text>}`.
- Modes `Type=Any`, `Type=Archaic`, and `Type=Classical`.
- Automatic wrapping based on the current `\linewidth`.
- Explicit line breaks with `\\`.
- `LineWidth=Auto|<dimension>` override.
- `start=LTR|RTL` initial direction control.
- `resetDirection=Page|Paragraph`.
- `ObscureLetters=On|Off` for koppa/digamma and related transliteration handling.
- `inLine=True|False` for transforming only bracketed spans inside ordinary text.
- Start/stop API with `\startBoustrophedon[<keys>] ... \stopBoustrophedon`.
- Convenience commands for common modes.
- Demo and template files with TeXStudio magic comments for XeLaTeX.

### Changed

- README updated to match the actual v1 feature set.
- Demo log cleaned by avoiding known missing glyph inputs in the `ObscureLetters=Off` contrast test.
- Regex punctuation normalization adjusted to avoid noisy endpoint warnings.

### Verified

- `examples/boustrophedon_demos.tex` builds with XeLaTeX.
- `examples/boustrophedon_template.tex` builds with XeLaTeX.
- Inline `Type=Classical` now renders using the Classical epigraphic font instead of plain mirrored Latin text.

## Pre-1.0

- Internal development versions before the stable release.
