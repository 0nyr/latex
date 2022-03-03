### Glossary and Acronyms

### Useful links

##### guides

[how to make Glossaries/Acronyms in LaTeX](https://www.resurchify.com/latex_tutorial/latex_glossaries.php)

[Glossaries / Acronyms | Overleaf](https://www.overleaf.com/learn/latex/Glossaries)




## Problems

### List of glossaries not displaying

First, don't forget to add the elements to the glossaries, with the `\glsaddall` flag. WARN: this is useless while using the build command `makeglossaries main` to build glossary and acronyms.

[StackOverflow](https://tex.stackexchange.com/questions/192378/list-of-glossaries-not-displaying)

The problem here is probably that the `.ist`, `.gls` and `.glo` are missing/not linked correctly.

To correct that, run the following commands:

`pdflatex main.tex`

`makeindex -s main.ist -o main.gls main.glo`

(use `makeglossaries main` instead, works with both acronyms and glossary)

`pdflatex main.tex`
