# CTAN Preparation Notes

CTAN is the long-term publication route for a LaTeX package. GitHub can host the project immediately; CTAN is the route that can eventually make the package available through TeX Live and MiKTeX.

## Recommended Before CTAN

- Decide the final package name: `boustrophidon`.
- Keep one maintained public repository.
- Include a recognized license, preferably LPPL 1.3c or later.
- Confirm that dependencies are available in TeX Live and MiKTeX:
  `xparse`, `expl3`, `graphicx`, `iftex`, `greek6cbc`, `greek4cbc`.
- Add a concise package description.
- Add a maintainer email or contact URL.
- Consider converting to `.dtx`/`.ins` if aiming for a conventional CTAN package structure.

## Minimal CTAN-Oriented Archive

```text
boustrophidon/
  README.md
  LICENSE
  boustrophidon.sty
  boustrophidon_demos.tex
  boustrophidon_demos.pdf
  boustrophidon_template.tex
  boustrophidon_template.pdf
  CHANGELOG.md
```

## CTAN Upload Metadata Draft

- Package name: `boustrophidon`
- Caption: Typeset boustrophedon text in LaTeX
- License: LPPL 1.3c or later
- Author/Maintainer: Aris Chatzichristos
- Topics: Greek, fonts, text direction, typography
- Summary:

```text
Boustrophidon typesets text in boustrophedon style, alternating writing direction line by line. It supports generic mirrored text, Archaic and Classical Greek glyph rendering, automatic wrapping, explicit line breaks, and inline bracketed spans.
```

## Upload

Use the CTAN upload form after the GitHub v1 release has been tested from a clean archive:

https://ctan.org/upload
