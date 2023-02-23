BXbase パッケージバンドル
=========================

LaTeX： 他の BX パッケージのためのサポートライブラリ

本バンドルの主な目的は、作者（ZR）の制作する他のパッケージ（名前が
“BX”や“PX”で始まる）が依拠するライブラリ機能の提供である。

ただし bxbase パッケージは少数のユーザレベルのコマンドも含むので
単体でも有用である。

### 前提環境

  * TeX フォーマット： LaTeX
  * TeX エンジン： 不問
  * DVI ウェア（DVI 出力時）： 不問

### 構成物

  * `bxbase.sty`： ‘bxbase’パッケージ
  * `bxbase.def`： ‘bxbase’のサブモジュール
  * `bxtoolbox.sty`： ‘bxtoolbox’パッケージ
  * `bxtoolbox.def`： ‘bxtoolbox’のサブモジュール
  * `bxtoolbox-ext.def`： ‘bxtoolbox’のサブモジュール
  * `bxtoolbox-ja.def`： ‘bxtoolbox’のサブモジュール
  * `bxutf8.def`： ‘bxutf8’入力エンコーディング定義
  * `bxutf8x.def`：‘bxutf8x’入力エンコーディング定義
  * `zxbase.sty`： ‘zxbase’パッケージ
  * `bxbase-ja.pdf`： ‘bxbase’のユーザ向け説明書（日本語）
  * `bxbase-ja.tex`： `bxbase-ja.pdf` のソースファイル

### インストール

TDS 1.1 に準拠するシステムの場合、以下のようにファイルを移動する：

  - `*.sty`, `*.def` → $TEXMF/tex/latex/BXbase

この後必要に応じて mktexlsr を実行する。

### ライセンス

本パッケージは MIT ライセンスの下で配布される。

bxbase パッケージ ― 基礎ライブラリ
----------------------------------

基本的に、他のパッケージの内部で読み込まれるものであり、作者（ZR）の制作
する他のパッケージで必要な機能を提供する。

本パッケージは幾つかのユーザ命令も提供していたが、その大部分が 1.1 版に
おいて非推奨となった。日本語入力に関する少数の機能が残されている。

### ユーザ向け機能

ユーザ向け機能についてはマニュアル `bxbase-ja.pdf` を参照されたい。

### 開発者向け機能

ここでは bxbase パッケージが提供する開発者向け機能について簡単に解説する。

※ bxbase パッケージは内部で bxtoolbox パッケージを読み込むため、bxtoolbox
の機能も利用できる。

#### 書式記述に関する注意

`<LaTeXマクロ定義記述>` は `\newcommand` 等の LaTeX マクロ定義命令に
後続する要素列で、以下のものに等しい。

    {<命令>}[<引数個数>][<引数既定値>]{<置換テキスト>}

`<TeXマクロ定義記述>` は `\def` 等の TeX マクロ定義プリミティブに
後続する要素列で、以下のものに等しい。

    <命令><引数宣言部>{<置換テキスト>}

`<TeXマクロ定義記述*>` は `<TeXマクロ定義記述>` の先頭の `<命令>`
を除去したもの。

#### プログラミング補助

  * `\bxDebug{<テキスト>}`  
    デバック出力用命令。このパッケージでの定義では何もしない。
  * `\bxRequireDefinition{<ファイルベース名>}`  
    拡張子 .def のファイルを `\usepackage` と同じ方式で読み込む。  
  * `\bxNullify\制御綴`  
    `\制御綴` を「何もしない命令」で `\providecommand` により
    上書きされないものに再定義する。
  * `\bxForEachIn<引数1>,<引数2>,...\do{<置換テキスト>}`  
    各々の引数について、`<置換テキスト>` の `#1` をそれで置き換えた
    ものを実行する。LaTeX の `\@for` のラッパーで、`\@for` と同じく、
    `\bxForEachIn` の直後のトークンは予め一度展開される。
  * `\bxForEachTokenIn<トークン1><トークン2>...\do{<置換テキスト>}`  
    各々の引数について `<置換テキスト>` の `#1` を置き換えたものを
    実行する。LaTeX の `\@tfor` のラッパー。
  * `\bxWithArgExpd{<引数1>}\do{<置換テキスト>}`  
  * `\bxWithArgsExpd{<引数1>}{<引数2>}...\do{<置換テキスト>}`  
    `<置換テキスト>` 中の `#1`、`#2`… を各々の引数を一回展開した
    ものに置き換えたものを実行する。`\bxWithArgExpd` は 1 引数用に
    最適化したもの。
  * `\bxWithArgFullExpd{<引数1>}\do{<置換テキスト>}`  
  * `\bxWithArgsFullExpd{<引数1>}{<引数2>}...\do{<置換テキスト>}`  
    `\bxWithArgsExpd` と同様だが、一回展開でなく完全展開する点が
    異なる。
  * `\bxChompComma<命令>`  
    `<命令>` の 置換テキストの先頭が `,` の場合、それを削除したもので
    再定義する。
  * `\bxAssign<代入文>\relax`  
    代入を行った後、代入文の後ろにゴミがないかを判定しその結果を
    スイッチ `\ifbxOk` に返す。
  * `\bxCheckMA<テキスト>\bxEndCheckMA`  
    `\edef` 中ではこの部分がエラーを出す命令に展開される。

#### TeX エンジン判別

  * `\bxEngineTypeX`  [整数定数]  
    1=pTeX拡張; 2=XeTeX拡張; 3=Omega拡張; 0=以上に該当せず
  * `\bxEngineTypeY`  [整数定数]  
    1=eTeX拡張; 3=pdfTeX拡張; 5=LuaTeX拡張; 0=以上に該当せず  
    ※現在の LuaTeX は X/Y=0/5 となる。
    ※upTeX か否かの判定は ifptex パッケージを用いる。

#### Babel 関係

  * `\bxAtBeginDocumentBabel{<テキスト>}`  
    Babel 読込時にのみ実行される begin-document 時のフック。
  * `\bxTrivLangDef{<言語名>}`  
    中身（キャプション定義等）が空の Babel 言語オプションを生成する。

#### 数値の書式化出力

  * `\bxToHexTwo{<整数>}`      [%02X 形式; 0x00～FF]  
  * `\bxToHexThree{<整数>}`    [%03X 形式; 0x000～FFF]  
  * `\bxToHexFour{<整数>}`     [%04X 形式; 0x0000～FFFF]  
  * `\bxToHexFive{<整数>}`     [%05X 形式; 0x00000～FFFFF]  
  * `\bxToHexFiveX{<整数>}`    [%05X 形式; 0x00000～FFFFF ※1]  
  * `\bxToHexEight{<整数>}`    [%08X 形式; 0x00000000～7FFFFFFF]  
  * `\bxToHexTiny{<整数>}`     [%X 形式; 0x0～FF]  
  * `\bxToHexSmall{<整数>}`    [%X 形式; 0x0～7FFF]  
  * `\bxToHexUC{<整数>}`       [%04X 形式; 0x0000～10FFFF ※2]  
    16 進表記を `\bxHex` に返す。UC は 4～6 桁での表記。  
    ※1 0xFFFFF を超える場合は `FFFFF` になる  
    ※2 XeTeX/LuaTeX/upTeX の場合、`\char` が可能な範囲。
  * `\bxToDecFour{<整数>}`     [%04d 形式; 0000～9999]  
  * `\bxToDecFive{<整数>}`     [%05d 形式; 00000～99999]  
    ゼロ付の 10 進表記を `\bxHex` に返す。

#### 符号値による入力

  * `\bxCodeValueSeq\制御綴{<符号値>,...}    [16進]`  
  * `\bxCodeValueSeqD\制御綴{<符号値>,...}   [10進]`  
    各々の `<符号値>` を解釈した結果を `\bxUcv` に代入してマクロ
    `\制御綴` を呼び出す。解釈方法はそれぞれ `\Ux` と `\AJ` 命令の
    解説にある通り。
  * `\bxUHex{<コード値16進表記>}`  
    bxutf8 が構成する内部表現。用いる機能は `\Ux` と同じ。
  * `\bxUInt{<整数>}`  
    bxutf8x が構成する内部表現。用いる機能は `\Ux` と同じ。

#### 文字列操作

  * `\bxToLower{<文字列>}  [小文字]`  
  * `\bxToUpper{<文字列>}  [大文字]`  
    `<文字列>` を小文字／大文字に変換したものを `\bxRes` に返す。

#### Special 出力

  * `\bxDocumentSpecial{<テキスト>}`  
    `\AtBeginDvi` を普通に用いて DVI の先頭部に special を出力する。

#### Safe caret 機能

  * `\bxBDHookSafeCaret`  
    safe caret 機能に関する begin-document フック。
  * `\bxEnableSafeCaret`  
    safe caret 機能を使用可能にしておく。すなわち、プレアンブルでこの
    命令が呼ばれなかった場合、safe caret は使用不可になる。実際にある
    状況で safe caret を有効にするには、`\bx@acr@normcaret` を「その
    状況での本来の `^` の動作」に定義した上で `^` をアクティブにする
    必要がある。  
    ※ ユーザ命令の `\safecaret` はこの命令を実行した上で、verbatim
    と babel での適切な safe caret 処理を有効化している。

#### Shadow map 機能

Shadow map とは「16 ビット整数 → 整数」の写像を TFM として表現
したもの。

  * `\bxUseShadowMap\制御綴{<TFM名>}`  
    `\制御綴` を指定の TFM から生成される shadow map として定義。
  * `\bxMap\制御綴`  
    整数レジスタ `\bxUcv` の現在の値に shadow map を適用し、その結果を
    `\bxUcv` に代入する。

#### モジュール名

ここでいう「モジュール」とは文書クラス（.cls）・パッケージ（.sty）・
定義ファイル（.def）の総称。「モジュール読込中に発生するエラーを出力
するためのマクロ」を別のモジュール内で定義する際に、呼び出した側の
モジュール名をメッセージ中に出力させるための仕組み。

  * `\bxSetModuleName{<文字列>}`  
    現在のモジュールに対するモジュール名を設定する。
  * `\bxModuleName`  
    現在のモジュールに対するモジュール名に展開される。モジュール名が
    設定されていない場合はファイルのベース名を代わりに使う。
  * `\bxError`            [`\PackageError` に対応]  
  * `\bxWarning`          [`\PackageWarning` に対応]  
  * `\bxWarningNoLine`    [`\PackageWarningNoLine` に対応]  
  * `\bxInfo`             [`\PackageInfo` に対応]  
    現在のモジュール名をパッケージ名として `\PackageError` 等を呼ぶ。

#### keyval の拡張

（xkeyval が普及した今では非推奨かも…）

keyval の `\setkeys` について、「未定義のキーをエラーにせず、代わりに
未定義のキーのリストを作成する」という変種を提供する。この機能は
xkeyval で `\setkeys*` として提供されている。しかし xkeyval が利用
できない環境に対応するために keyval へのパッチとして実現すること
にする。しかし、xkeyval はこのパッチを無効化してしまう。従って
xkeyval.sty が存在するかに応じて処理を分けることにした。

  * `\bxPrepareSetKeysSafe`  
    `\bxSetKeysSafe` を使用可能にする。  
    ※ xkeyval.sty が存在するかを判定し、存在すれば読み込む。
    そして `\bxSetKeysSafe` の実現方法をこの段階で確定させる。
  * `\bxSetKeysSafe{<ファミリ>}{<テキスト>}`  
    `\setkeys` と同様だが、未定義のキーをエラーとせず、代わりに
    未定義のキーからなるコンマ区切りのリストを `\bxRestKeys` に
    代入する。

#### ドライバ判別

以下の説明で「先天的な」ドライバとは、TeX 実行時に使用が判定できる
もの（事実上「TeX エンジンがドライバを兼ねるもの」に等しい）を指し、
例えば pdfTeX、XeTeX、LuaTeX が該当する。

  * `\bxDriverList`  
    （後天的な）ドライバ名のリスト。  
    ※ 現状では「`dvips,dvipdfmx,dviout`」。
  * `\bxDriverInherent`  
    先天的なドライバ名（未定義なら空）に展開される。
  * `\bxSetDriver[<ファイル名>]{<ドライバ名>}`  
    指定のファイル名をもつモジュールに対するドライバ名を指定する。
    `<ファイル名>` がない場合は現在のモジュールに対する設定。
  * `\bxDriver`  
    現在のモジュールに対するドライバ名に展開される。未定義ならば
    `default` を返す。
  * `\bxDriverSpecifiedFor{<ファイル名>}`  
    `\bxDriver` と同様だが、指定のファイル名をもつモジュールに
    対する設定を返す。
  * `\bxDefineDDProcess{<名前>}{<ドライバ名>}<TeXマクロ定義記述*>`  
    ドライバ依存マクロを定義する。
  * `\bxDefineDDProcessDefault{<名前>}`  
    `<ドライバ名>` が `default` の `\bxDefineDDProcess`。
  * `\bxDoDDProcess{<名前>}`  
    ドライバ依存マクロを実行する。
  * `\bxDeclareDriverOptions`  
    後天的なドライバ名の各々について、「`\bxSetDriver{ドライバ名}`
    を呼ぶ」という動作のパッケージ（クラス）オプションを定義する。

bxtoolbox パッケージ ― 非 e-TeX エンジンでの etoolbox の模倣
-------------------------------------------------------------

本パッケージの主な目的は、etoolbox パッケージの一部の機能を e-TeX 拡張を
持たないエンジンで利用可能にすることである。（pTeX エンジンの e-TeX 拡張
が普及し出したのは 2010 年頃である。）

なお、本パッケージを e-TeX 拡張をもつエンジンで読み込んだ場合は、本物の
etoolbox が読み込まれてその機能が使われる。

### etoolbox 互換命令

ここに挙げる命令は、etoolbox の命令の複製であり、それぞれ、命令名の頭の
`bx` を取って先頭を小文字に変えた名前（`\bxCsdef`→`\csdef`）の etoolbox
の命令に対応する。e-TeX 拡張のエンジンで動作する場合は実際に etoolbox を
読み込んでそれの命令のエイリアスとするが、そうでない場合は自前の実装を
用いる。

各命令の詳細については etoolbox のマニュアルを参照されたい。etoolbox の
元の命令と仕様が異なる部分にのみ説明を付している（この説明は e-TeX 非拡張
のエンジンでの動作時のみ当てはまることに注意）。

(頑強な命令の定義)

  * `\bxNewrobustcmd[*]<LaTeXマクロ定義記述>`  
  * `\bxRenewrobustcmd[*]<LaTeXマクロ定義記述>`  
  * `\bxProviderobustcommand[*]<LaTeXマクロ定義記述>`  
  * `\bxRobustify{<命令>}`  
    e-TeX の \protected の代わりに LaTeX の protect 処理を用いる。結果
    的に \DeclareRobustCommand と同じ処理が使われる。

(メイン文書コンパイル時フック)

  * `\AfterPreamble{<テキスト>}`  
  * `\AtEndPreamble{<テキスト>}`  
  * `\AfterEndPreamble{<テキスト>}`  
  * `\AfterEndDocument{<テキスト>}`  

(マクロ定義)

  * `\csdef<TeXマクロ定義記述*>`  
  * `\csgdef<TeXマクロ定義記述*>`  
  * `\csedef<TeXマクロ定義記述*>`  
  * `\csxdef<TeXマクロ定義記述*>`  

(命令の意味の操作)

  * `\cslet{<命令名1>}{<命令2>}`  
  * `\letcs{<命令1>}{<命令名2>}`  
  * `\csletcs{<命令名1>}{<命令名2>}`  
  * `\bxCsuse{<命令名>}`  
  * `\undef{<命令>}`  
  * `\csundef{<命令名>}`  
  * `\bxCsshow{<命令名>}`  
    `\bxCsuse` と `\bxCsshow` は、LaTeX の protect を施しているが、
    動く引数の中で展開されるとエラーになる。

(マクロの追記式定義)

  * `\appto{<命令>}{<テキスト>}`  
  * `\gappto{<命令>}{<テキスト>}`  
  * `\eappto{<命令>}{<テキスト>}`  
  * `\xappto{<命令>}{<テキスト>}`  
  * `\csappto{<命令名>}{<テキスト>}`  
  * `\csgappto{<命令名>}{<テキスト>}`  
  * `\cseappto{<命令名>}{<テキスト>}`  
  * `\csxappto{<命令名>}{<テキスト>}`  
  * `\preto{<命令>}{<テキスト>}`  
  * `\gpreto{<命令>}{<テキスト>}`  
  * `\epreto{<命令>}{<テキスト>}`  
  * `\xpreto{<命令>}{<テキスト>}`  
  * `\cspreto{<命令名>}{<テキスト>}`  
  * `\csgpreto{<命令名>}{<テキスト>}`  
  * `\csepreto{<命令名>}{<テキスト>}`  
  * `\csxpreto{<命令名>}{<テキスト>}`  

(真理値変数―bool系)

  * `\newbool{<名前>}`  
  * `\providebool{<名前>}`  
  * `\booltrue{<名前>}`  
  * `\boolfalse{<名前>}`  
  * `\setbool{<名前>}{<値>}`  
  * `\ifbool{<名前>}{<真>}{<偽>}`  
  * `\notbool{<名前>}{<真>}{<偽>}`  

(真理値変数―toggle系)

  * `\newtoggle{<名前>}`  
  * `\providetoggle{<名前>}`  
  * `\toggletrue{<名前>}`  
  * `\togglefalse{<名前>}`  
  * `\settoggle{<名前>}{<値>}`  
  * `\iftoggle{<名前>}{<真>}{<偽>}`  
  * `\nottoggle{<名前>}{<真>}{<偽>}`  

(定義済判定)

  * `\ifdef{<命令>}{<真>}{<偽>}`  
  * `\ifundef{<命令>}{<真>}{<偽>}`  
  * `\bxIfcsdef{<命令名>}{<真>}{<偽>}`  
  * `\bxIfcsundef{<命令名>}{<真>}{<偽>}`  
    `\bxIfcsdef` と `\bxIfcsdef` は動く引数の中で展開されるとエラーに
    なる。

### それ以外の命令

種々の事情により、「etoolbox 互換用」以外の機能も含まれている。

(エンジンチェック―ifトークン)

  * `\ifbxineTeX`  
  * `\ifbxinpdfTeX`  
  * `\ifbxinLuaTeX`  
  * `\ifbxinOmega`  
  * `\ifbxinAleph`  
  * `\ifbxinXeTeX`  
  * `\ifbxinpTeX`  
  * `\ifbxinupTeX`  
  * `\ifbxinnativeupTeX`（内部Unicode動作のupTeXか）  
    エンジンのチェック。これらは TeX の if-トークンである。

(エンジンチェック―LaTeXテスト)

  * `\bxIfineTeX{<真>}{<偽>}`  
  * `\bxIfinpdfTeX{<真>}{<偽>}`  
  * `\bxIfinLuaTeX{<真>}{<偽>}`  
  * `\bxIfinOmega{<真>}{<偽>}`  
  * `\bxIfinAleph{<真>}{<偽>}`  
  * `\bxIfinXeTeX{<真>}{<偽>}`  
  * `\bxIfinpTeX{<真>}{<偽>}`  
  * `\bxIfinupTeX{<真>}{<偽>}`  
  * `\bxIfinnativeupTeX{<真>}{<偽>}`（内部Unicode動作のupTeXか）  
    エンジンのチェック。これらは LaTeX 形式のテストである。（完全展開
    可能である。）

(プリミティブifトークンのLaTeXテスト版)

  * `\bxIf{<テスト>}{<真>}{<偽>}`  
  * `\bxIfcat{<テスト>}{<真>}{<偽>}`  
  * `\bxIfx{<テスト>}{<真>}{<偽>}`  
  * `\bxIfdim{<テスト>}{<真>}{<偽>}`  
  * `\bxIfnum{<テスト>}{<真>}{<偽>}`  
    TeX のプリミティブなテストを LaTeX 形式のテストにしたもの。例えば
    以下のようにして使う。  
    `\bxIfx{\somecs\relax}{\dotrue}{\dofalse}`  
    `\bxIfnum{\count@<3}{\dotrue}{\dofalse}`  
    （これらの命令は完全展開可能である。）

(プリミティブ判定)

  * `\bxIfPrimitive{<命令>}{<真>}{<偽>}`  
  * `\bxIfPrimitiveX{<命令名>}{<真>}{<偽>}`  
    `<命令>` が同名の TeX プリミティブであるかを判定する。機能としては
    pdfTeX の `\ifpdfprimitive` と同じ。`\bxIfPrimitive` は脆弱である。
    `\bxIfPrimitiveX` は完全展開可能（従って頑強）であるが、pdfTeX
    拡張の `\ifpdfprimitive` が使えない時は処理が非常に重い。
  * `\bxIfCsPrimitive{<命令名>}{<真>}{<偽>}`  
    引数が命令名であることを除き `\bxIfPrimitive` と同じ。

(文字列化)

  * `\bxDetokenize{<テキスト>}`  
    e-TeX 拡張の `\detokenize` と同じ機能で、e-TeX 拡張が有効の場合は
    `\detokenize` のエイリアスになる。無効の場合は自前の実装を使うが、
    処理が非常に重い。（完全展開可能である。）
  * `\bxStringify{<テキスト>}`  
    完全展開して detokenize した文字列に展開する。現状では全エンジン
    について自前の実装を使っていて処理が非常に重い。（完全展開可能。）

(トークン列比較)

  * `\bxIfExpToEqual{<テキスト1>}{<テキスト2>}{<真>}{<偽>}`  
  * `\bxIfExpToEqualX{<テキスト1>}{<テキスト2>}{<真>}{<偽>}`  
    2つのテキストについて、完全展開して detokenize した結果の文字列が
    等しいかを判定する。機能としては pdfTeX の `\pdfstrcmp` での等価
    判定と同じ。`\bxIfExpToEqual` は脆弱である。`\bxIfExpToEqualX`
    は完全展開可能だが、`\pdfstrcmp` が使えない時は処理が非常に重い。
  * `\bxIfstrequalX{<テキスト1>}{<テキスト2>}{<真>}{<偽>}`  
    etoolbox の `\ifstrequal` と同じ機能、すなわち 2 つのテキストに
    ついて展開せずに detokenize した結果の文字列が等しいかを判定する。
    元の `\ifstrequal` と異なり完全展開可能であるが、e-TeX 拡張が無効
    の時は処理が非常に重い。

(プレアンブル専用命令宣言)

  * `\bxPreamble<TeXマクロ定義命令><TeXマクロ定義記述>`  
  * `\bxPreamble<LaTeXマクロ定義命令>[*]<LaTeXマクロ定義記述>`  
    `\@onlypreamble` を設定してマクロを定義する。  
    ※ 実際の動作は単に `\bxPreamble\制御綴A[*]\制御綴B` を  
    `\@onlypreamble\制御綴B \制御綴A[*]\制御綴B`  
    に置き換えているだけである。

(保護付マクロ定義)

  * `\bxRobustdef<TeXマクロ定義記述>`  
  * `\bxRobustgdef<TeXマクロ定義記述>`  
  * `\bxRobustedef<TeXマクロ定義記述>`  
  * `\bxRobustxdef<TeXマクロ定義記述>`  
    保護付な命令を定義する。e-TeX 拡張が有効であれば、`\protected` を
    有効にし、無効であれば、LaTeX の保護機構を用いる。前に `\long` を
    付けられるが `\global` は不可。

(その他)

  * `\bxIfInMovingArg{<真>}{<偽>}`  
    いわゆる動く引数(実行が抑止された環境)であるかのテスト。実行が有効
    である場合は、<偽> を実行したのと等価になる。実行が抑止されている
    場合は「無意味な代入文」の後に <真> を続けたものに展開される。この
    命令は、動く引数の中での使用を事前に検査してエラーを出すという目的
    を想定している。(`\bxCheckForMovingArg` も参照。)

  * `\bxMessageToken{<文字列>}{<テキスト>}`  
    `<テキスト>` の中の `#1` を制御綴 `\<文字列>` に置換したテキスト
    を実行する。`\<文字列>` の意味は変化しない。`<テキスト>` 中で
    パラメタ `#1` 等を使う場合は `##1` のように書く必要がある。例えば
    以下のように用いる。

        \bxMessageToken{Hello TeX!}{\def\dohello{\do#1}}

    `\dohello` の定義は `\do` の後に制御綴「`\Hello TeX!`」が続いた
    ものになる。

  * `\bxCheckForMovingArg{<テキスト>}`  
    動く引数の中であるかの確認。動く引数の中でない場合は `<テキスト>`
    が実行されるが、ある場合は次のように「未定義命令の形」でエラーが
    表示される。ここでは、`\xx@prepare` の中で `\bxCheckForMovingArg`
    のテストを行っているとする。

        ! Undefined control sequence.
        <argument> \ ERROR: Use in wrong place!
        <*> \protected@edef\xx@example{\xx@prepare
                                                  \xx@tmpa}

    ※ 実行が抑止されている場合は `\errmessage` プリミティブも実行
    されないので、普通にエラー表示ができないのである。  
    ※ `\bxIfInMovingArg` を利用しているので、そこに述べられている
    ように、動く引数である場合の展開結果にはゴミが残る。

zxbase パッケージ ― XeTeX 用基礎ライブラリ
-------------------------------------------

作者（ZR）の制作する他のパッケージで必要な、XeTeX 特有の機能を提供する。

現状では、本パッケージに公開の機能は存在しない。

更新履歴
--------

  * Version 1.2a 〈2023/02/23〉
      - `\ifbxinnativeupTeX`／`\bxIfinnativeupTeX` を追加。
      - バグ修正。
  * Version 1.2  〈2020/10/04〉
      - LaTeX カーネル 2020/10/01 版への対応。
      - `\bxDocumentSpecialUrgent` を非推奨にした。
  * Version 1.1  〈2017/05/29〉
      - 内容の整理。
      - 一部の機能を非推奨にした。
  * Version 1.0  〈2013/04/29〉
      - ほぼ全面的な書き直し。
  * Version 0.5  〈2010/06/15〉
      - bxbase: `\JI`/`\KI` を追加。
      - bxbase: `\dvipdfmxmapline`/`\dvipdfmxmapfont` を追加。
      - bxutf8: BMP 外の符号値への対応。
  * Version 0.4a 〈2009/11/16〉
      - bxbase で `\UI`/`\Ux` を zxjatype と、`\AJ` を zxotf
        と連携させた。
      - zxbase パッケージを追加。
  * Version 0.4  〈2009/07/05〉
      - PXbase の v0.4 に合わせた改訂。
  * Version 0.3  〈2008/04/06〉
      - bxutf8x を追加。
      - bxutf8 のバグを修正。
      - bxbase でも pxbase の命令 `\recordpapersize` を使用可能にした。
  * Version 0.2  〈2008/03/28〉
      - 最初の公開版。

--------------------
Takayuki YATO (aka. "ZR")  
https://github.com/zr-tex8r
