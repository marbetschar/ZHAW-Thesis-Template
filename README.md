# ZHAW Thesis Template

- [Setup Instructions](#setup-instructions)
- [Usage](#usage)

## Setup Instructions

We assume you have the following software installed on your system:

- [Zettlr](https://docs.zettlr.com/en/install/)
- Pandoc
    - [Core](https://pandoc.org/installing.html)
    - [citeproc](https://github.com/jgm/citeproc)
    - [pandoc-crossref](https://github.com/lierdakil/pandoc-crossref#installation)
- LaTeX
    - Windows: [MikTeX](https://miktex.org/download)
    - macOS: [MacTex](https://www.tug.org/mactex/morepackages.html) (_It suffices to install the Basic Tex, which is much smaller than the full version!_)
    - Linux: [TeX Live](https://www.tug.org/texlive/) (install the `texlive-base` package. You may also need to install the `texlive-xetex`-package)

### Manjaro Linux

The easiest way to install Zettlr is to use [its community package](https://archlinux.org/packages/community/x86_64/zettlr/).

```shell
sudo pamac install zettlr
```

The Zettlr community package already declares pandoc as dependency. However, at the time of this writing (2022-12-03),
the crossref plugin is missing from the dependency list. Therefore we are going to install this additional plugin ourselves:

```shell
sudo pamac install pandoc-crossref
...
Choose optional dependencies for pandoc:
1:  texlive-core: for pdf output

Enter a selection (default=none): 1
...
```

After you installed all the packages, open Zettlr and go to its settings (`Ctrl + ,`). In the export tab deactivate `Use the internal Pandoc for exports`. Make sure to restart Zettlr.

Now you should be able to correctly export usign both, `PDF Document` and `PDF (LaTeX)` with all cross references resolved.

## Usage

