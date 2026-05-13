# Boustrophidon v1.0.0 Release Notes

Boustrophidon is a LaTeX package for typesetting text in boustrophedon style:
the direction alternates line by line, and reverse lines mirror the text or
letterforms.

## Highlights

- Generic mirrored text with `Type=Any`.
- Archaic and Classical Greek epigraphic rendering with `Type=Archaic` and `Type=Classical`.
- Greek Unicode and Latin transliteration input.
- Automatic line wrapping and explicit `\\` line breaks.
- Inline mode:

```tex
\boustrophidon[inLine=True]{Normal text with [THIS PART] mirrored inline.}
```

- TeXStudio-ready demo/template files using XeLaTeX magic comments.

## Requirements

- XeLaTeX or LuaLaTeX recommended.
- Required LaTeX packages:
  `xparse`, `expl3`, `graphicx`, `iftex`, `greek6cbc`, `greek4cbc`.

## Known Notes

- pdfLaTeX can be used for plain transliteration workflows, but Greek Unicode is best with XeLaTeX or LuaLaTeX.
- In inline mode, square brackets `[ ... ]` are markup delimiters and are not printed as content.
- The demo includes some intentional overfull boxes in the displayed input examples because long `\detokenize` lines are shown verbatim.

## Release Contents

- `boustrophidon.sty`
- `README.md`
- `boustrophidon_demos.tex`
- `boustrophidon_demos.pdf`
- `boustrophidon_template.tex`
- `boustrophidon_template.pdf`
- Release support documents in this folder.
