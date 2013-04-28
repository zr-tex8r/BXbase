BXbase Package Bundle
=====================

LaTeX: Support library for other BX packages

THe main purpose of this bundle is to serve as underlying library
to make work other packages created by the same author (their names
start with “BX” or “PX”).
However bxbase package contains a few user-level commands and is of
some use by itself.

### System Requirements

  - TeX format: LaTeX2e
  - TeX engine: any engine

### Installation

In a system compliant to TDS 1.1, move the files as follows:

  - `*.sty`, `*.def` → $TEXMF/tex/latex/BXbase

And rehash your TEXMF trees if necessary.

bxbase Package ― The base library
----------------------------------

This package is loaded inside other packages written by the same
author. It also contains some user-level commands; see the manual
bxbase-user-en.pdf for detail.

There is also a brief refernce for package-level features, but
unfortulately only in Japanese (bxbase-dev-ja).

Revision History
----------------

  * version 1.0  [2013/04/29]
  * version 0.5  [2010/06/15]
  * version 0.4a [2009/11/16]
  * version 0.4  [2009/07/05]
  * version 0.3  [2008/04/06]
  * version 0.2  [2008/03/28]

----------------------------------------

BXbase パッケージバンドル
=========================

LaTeX: 他の BX パッケージのためのサポートライブラリ

本バンドルの主な目的は、作者（ZR）の制作する他のパッケージ（名前が
“BX”や“PX”で始まる）が依拠するライブラリ機能の提供である。
ただし bxbase パッケージは少数のユーザレベルのコマンドも含むので
単体でも有用である。

### システム要件

  - TeX フォーマット： LaTeX2e
  - TeX エンジン： 不問

### インストール

TDS 1.1 に準拠するシステムの場合、以下のようにファイルを移動する：

  - `*.sty`, `*.def` → $TEXMF/tex/latex/BXbase

この後必要に応じて mktexlsr を実行する。

bxbase パッケージ ― 基礎ライブラリ
----------------------------------

基本的に、他のパッケージの内部で読み込まれるものである。このパッケージ
が提供するユーザ命令にの詳細についてはマニュアル（bxbase-user-ja.pdf）
を参照してほしい。

パッケージレベル（開発者用）機能については bxbase-dev-ja ファイルを
参照してほしい。

更新履歴
--------

  * version 1.0  [2013/04/29]
      - ほぼ全面的な書き直し。
  * version 0.5  [2010/06/15]
      - bxbase: `\JI`/`\KI` を追加。
      - bxbase: `\dvipdfmxmapline`/`\dvipdfmxmapfont` を追加。
      - bxutf8: BMP 外の符号値への対応。
  * version 0.4a [2009/11/16]
      - bxbase で `\UI`/`\Ux` を zxjatype と、`\AJ` を zxotf
        と連携させた。
      - zxbase パッケージを追加。
  * version 0.4  [2009/07/05]
      - PXbase の v0.4 に合わせた改訂。
  * version 0.3  [2008/04/06]
      - bxutf8x を追加。
      - bxutf8 のバグを修正。
      - bxbase でも pxbase の命令 `\recordpapersize` を使用可能にした。
  * version 0.2  [2008/03/28]
      - 最初の公開版。

----------------------------------------
Takayuki YATO (aka. "ZR")  
http://zrbabbler.sp.land.to/
