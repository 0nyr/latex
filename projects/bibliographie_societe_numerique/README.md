# Les bibliographies en LaTeX

### Useful links

##### tools

[bibliography generator | bibguru](https://app.bibguru.com/p/) 🌟

##### biblatex

[getting started with biblatex](https://www.overleaf.com/learn/latex/Articles/Getting_started_with_BibLaTeX)

[Biblatex bibliography styles](https://www.overleaf.com/learn/latex/Biblatex_bibliography_styles)

[Font sizes, families, and styles](https://www.overleaf.com/learn/latex/Font_sizes%2C_families%2C_and_styles#Font_sizes)

[Typesetting quotations (epigraph, quotations...)](https://www.overleaf.com/learn/latex/Typesetting_quotations)

[Biblatex full doc](http://linorg.usp.br/CTAN/macros/latex/contrib/biblatex/doc/biblatex.pdf) ⭐️

## Using biblatex

We use `biblatex`, a more powerful tool than the default `bibtex` for bibliography.

```shell
(base)  ❮ onyr ★  kenzae❯ ❮ bibliographie_societe_numerique❯❯ pdflatex main.tex 
This is pdfTeX, Version 3.14159265-2.6-1.40.20 (TeX Live 2019/Debian) (preloaded format=pdflatex)
 restricted \write18 enabled.
entering extended mode
(./main.tex
LaTeX2e <2020-02-02> patch level 2
L3 programming layer <2020-02-14>
[...]
```

To compile our bibliography, we need to parse the `main.bcf` through `biber`. See [here | How to use biber | StackExchange](https://tex.stackexchange.com/questions/26516/how-to-use-biber) for more info.

```shell
(base)  ❮ onyr ★  kenzae❯ ❮ bibliographie_societe_numerique❯❯ biber main
INFO - This is Biber 2.16
INFO - Logfile is 'main.blg'
INFO - Reading 'main.bcf'
INFO - Found 20 citekeys in bib section 0
INFO - Processing section 0
INFO - Looking for bibtex format file 'biblio.bib' for section 0
INFO - LaTeX decoding ...
INFO - Found BibTeX data source 'biblio.bib'
INFO - Overriding locale 'nil' defaults 'variable = shifted' with 'variable = non-ignorable'
INFO - Overriding locale 'nil' defaults 'normalization = NFD' with 'normalization = prenormalized'
INFO - Sorting list 'ynt/global//global/global' of type 'entry' with template 'ynt' and locale 'nil'
INFO - No sort tailoring available for locale 'nil'
INFO - Writing 'main.bbl' with encoding 'UTF-8'
INFO - Output to main.bbl
```

## Errors

#### Package babel Error: Unknown option `french'.

See [StackOverflow](https://tex.stackexchange.com/questions/139700/package-babel-error-unknown-option-francais).

Error with `babel` package for `french`.

```shell
! Package babel Error: Unknown option `french'. Either you misspelled it
(babel)                or the language definition file french.ldf was not found
.
```

`sudo apt-get install texlive-lang-european`: install necessary package for language support. Another method is to install `texlive-lang-french` or even `texlive-lang-all`. Use Synaptics to search and install those packages.
