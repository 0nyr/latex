# Latex

### Useful links

[Overleaf](https://www.overleaf.com/)

[Overleaf Latex doc](https://www.overleaf.com/learn)

##### tools

[bibliography manager | bibguru](https://github.com/0nyr/compare-consensus-protocols) ⭐️

##### tutos

[LaTex généralités](https://fr.wikibooks.org/wiki/LaTeX/G%C3%A9n%C3%A9ralit%C3%A9s)

[LaTex tutorial](https://latex-tutorial.com/tutorials/)

[learn LaTeX in 30min | Overleaf](https://www.overleaf.com/learn/latex/Learn_LaTeX_in_30_minutes)

[LaTeX pour prof de maths](http://math.univ-lyon1.fr/irem/IMG/pdf/LatexPourLeProfDeMaths.pdf)

##### doc

[LaTex doc | Overleaf](https://www.overleaf.com/learn/latex/Main_Page)

[TeX live doc](https://www.tug.org/texlive/)

##### vscode - LaTeX Workshop

[LaTeX Workshop wiki | GitHub](https://github.com/James-Yu/LaTeX-Workshop/wiki)

[LaTeX + VSCode](https://maumneto.medium.com/git-vs-code-overleaf-91ecfd586b36)

[installation &amp; prerequisites](https://github.com/James-Yu/LaTeX-Workshop/wiki/Install#settings)

[compiling &amp; multi-file projects](https://github.com/James-Yu/LaTeX-Workshop/wiki/Compile#cleaning-generated-files)

##### latex formatting

[code listing &amp; formatting | Overleaf](https://www.overleaf.com/learn/latex/Code_listing)

[formatting code in latex](https://denbeke.be/blog/programming/syntax-highlighting-in-latex/)

[formatting code | Wiki](https://en.wikibooks.org/wiki/LaTeX/Source_Code_Listings)

##### Tuto links

[Latex pour le prof](http://math.univ-lyon1.fr/irem/IMG/pdf/LatexPourLeProfDeMaths.pdf) - Full writen tutorial (french)

## Contacts

Enzo - Serenz#4586 (discord) – Ser Enz (Facebook :
[https://www.facebook.com/enzo.srrtt.69](https://www.facebook.com/enzo.srrtt.69))

Benoit Saunier – Benoit Saunier  (Faceboobs :
https://www.facebook.com/benoit.sau)

## commands

`latexmk` : Automatic LaTeX document generation routine

`pdflatex` : convert `.tex` documents to `.pdf`.

`tlmgr` : tlmgr manages an existing TeX Live installation, both packages and
configuration options.

## Installing necessary software

### TexLive

##### official installation process

Follow the instructions of the [Installation guide | official](https://www.tug.org/texlive/acquire-netinstall.html). Get the tar.gz file, extract it, then run the provided install script by running `sudo perl install-tl`. This will launch the default cli installer but the is also a graphical one.

The installation then takes some time. Just wait.

```shell
(base)  ❮ onyr ★  kenzae❯ ❮ install-tl-20220110❯❯ sudo perl install-tl 
======================> TeX Live installation procedure <=====================

======>   Letters/digits in <angle brackets> indicate   <=======
======>   menu items for actions or customizations      <=======
= help>   https://tug.org/texlive/doc/install-tl.html   <=======

 Detected platform: GNU/Linux on x86_64
 
 <B> set binary platforms: 1 out of 16

 <S> set installation scheme: scheme-full

 <C> set installation collections:
     40 collections out of 41, disk space required: 7223 MB

 <D> set directories:
   TEXDIR (the main TeX directory):
     /usr/local/texlive/2021
   TEXMFLOCAL (directory for site-wide local files):
     /usr/local/texlive/texmf-local
   TEXMFSYSVAR (directory for variable and automatically generated data):
     /usr/local/texlive/2021/texmf-var
   TEXMFSYSCONFIG (directory for local config):
     /usr/local/texlive/2021/texmf-config
   TEXMFVAR (personal directory for variable and automatically generated data):
     ~/.texlive2021/texmf-var
   TEXMFCONFIG (personal directory for local config):
     ~/.texlive2021/texmf-config
   TEXMFHOME (directory for user-specific files):
     ~/texmf

 <O> options:
   [ ] use letter size instead of A4 by default
   [X] allow execution of restricted list of programs via \write18
   [X] create all format files
   [X] install macro/font doc tree
   [X] install macro/font source tree
   [ ] create symlinks to standard directories

 <V> set up for portable installation

Actions:
 <I> start installation to hard disk
 <P> save installation profile to 'texlive.profile' and exit
 <Q> quit

Enter command: I
Installing to: /usr/local/texlive/2021
Installing [0001/4307, time/total: ??:??/??:??]: texlive.infra [430k]
Installing [0002/4307, time/total: 00:00/00:00]: texlive.infra.x86_64-linux [143k]
Installing [0003/4307, time/total: 00:00/00:00]: 12many [376k]
Installing [0004/4307, time/total: 00:00/00:00]: 2up [56k]
Installing [0005/4307, time/total: 00:01/01:00:40]: a0poster [119k]
Installing [0006/4307, time/total: 00:01/54:14]: a2ping [69k]
[...]

Welcome to TeX Live!


See /usr/local/texlive/2021/index.html for links to documentation.
The TeX Live web site (https://tug.org/texlive/) contains any updates and corrections. TeX Live is a joint project of the TeX user groups around the world; please consider supporting it by joining the group best for you. The list of groups is available on the web at https://tug.org/usergroups.html.


Add /usr/local/texlive/2021/texmf-dist/doc/man to MANPATH.
Add /usr/local/texlive/2021/texmf-dist/doc/info to INFOPATH.
Most importantly, add /usr/local/texlive/2021/bin/x86_64-linux
to your PATH for current and future sessions.
Logfile: /usr/local/texlive/2021/install-tl.log
```

Then, add necessary paths as environment variables in `.bashrc`:

```plaintext
# LaTex
export PATH="$PATH:/usr/local/texlive/2021/bin/x86_64-linux"
export MANPATH="$MANPATH:/usr/local/texlive/2021/texmf-dist/doc/man"
export INFOPATH="$INFOPATH:/usr/local/texlive/2021/texmf-dist/doc/info"
```

And check everything is good:

```shell
(base)  ❮ onyr ★  kenzae❯ ❮ install-tl-20220110❯❯ echo $INFOPATH

(base)  ❮ onyr ★  kenzae❯ ❮ install-tl-20220110❯❯ source ~/.bashrc 

               ██████╗ ███╗   ██╗██╗   ██╗██████╗   
              ██╔═══██╗████╗  ██║╚██╗ ██╔╝██╔══██╗  
    █████╗    ██║   ██║██╔██╗ ██║ ╚████╔╝ ██████╔╝    █████╗
    ╚════╝    ██║   ██║██║╚██╗██║  ╚██╔╝  ██╔══██╗    ╚════╝
              ╚██████╔╝██║ ╚████║   ██║   ██║  ██║  
               ╚═════╝ ╚═╝  ╚═══╝   ╚═╝   ╚═╝  ╚═╝  
                                    
 to loom up  =  surgir, apparaître (négatif) [375] 

(base)  ❮ onyr ★  kenzae❯ ❮ install-tl-20220110❯❯ echo $INFOPATH
:/usr/local/texlive/2021/texmf-dist/doc/info
```

##### ubuntu quick install

`sudo apt install texlive-full` : install `texlive`, the official linux TeX package.

```shell
(base) onyr@aezyr:~/Documents/code/latex/example/Sartre_H3_200327_Boutron_Bouvier_Monnier_Saunier$ sudo apt update
(base) onyr@aezyr:~/Documents/code/latex/example/Sartre_H3_200327_Boutron_Bouvier_Monnier_Saunier$ sudo apt update
[...]
(base) onyr@aezyr:~/Documents/code/latex/example/Sartre_H3_200327_Boutron_Bouvier_Monnier_Saunier$ sudo apt install texlive-full
Reading package lists... Done
Building dependency tree   
Reading state information... Done
The following packages were automatically installed and are no longer required:
  libfprint-2-tod1 libllvm10
Use 'sudo apt autoremove' to remove them.
The following additional packages will be installed:
  aglfn asymptote asymptote-doc biber chktex cm-super cm-super-minimal context context-modules dvidvi dvipng dvisvgm feynmf
  fonts-adf-accanthis fonts-adf-berenis fonts-adf-gillius fonts-adf-universalis fonts-arphic-bkai00mp fonts-arphic-bsmi00lp
  fonts-arphic-gbsn00lp fonts-arphic-gkai00mp fonts-baekmuk fonts-cabin fonts-cantarell fonts-comfortaa fonts-croscore
  fonts-crosextra-caladea fonts-crosextra-carlito fonts-ebgaramond fonts-ebgaramond-extra fonts-font-awesome fonts-freefont-otf
  fonts-gfs-artemisia fonts-gfs-baskerville fonts-gfs-bodoni-classic fonts-gfs-complutum fonts-gfs-didot fonts-gfs-didot-classic
  fonts-gfs-gazis fonts-gfs-neohellenic fonts-gfs-olga fonts-gfs-porson fonts-gfs-solomos fonts-gfs-theokritos fonts-go
  fonts-hosny-amiri fonts-ipaexfont-gothic fonts-ipaexfont-mincho fonts-ipafont-gothic fonts-ipafont-mincho fonts-junicode fonts-lato
  fonts-linuxlibertine fonts-lmodern fonts-lobster fonts-lobstertwo fonts-noto-core fonts-oflb-asana-math fonts-open-sans
  fonts-sil-gentium fonts-sil-gentium-basic fonts-sil-gentiumplus fonts-sil-gentiumplus-compact fonts-stix fonts-texgyre
  fonts-tlwg-garuda-otf fonts-tlwg-kinnari-otf fonts-tlwg-laksaman-otf fonts-tlwg-loma-otf fonts-tlwg-mono-otf fonts-tlwg-norasi-otf
  fonts-tlwg-purisa-otf fonts-tlwg-sawasdee-otf fonts-tlwg-typewriter-otf fonts-tlwg-typist-otf fonts-tlwg-typo-otf
  fonts-tlwg-umpush-otf fonts-tlwg-waree-otf fonts-unfonts-core fonts-unfonts-extra fragmaster freeglut3 gsfonts imagemagick
  imagemagick-6-common imagemagick-6.q16 javascript-common lacheck latex-cjk-all latex-cjk-chinese latex-cjk-chinese-arphic-bkai00mp
  latex-cjk-chinese-arphic-bsmi00lp latex-cjk-chinese-arphic-gbsn00lp latex-cjk-chinese-arphic-gkai00mp latex-cjk-common
  latex-cjk-japanese latex-cjk-japanese-wadalab latex-cjk-korean latex-cjk-thai latexdiff latexmk lcdf-typetools libalgorithm-c3-perl
  libapache-pom-java libautovivification-perl libb-hooks-endofscope-perl libb-hooks-op-check-perl libbtparse2
  libbusiness-isbn-data-perl libbusiness-isbn-perl libbusiness-ismn-perl libbusiness-issn-perl libclass-accessor-perl libclass-c3-perl
  libclass-c3-xs-perl libclass-data-inheritable-perl libclass-inspector-perl libclass-method-modifiers-perl libclass-singleton-perl
  libclass-xsaccessor-perl libclone-perl libcommons-logging-java libcommons-parent-java libdata-compare-perl libdata-optlist-perl
  libdata-uniqid-perl libdate-simple-perl libdatetime-calendar-julian-perl libdatetime-format-builder-perl
  libdatetime-format-strptime-perl libdatetime-locale-perl libdatetime-perl libdatetime-timezone-perl libdevel-callchecker-perl
  libdevel-caller-perl libdevel-globaldestruction-perl libdevel-lexalias-perl libdevel-stacktrace-perl libdist-checkconflicts-perl
  libdynaloader-functions-perl libemail-date-format-perl libemf1 libencode-eucjpms-perl libencode-hanextra-perl libencode-jis2k-perl
  libencode-perl libeval-closure-perl libexception-class-perl libexporter-tiny-perl libfile-find-rule-perl libfile-homedir-perl
  libfile-sharedir-perl libfile-slurper-perl libfile-which-perl libfontbox-java libglew2.1 libgsl23 libgslcblas0 libipc-run3-perl
  libipc-shareable-perl libjs-jquery liblingua-translit-perl liblist-allutils-perl liblist-moreutils-perl liblist-someutils-perl
  liblist-someutils-xs-perl liblist-utilsby-perl liblog-dispatch-perl liblog-log4perl-perl liblqr-1-0 libmagick++-6.q16-8
  libmagickcore-6.q16-6 libmagickcore-6.q16-6-extra libmagickwand-6.q16-6 libmail-sendmail-perl libmime-charset-perl libmime-lite-perl
  libmime-types-perl libmodule-implementation-perl libmodule-runtime-perl libmro-compat-perl libnamespace-autoclean-perl
  libnamespace-clean-perl libnetpbm10 libnumber-compare-perl libosp5 libostyle1c2 libpackage-stash-perl libpackage-stash-xs-perl
  libpadwalker-perl libparams-classify-perl libparams-util-perl libparams-validate-perl libparams-validationcompiler-perl
  libparse-recdescent-perl libpdfbox-java libperlio-utf8-strict-perl libplot2c2 libpoppler-qt5-1 libpstoedit0c2a libptexenc1
  libreadonly-perl libref-util-perl libref-util-xs-perl libregexp-common-perl librole-tiny-perl libruby2.7 libsigsegv2 libsombok3
  libsort-key-perl libspecio-perl libsub-exporter-perl libsub-exporter-progressive-perl libsub-identify-perl libsub-install-perl
  libsub-name-perl libsub-quote-perl libsys-hostname-long-perl libtcl8.6 libteckit0 libtexlua53 libtexluajit2 libtext-bibtex-perl
  libtext-csv-perl libtext-csv-xs-perl libtext-glob-perl libtext-roman-perl libtext-unidecode-perl libtie-cycle-perl libtk8.6
  libunicode-linebreak-perl libutempter0 libvariable-magic-perl libxml-libxml-perl libxml-libxml-simple-perl libxml-libxslt-perl
  libxml-namespacesupport-perl libxml-sax-base-perl libxml-sax-expat-perl libxml-sax-perl libxml-writer-perl libxstring-perl
  libyaml-tiny-perl libzip5 libzzip-0-13 lmodern netpbm openjade pfb2t1c2pfb prerex preview-latex-style ps2eps pstoedit psutils
  purifyeps rake ruby ruby-minitest ruby-net-telnet ruby-power-assert ruby-test-unit ruby-xmlrpc ruby2.7 rubygems-integration t1utils
  tcl tcl8.6 teckit tex-common tex-gyre texinfo texlive-base texlive-bibtex-extra texlive-binaries texlive-extra-utils
  texlive-font-utils texlive-fonts-extra texlive-fonts-extra-doc texlive-fonts-extra-links texlive-fonts-recommended
  texlive-fonts-recommended-doc texlive-formats-extra texlive-games texlive-humanities texlive-humanities-doc texlive-lang-arabic
  texlive-lang-chinese texlive-lang-cjk texlive-lang-cyrillic texlive-lang-czechslovak texlive-lang-english texlive-lang-european
  texlive-lang-french texlive-lang-german texlive-lang-greek texlive-lang-italian texlive-lang-japanese texlive-lang-korean
  texlive-lang-other texlive-lang-polish texlive-lang-portuguese texlive-lang-spanish texlive-latex-base texlive-latex-base-doc
  texlive-latex-extra texlive-latex-extra-doc texlive-latex-recommended texlive-latex-recommended-doc texlive-luatex texlive-metapost
  texlive-metapost-doc texlive-music texlive-pictures texlive-pictures-doc texlive-plain-generic texlive-pstricks texlive-pstricks-doc
  texlive-publishers texlive-publishers-doc texlive-science texlive-science-doc texlive-xetex tipa tk tk8.6 vprerex xterm
Suggested packages:
  asymptote-x11 perl-tk fontforge context-nonfree imagemagick-doc autotrace enscript ffmpeg gimp gnuplot grads hp2xx html2ps libwmf-bin
  mplayer povray radiance transfig ufraw-batch apache2 | lighttpd | httpd auctex hbf-cns40-b5 hbf-jfs56 hbf-kanji48 libgd-barcode-perl
  libavalon-framework-java libcommons-logging-java-doc libexcalibur-logkit-java liblog4j1.2-java libscalar-properties-perl glew-utils
  gsl-ref-psdoc | gsl-doc-pdf | gsl-doc-info | gsl-ref-html libdbd-csv-perl liblog-dispatch-filerotate-perl librrds-perl
  libxml-dom-perl inkscape libjxr-tools libpod2-base-perl default-mta | mail-transport-agent libmojolicious-perl libscalar-number-perl
  libtest-fatal-perl libxml-sax-expatxs-perl doc-base xfig | ivtools-bin | tgif | transfig ri ruby-dev bundler tcl-tclreadline
  debhelper xzdec xindy python3-pygments icc-profiles libspreadsheet-parseexcel-perl dot2tex ruby-tcltk | libtcltk-ruby
  default-jre-headless xfonts-cyrillic
Recommended packages:
  fonts-freefont
[...]
```

## VS-Code extension - Latex Workshop

Use `James-Yu.latex-workshop` extension available [here](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop). Follow the [documentation](https://github.com/James-Yu/LaTeX-Workshop/wiki). This extension enables to compile on save and display the document at the same time as the .tex code.

> To edit extension settings, go in the extension section, select `LaTeX Workshop`. Then on the extension page, click on the gear icon ⚙️ and click on Extension settings.

### Installation

> Use `LaTeX Workshop` extension.

[Installation and prerequisites](https://github.com/James-Yu/LaTeX-Workshop/wiki/Install)

### settings

The compilation process of LaTeX creates a lot of useless files. Hence I prefer to remove them automatically.

### commands

`latex-workshop.latex.autoClean.run` : set to `onBuild`.

`Ctrl + Shift + P` : launch command prompt for VSCode

`Ctrl + Alt + B` : Build LaTeX project

`Ctrl + alt + C` : Clean up auxiliary files
