# Latex

### Useful links

[Overleaf](https://www.overleaf.com/)

### Tuto links

[http://math.univ-lyon1.fr/irem/IMG/pdf/LatexPourLeProfDeMaths.pdf](http://math.univ-lyon1.fr/irem/IMG/pdf/LatexPourLeProfDeMaths.pdf) - Full writen tutorial (french)

### Bibliography

[What citation style to use for computer science](https://www.bibguru.com/blog/citation-style-for-computer-science/)

[IEEE citation style](https://paperpile.com/s/proceedings-of-the-ieee-citation-style/)

[bibguru | automatic Bibliography generator (use IEEE)](https://app.bibguru.com/)

### Contacts

Enzo - Serenz#4586 (discord) – Ser Enz (Facebook :
[https://www.facebook.com/enzo.srrtt.69](https://www.facebook.com/enzo.srrtt.69))

Benoit Saunier – Benoit Saunier  (Faceboobs :
https://www.facebook.com/benoit.sau)

## Installing necessary software

### TexLive

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

### VS-Code extension

Use `James-Yu.latex-workshop` extension available [here](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop). Follow the [documentation](https://github.com/James-Yu/LaTeX-Workshop/wiki). This extension enables to compile on save and display the document at the same time as the .tex code.
