# Doe's Business Card Template

A [Craftadoc](https://craftadoc.com) template. (Using LaTeX.)

Easily create a beautiful business card by using Doe's Business Card template. The colors can be changed.

### How do I use this?

#### Option 1:

Directly use the template in your browser using Craftadoc [here!](https://app.craftadoc.com/template/overview/64ad3d48ed7e4c2be8ad8bb0) And fill in the template using the automatically generated UI. This is the easiest option.

#### Option 2:

Open the source code in Overleaf: visit [the template page](https://app.craftadoc.com/template/overview/64ad3d48ed7e4c2be8ad8bb0), select the gear icon in the top right and select `Open in Overleaf`.

#### Option 3:

Clone this repository and use your favorite latex compiler locally. (This template uses XeLatex.)

## Example:
![does-business-card-example](./example.png)

## Source:
https://github.com/opieters/business-card

<br/>

---

# ORIGINAL README FOR REFERENCE:

Business Card
=============

Example:

<div>
    <img src="images/front.png" alt-="front side business card" width="200px"/>
    <img src="images/back.png" alt-="back side business card" width="200px"/>
</div>

How this business card was designed, is explained in [this blog post](https://olivierpieters.be/blog/2017/02/11/designing-a-business-card-in-latex).

Requirements
------------

* Recent TeX installation (tested on a 2017 one)
* XeLaTeX
* [Font Awesome](https://github.com/xdanaux/fontawesome-latex)
* [Fira Sans](https://github.com/mozilla/Fira)

It is also possible to use [this Docker container](https://hub.docker.com/r/accupara/business-cards/):

```shell
docker run \
    --rm -it \
    -v `pwd`:/tmp/src accupara/business-cards \
    /bin/bash -c 'cd /tmp/src/src ; xelatex front.tex;'
```

Installing Dependancies on Ubuntu or Debian
-------------------------------------------
``` shell
sudo apt install texlive-latex-recommended texlive-latex-extra texlive-fonts-recommended texlive-fonts-extra
```

Building Documents
------------------

Build the front and back sides with XeLaTeX:

```shell
xelatex src/front.tex
xelatex src/back.tex
```

SVG Files
---------

LaTeX is not equipped to handle SVG files directly. A conversion to a PDF file is needed. This can be done using an external tool such as Inkscape:

```shell
inkscape --without-gui --export-area-drawing --file=logo.svg --export-pdf=logo.pdf
```

License
-------

GNU GPLv3. See LICENSE file.

© 2017 Olivier Pieters
