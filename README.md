# Boustrophedon (LaTeX)

## LaTeX Package

**Created by Aris Chatzichristos, PhD**

---

## Overview

This package typesets text in *boustrophedon* style, alternating the writing direction on each line.

Have you ever wondered why most Western languages are written left-to-right, while many Middle Eastern languages are written right-to-left? Both conventions may seem arbitrary today—but this was not always the case.

In one of the earliest fully developed alphabets, the Archaic Greek alphabet (from *alpha* and *beta*, hence “alphabet”), writing was often performed *boustrophedon*, meaning “as the ox turns in ploughing.” Text was written left-to-right on one line, then right-to-left on the next, with both the direction of the text *and the letterforms themselves* mirrored accordingly.

This method creates a continuous flow of reading, as the reader does not need to jump back to the start of each new line, but instead follows the text in a natural back-and-forth motion.

Reading takes some getting used to, but after a while it becomes surprisingly natural. One may also observe that:

- Capital letters (both in the Latin alphabet and especially in the Greek alphabet) are particularly well-suited to this type of writing, and are much easier to read than lowercase letters (which were developed later in both systems).
- For example, pairs such as *b* vs *d*, or cases like ὡ vs ὠ in polytonic Greek, can make reading more difficult, as the reader must keep mental track of the text direction.
- In contrast, capital Greek letters—already in use during the boustrophedon period—have the appropriate symmetry to be read in both directions without ambiguity.

This package brings an ancient writing paradigm into modern digital typography.

---

## Features

- Boustrophedon rendering (alternating line direction)
- Mirrored letterforms on alternating lines
- Automatic paragraph wrapping
- Explicit line breaks using `\\`
- Inline rendering with `inLine=True`, where only text inside `[ ... ]` is transformed
- Support for Latin transliteration and Greek Unicode text
- Archaic and Classical Greek transformations
- Optional digamma (Ϝ) and koppa (Ϙ) handling
- Configurable initial direction, reset policy, and line width

---

## Installation

For quick use, place `boustrophedon.sty` in the same directory as your `.tex` file, or install it in a local TeX tree.

For the documented-source distribution, generate the package file with:

```tex
latex boustrophedon.ins
```

This writes `boustrophedon.sty` from `boustrophedon.dtx`.

In TeXStudio, compile with **XeLaTeX**. The demo and template include these magic comments so TeXStudio can pick the right engine automatically:

```tex
% !TeX program = xelatex
% !TeX encoding = UTF-8
```

## Requirements

- XeLaTeX or LuaLaTeX recommended (Greek Unicode works best)
- LaTeX packages: `xparse`, `expl3`, `graphicx`, `iftex`, `greek6cbc`, `greek4cbc`

## License

Boustrophedon is distributed under the LaTeX Project Public License, version 1.3c or later. See `LICENSE` and `NOTICE`.

## Quick start

```tex
\usepackage[Type=Classical,ObscureLetters=On]{boustrophedon}

\boustrophedon{DHMOS ATHNAIWN \\ TIMWN ANDRA AGAQON \\ KAI SWFRONA}
```

Supported modes:

- `Type=Any` -- mirror whole line or inline span as generic text
- `Type=Archaic` -- epigraphic Greek rendering using `greek6cbc`
- `Type=Classical` -- epigraphic Greek rendering using `greek4cbc`

## Main command

```tex
\boustrophedon[<keys>]{<text>}
```

Keys:

- `Type=Any|Archaic|Classical` (default `Any`)
- `start=LTR|RTL` (default `LTR`)
- `resetDirection=Page|Paragraph` (default `Page`)
- `LineWidth=Auto|<dimension>` (default `Auto`) -- override target line width (e.g. `LineWidth=0.85\textwidth` or `LineWidth=0.85\linewidth`)
  - With `Auto`, the package targets `0.95\linewidth` and never exceeds the current `\linewidth`.
- `ObscureLetters=On|Off` (default `On`) -- enables koppa/digamma handling
- `inLine=True|False` (default `False`) -- keeps surrounding text normal and transforms only bracketed spans

Inline example:

```tex
\boustrophedon[inLine=True]{Normal text with [THIS PART] mirrored inline.}
\boustrophedon[Type=Classical,inLine=True]{A sentence with [DHMOS ATHNAIWN] embedded.}
```

In inline mode, `[ ... ]` acts as markup and the brackets are not intended as content.

Deprecated (kept for compatibility):

- `reset=paragraph|page` (same as `resetDirection`, but lowercase)
- `digammaAndKoppa=On|Off` (same as `ObscureLetters`)

## start/stop form

```tex
\startBoustrophedon[Type=Archaic]
ANDRA MOI ENNEPE MOUSA POLYTROPON ...
\stopBoustrophedon
```

## Demos

- `examples/boustrophedon_demos.tex` -> `examples/boustrophedon_demos.pdf`
- `examples/boustrophedon_template.tex` -> `examples/boustrophedon_template.pdf`
- `boustrophedon.dtx` -> `boustrophedon.pdf` package manual

## Release Status

Boustrophedon v1.1.0 adds CTAN-style `.dtx`/`.ins` packaging, a generated package manual, and GitHub issue templates for bug reports and feature requests.
