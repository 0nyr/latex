# Babel and Texlive

### Useful links

##### installation

[search and install language specific package | StackExchange](https://tex.stackexchange.com/questions/73526/how-to-install-a-language-package-in-texmaker-on-ubuntu-12-04)


## Installing packages

To support different languages and fonts, one need to install the required packages.

`sudo apt-cache search texlive french`: search package with texlive and french in their name. This is used to search for the French language package.

`sudo apt-get install texlive-lang-french`: This is used to install the French language specific package.

`sudo apt-get install texlive-lang-greek`: This is used to install the Greek language specific package.

```shell
$ sudo apt-cache search texlive french
 texlive-doc-fr - TeX Live: French documentation
 texlive-lang-french - TeX Live: French

$sudo apt-get install texlive-lang-french
```

## Writing in greek

[Excellent ressource here](https://www.tuteurs.ens.fr/logiciels/latex/grec.html)
