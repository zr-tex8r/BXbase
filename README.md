BXbase Package Bundle
=====================

LaTeX: Support library for other BX packages

The main purpose of this bundle is to serve as underlying library
to make work other packages created by the same author (their names
start with “BX” or “PX”).

However bxbase package contains a few user-level commands and is of
some use by itself.

### System Requirements

  * TeX format: LaTeX.
  * TeX engine: Any engine.
  * DVI-ware (in DVI output): Anything.

### Package content

  * `bxbase.sty`: the ‘bxbase’ package
  * `bxbase.def`: a submodule of ‘bxbase’
  * `bxtoolbox.sty`: the ‘bxtoolbox’ package
  * `bxtoolbox.def`: a submodule of ‘bxtoolbox’
  * `bxtoolbox-ext.def`: a submodule of ‘bxtoolbox’
  * `bxtoolbox-ja.def`: a submodule of ‘bxtoolbox’
  * `bxutf8.def`: the ‘bxutf8’ input encoding definition
  * `bxutf8x.def`: the ‘bxutf8x’ input encoding definition
  * `zxbase.sty`: the ‘zxbase’ package
  * `bxbase-ja.pdf`: the user manual for the ‘bxbase’ (in Japanese)
  * `bxbase-ja.tex`: the source file of `bxbase-ja.pdf`

### Installation

In a system compliant to TDS 1.1, move the files as follows:

  - `*.sty`, `*.def` → $TEXMF/tex/latex/BXbase

And rehash your TEXMF trees if necessary.

### License

This package is distributed under the MIT License.

bxbase Package ― The base library
----------------------------------

This package provides many package-level features, which are required by
other packages created by the same author.

It also contains some user-level commands, but most of such commands have
been deprecated since v1.1, except a few which are related to inputting
Japanese text.

Unfortunately the documentation is available only in Japanese. (However,
those unfamiliar with the Japanese language will probably have no need to
load this package directly.)

bxtoolbox Package ― To emulate etoolbox on non-e-TeX
-----------------------------------------------------

The main goal of this package is to provide part of the functions of the
[etoolbox] package for TeX engines without e-TeX extension. (Note that
TeX users in Japan have long used the pTeX engine for writing Japanese,
and e-TeX extention for that engine did not appear until around 2010.)

[etoolbox]: https://www.ctan.org/pkg/etoolbox

Note that when this package is loaded in e-TeX engines, then it loads
the real etoolbox and uses the functions of that package.

### e-TeX functions provided by this package

Below is the list:

    \AfterPreamble \AtEndPreamble \AfterEndPreamble
    \AfterEndDocument
    \csdef \csgdef \csedef \csxdef
    \cslet \letcs \csletcs \undef \csundef
    \appto \gappto \eappto \xappto
    \csappto \csgappto \cseappto \csxappto
    \preto \gpreto \epreto \xpreto
    \cspreto \csgpreto \csepreto \csxpreto
    \newbool \providebool \booltrue \boolfalse
    \setbool \ifbool \notbool
    \newtoggle \providetoggle \toggletrue \togglefalse
    \settoggle \iftoggle \nottoggle
    \ifdef \ifundef
    \ifstrequal \ifstrempty

### “Fakes” provided by this package

These commands have a name of the original command prefixed by “bx”,
that is, `\bxZzz` instead of `\zzz`. Some come in two versions: `\bxZzz`
works as `\zzz` but is lack of expandability `\zzz` has, whereas `\bxZzzX`
is expandable as `\zzz` is but otherwise flawed.

  * `\bxNewrobustcmd`: Uses LaTeX-protect instead of `\protected`.
  * `\bxRenewrobustcmd`: Ditto.
  * `\bxProviderobustcmd`: Ditto.
  * `\bxRobustify`: Ditto.
  * `\bxCsuse`: Forbidden in moving arguments.
  * `\bxCsuseX`: Suffering from `\relax`’ifying.
  * `\bxCsshow`: Forbidden in moving arguments.
  * `\bxIfcsdef`: Forbidden in moving arguments.
  * `\bxIfcsundef`: Forbidden in moving arguments.
  * `\bxIfcsundefX`: Suffering from `\relax`’ifying.

Note: On e-TeX extended engines, these commands are simply aliases to the
real commands of etoolbox.

zxbase Package ― The base library for XeTeX
--------------------------------------------

This package provides XeTeX-specific features, which are required by
other packages created by the same author.

For the present this package contains no public features.

Revision History
----------------

  * Version 1.2a 〈2023/02/23〉
  * Version 1.2  〈2020/10/04〉
      - Support LaTeX kernel 2020/10/01.
  * Version 1.1  〈2017/05/29〉
  * Version 1.0  〈2013/04/29〉
  * Version 0.5  〈2010/06/15〉
  * Version 0.4a 〈2009/11/16〉
  * Version 0.4  〈2009/07/05〉
  * Version 0.3  〈2008/04/06〉
  * Version 0.2  〈2008/03/28〉

--------------------
Takayuki YATO (aka. "ZR")  
https://github.com/zr-tex8r
