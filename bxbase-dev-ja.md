bxbase $B$K4^$^$l$k3+H/<T8~$15!G=(B
===============================

$B$3$3$G$O!"(Bbxbase $B%Q%C%1!<%8!J(Bbxbase.sty$B!K$,Ds6!$9$k3+H/<T8~$1(B
$B5!G=$K$D$$$F4JC1$K2r@b$9$k!#$3$l$O<!$N(B 2 $B$D$KBgJL$5$l$k!#(B

  * bxtoolbox $B%Q%C%1!<%8!J(Bbxbase $B$+$iFI$_9~$^$l$k!K$N5!G=!'(B  
    etoolbox $B8_495!G=!"$=$NB>$NHFMQE*$J5!G=!#(B
  * bxbase.def$B!J(Bbxbase $B$N%3!<%I$N<BBN!K$GDj5A$5$l$k5!G=!'(B  
    $B@[:n%Q%C%1!<%8$G$N;HMQ$rA[Dj$7$?5!G=!#(B

### $B=q<05-=R$K4X$9$kCm0U(B

`<LaTeX$B%^%/%mDj5A5-=R(B>` $B$O(B `\newcommand` $BEy$N(B LaTeX $B%^%/%mDj5AL?Na$K(B
$B8eB3$9$kMWAGNs$G!"0J2<$N$b$N$KEy$7$$!#(B

    {<$BL?Na(B>}[<$B0z?t8D?t(B>][<$B0z?t4{DjCM(B>]{<$BCV49%F%-%9%H(B>}

`<TeX$B%^%/%mDj5A5-=R(B>` $B$O(B `\def` $BEy$N(B TeX $B%^%/%mDj5A%W%j%_%F%#%V$K(B
$B8eB3$9$kMWAGNs$G!"0J2<$N$b$N$KEy$7$$!#(B

    <$BL?Na(B><$B0z?t@k8@It(B>{<$BCV49%F%-%9%H(B>}

`<TeX$B%^%/%mDj5A5-=R(B*>` $B$O(B `<TeX$B%^%/%mDj5A5-=R(B>` $B$N@hF,$N(B `<$BL?Na(B>`
$B$r=|5n$7$?$b$N!#(B

bxbase.def $B$GDj5A$5$l$k5!G=(B
---------------------------

### $B%W%m%0%i%_%s%0Jd=u(B

  * `\bxDebug{<$B%F%-%9%H(B>}`  
    $B%G%P%C%/=PNOMQL?Na!#$3$N%Q%C%1!<%8$G$NDj5A$G$O2?$b$7$J$$!#(B
  * `\bxRequireDefinition{<$B%U%!%$%k%Y!<%9L>(B>}`  
    $B3HD%;R(B .def $B$N%U%!%$%k$r(B `\usepackage` $B$HF1$8J}<0$GFI$_9~$`!#(B  
    [$B5lL?NaL>(B: `\bxInputDefFile`]
  * `\bxNullify\$B@)8fDV(B`  
    `\$B@)8fDV(B` $B$r!V2?$b$7$J$$L?Na!W$G(B `\providecommand` $B$K$h$j(B
    $B>e=q$-$5$l$J$$$b$N$K:FDj5A$9$k!#(B
  * `\bxForEachIn<$B0z?t(B1>,<$B0z?t(B2>,...\do{<$BCV49%F%-%9%H(B>}`  
    $B3F!9$N0z?t$K$D$$$F!"(B`<$BCV49%F%-%9%H(B>` $B$N(B `#1` $B$r$=$l$GCV$-49$($?(B
    $B$b$N$r<B9T$9$k!#(BLaTeX $B$N(B `\@for` $B$N%i%C%Q!<$G!"(B`\@for` $B$HF1$8$/!"(B
    `\bxForEachIn` $B$ND>8e$N%H!<%/%s$OM=$a0lEYE83+$5$l$k!#(B
  * `\bxForEachTokenIn<$B%H!<%/%s(B1><$B%H!<%/%s(B2>...\do{<$BCV49%F%-%9%H(B>}`  
    $B3F!9$N0z?t$K$D$$$F(B `<$BCV49%F%-%9%H(B>` $B$N(B `#1` $B$rCV$-49$($?$b$N$r(B
    $B<B9T$9$k!#(BLaTeX $B$N(B `\@tfor` $B$N%i%C%Q!<!#(B
  * `\bxWithArgExpd{<$B0z?t(B1>}\do{<$BCV49%F%-%9%H(B>}`  
  * `\bxWithArgsExpd{<$B0z?t(B1>}{<$B0z?t(B2>}...\do{<$BCV49%F%-%9%H(B>}`  
    `<$BCV49%F%-%9%H(B>` $BCf$N(B `#1`$B!"(B`#2`$B!D(B $B$r3F!9$N0z?t$r0l2sE83+$7$?(B
    $B$b$N$KCV$-49$($?$b$N$r<B9T$9$k!#(B`\bxWithArgExpd` $B$O(B 1 $B0z?tMQ$K(B
    $B:GE,2=$7$?$b$N!#(B
  * `\bxWithArgFullExpd{<$B0z?t(B1>}\do{<$BCV49%F%-%9%H(B>}`  
  * `\bxWithArgsFullExpd{<$B0z?t(B1>}{<$B0z?t(B2>}...\do{<$BCV49%F%-%9%H(B>}`  
    `\bxWithArgsExpd` $B$HF1MM$@$,!"0l2sE83+$G$J$/40A4E83+$9$kE@$,(B
    $B0[$J$k!#(B
  * `\bxChompComma<$BL?Na(B>`  
    `<$BL?Na(B>` $B$N(B $BCV49%F%-%9%H$N@hF,$,(B `,` $B$N>l9g!"$=$l$r:o=|$7$?$b$N$G(B
    $B:FDj5A$9$k!#(B
  * `\bxAssign<$BBeF~J8(B>\relax`  
    $BBeF~$r9T$C$?8e!"BeF~J8$N8e$m$K%4%_$,$J$$$+$rH=Dj$7$=$N7k2L$r(B
    $B%9%$%C%A(B `\ifbxOk` $B$KJV$9!#(B
  * `\bxCheckMA<$B%F%-%9%H(B>\bxEndCheckMA`  
    `\edef` $BCf$G$O$3$NItJ,$,%(%i!<$r=P$9L?Na$KE83+$5$l$k!#(B
  * `\bxCheckCounterpart{<$B%Y!<%9L>(B>}`  
    $B8=:_$N%U%!%$%k$H(B `<$B%Y!<%9L>(B>`$B!JF1$83HD%;R!K$H$N4V$GHG$rHf3S$9$k!#(B
    $B$b$7!"8e<T$,FI9~:Q$G$+$DHG$,?7$7$$>l9g$O!"8=:_$N%U%!%$%k$NFI9~$r(B
    $BCf;_$9$k!#(B  
    [$B5lL>>N!'(B `\bxCheckCPart`]

### TeX $B%(%s%8%sH=JL(B

  * `\bxEngineTypeX`  [$B@0?tDj?t(B]  
    1=pTeX$B3HD%(B; 2=XeTeX$B3HD%(B; 3=Omega$B3HD%(B; 0=$B0J>e$K3:Ev$;$:(B
  * `\bxEngineTypeY`  [$B@0?tDj?t(B]  
    1=eTeX$B3HD%(B; 3=pdfTeX$B3HD%(B; 5=LuaTeX$B3HD%(B; 0=$B0J>e$K3:Ev$;$:(B  
    $B"(=>Mh$O(B LuaTeX $B$O(B X/Y=3/3 $B$H$7$F$$$?$,!">/$J$/$H$b8=:_$N(B
    LaTeX $B$G$O(B LuaTeX $B$O(B Omega $B3HD%$r$b$D$H$_$J$5$J$$$N$G!"(B
    X/Y=0/5 $B$N0LCV$KJQ99$7$?!#(B  
    $B"((BupTeX $B$+H]$+$NH=Dj$O(B ifptex $B%Q%C%1!<%8$rMQ$$$k!#(B

### Babel $B4X78(B

  * `\bxBDHookBabel`  
    Babel $B4X78$N(B begin-document $B%U%C%/!#(B
  * `\bxAtBeginDocumentBabel{<$B%F%-%9%H(B>}`  
    Babel $BFI9~;~$K$N$_<B9T$5$l$k(B begin-document $B;~$N%U%C%/!#(B
  * `\bxTrivLangDef{<$B8@8lL>(B>}`  
    $BCf?H!J%-%c%W%7%g%sDj5AEy!K$,6u$N(B Babel $B8@8l%*%W%7%g%s$r@8@.$9$k!#(B

### $B?tCM$N=q<02==PNO(B

  * `\bxToHexTwo{<$B@0?t(B>}`      [%02X $B7A<0(B; 0x00$B!A(BFF]  
  * `\bxToHexThree{<$B@0?t(B>}`    [%03X $B7A<0(B; 0x000$B!A(BFFF]  
  * `\bxToHexFour{<$B@0?t(B>}`     [%04X $B7A<0(B; 0x0000$B!A(BFFFF]  
  * `\bxToHexFive{<$B@0?t(B>}`     [%05X $B7A<0(B; 0x00000$B!A(BFFFFF]  
  * `\bxToHexFiveX{<$B@0?t(B>}`    [%05X $B7A<0(B; 0x00000$B!A(BFFFFF $B"((B1]  
  * `\bxToHexEight{<$B@0?t(B>}`    [%08X $B7A<0(B; 0x00000000$B!A(B7FFFFFFF]  
  * `\bxToHexTiny{<$B@0?t(B>}`     [%X $B7A<0(B; 0x0$B!A(BFF]  
  * `\bxToHexSmall{<$B@0?t(B>}`    [%X $B7A<0(B; 0x0$B!A(B7FFF]  
  * `\bxToHexUC{<$B@0?t(B>}`       [%04X $B7A<0(B; 0x0000$B!A(B10FFFF $B"((B2]  
    16 $B?JI=5-$r(B `\bxHex` $B$KJV$9!#(BUC $B$O(B 4$B!A(B6 $B7e$G$NI=5-!#(B  
    $B"((B1 0xFFFFF $B$rD6$($k>l9g$O(B `FFFFF` $B$K$J$k(B  
    $B"((B2 XeTeX/LuaTeX/upTeX $B$N>l9g!"(B`\char` $B$,2DG=$JHO0O!#(B
  * `\bxToDecFour{<$B@0?t(B>}`     [%04d $B7A<0(B; 0000$B!A(B9999]  
  * `\bxToDecFive{<$B@0?t(B>}`     [%05d $B7A<0(B; 00000$B!A(B99999]  
    $B%<%mIU$N(B 10 $B?JI=5-$r(B `\bxHex` $B$KJV$9!#(B

### $BId9fCM$K$h$kF~NO(B

  * `\bxBDHookUnicode`  
  * `\bxBDHookJisInput`  
    $BId9fCMF~NO$K4X$9$k(B begin-document $B%U%C%/!#(B
  * `\bxCodeValueSeq\$B@)8fDV(B{<$BId9fCM(B>,...}    [16$B?J(B]`  
  * `\bxCodeValueSeqD\$B@)8fDV(B{<$BId9fCM(B>,...}   [10$B?J(B]`  
    $B3F!9$N(B `<$BId9fCM(B>` $B$r2r<a$7$?7k2L$r(B `\bxUcv` $B$KBeF~$7$F%^%/%m(B
    `\$B@)8fDV(B` $B$r8F$S=P$9!#2r<aJ}K!$O$=$l$>$l(B `\Ux` $B$H(B `\AJ` $BL?Na$N(B
    $B2r@b$K$"$kDL$j!#(B
  * `\bxUHex{<$B%3!<%ICM(B16$B?JI=5-(B>}`  
    bxutf8 $B$,9=@.$9$kFbItI=8=!#MQ$$$k5!G=$O(B `\Ux` $B$HF1$8!#(B
  * `\bxUInt{<$B@0?t(B>}`  
    bxutf8x $B$,9=@.$9$kFbItI=8=!#MQ$$$k5!G=$O(B `\Ux` $B$HF1$8!#(B

### $BJ8;zNsA`:n(B

  * `\bxToLower{<$BJ8;zNs(B>}  [$B>.J8;z(B]`  
  * `\bxToUpper{<$BJ8;zNs(B>}  [$BBgJ8;z(B]`  
    `<$BJ8;zNs(B>` $B$r>.J8;z!?BgJ8;z$KJQ49$7$?$b$N$r(B `\bxRes` $B$KJV$9!#(B

### Special $B=PNO(B

  * `\bxDocumentSpecial{<$B%F%-%9%H(B>}`  
    `\AtBeginDvi` $B$rIaDL$KMQ$$$F(B DVI $B$N@hF,It$K(B special $B$r=PNO$9$k!#(B
  * `\bxDocumentSpecialUrgent{<$B%F%-%9%H(B>}`  
    DVI $B$N$J$k$Y$/@hF,!JB>$N(B special $B$h$jA0!K$N0LCV$K(B special $B$r=PNO!#(B

### Safe caret $B5!G=(B

  * `\bxBDHookSafeCaret`  
    safe caret $B5!G=$K4X$9$k(B begin-document $B%U%C%/!#(B
  * `\bxEnableSafeCaret`  
    safe caret $B5!G=$r;HMQ2DG=$K$7$F$*$/!#$9$J$o$A!"%W%l%"%s%V%k$G$3$N(B
    $BL?Na$,8F$P$l$J$+$C$?>l9g!"(Bsafe caret $B$O;HMQIT2D$K$J$k!#<B:]$K$"$k(B
    $B>u67$G(B safe caret $B$rM-8z$K$9$k$K$O!"(B`\bx@acr@normcaret` $B$r!V$=$N(B
    $B>u67$G$NK\Mh$N(B `^` $B$NF0:n!W$KDj5A$7$?>e$G(B `^` $B$r%"%/%F%#%V$K$9$k(B
    $BI,MW$,$"$k!#(B  
    $B"((B $B%f!<%6L?Na$N(B `\safecaret` $B$O$3$NL?Na$r<B9T$7$?>e$G!"(Bverbatim
    $B$H(B babel $B$G$NE,@Z$J(B safe caret $B=hM}$rM-8z2=$7$F$$$k!#(B

### Shadow map $B5!G=(B

Shadow map $B$H$O!V(B16 $B%S%C%H@0?t(B $B"*(B $B@0?t!W$N<LA|$r(B TFM $B$H$7$FI=8=(B
$B$7$?$b$N!#(B

  * `\bxUseShadowMap\$B@)8fDV(B{<TFM$BL>(B>}`  
    `\$B@)8fDV(B` $B$r;XDj$N(B TFM $B$+$i@8@.$5$l$k(B shadow map $B$H$7$FDj5A!#(B
  * `\bxMap\$B@)8fDV(B`  
    $B@0?t%l%8%9%?(B `\bxUcv` $B$N8=:_$NCM$K(B shadow map $B$rE,MQ$7!"$=$N7k2L$r(B
    `\bxUcv` $B$KBeF~$9$k!#(B

### $B%b%8%e!<%kL>(B

$B$3$3$G$$$&!V%b%8%e!<%k!W$H$OJ8=q%/%i%9!J(B.cls$B!K!&%Q%C%1!<%8!J(B.sty$B!K!&(B
$BDj5A%U%!%$%k!J(B.def$B!K$NAm>N!#!V%b%8%e!<%kFI9~Cf$KH/@8$9$k%(%i!<$r=PNO(B
$B$9$k$?$a$N%^%/%m!W$rJL$N%b%8%e!<%kFb$GDj5A$9$k:]$K!"8F$S=P$7$?B&$N(B
$B%b%8%e!<%kL>$r%a%C%;!<%8Cf$K=PNO$5$;$k$?$a$N;EAH$_!#(B

  * `\bxSetModuleName{<$BJ8;zNs(B>}`  
    $B8=:_$N%b%8%e!<%k$KBP$9$k%b%8%e!<%kL>$r@_Dj$9$k!#(B
  * `\bxModuleName`  
    $B8=:_$N%b%8%e!<%k$KBP$9$k%b%8%e!<%kL>$KE83+$5$l$k!#%b%8%e!<%kL>$,(B
    $B@_Dj$5$l$F$$$J$$>l9g$O%U%!%$%k$N%Y!<%9L>$rBe$o$j$K;H$&!#(B
  * `\bxError`            [`\PackageError` $B$KBP1~(B]  
  * `\bxWarning`          [`\PackageWarning` $B$KBP1~(B]  
  * `\bxWarningNoLine`    [`\PackageWarningNoLine` $B$KBP1~(B]  
  * `\bxInfo`             [`\PackageInfo` $B$KBP1~(B]  
    $B8=:_$N%b%8%e!<%kL>$r%Q%C%1!<%8L>$H$7$F(B `\PackageError` $BEy$r8F$V!#(B

### keyval $B$N3HD%(B

$B!J(Bxkeyval $B$,Ia5Z$7$?:#$G$OHs?d>)$+$b!D!K(B

keyval $B$N(B `\setkeys` $B$K$D$$$F!"!VL$Dj5A$N%-!<$r%(%i!<$K$;$:!"Be$o$j$K(B
$BL$Dj5A$N%-!<$N%j%9%H$r:n@.$9$k!W$H$$$&JQ<o$rDs6!$9$k!#$3$N5!G=$O(B
xkeyval $B$G(B `\setkeys*` $B$H$7$FDs6!$5$l$F$$$k!#$7$+$7(B xkeyval $B$,MxMQ(B
$B$G$-$J$$4D6-$KBP1~$9$k$?$a$K(B keyval $B$X$N%Q%C%A$H$7$F<B8=$9$k$3$H(B
$B$K$9$k!#$7$+$7!"(Bxkeyval $B$O$3$N%Q%C%A$rL58z2=$7$F$7$^$&!#=>$C$F(B
xkeyval.sty $B$,B8:_$9$k$+$K1~$8$F=hM}$rJ,$1$k$3$H$K$7$?!#(B

  * `\bxPrepareSetKeysSafe`  
    `\bxSetKeysSafe` $B$r;HMQ2DG=$K$9$k!#(B  
    $B"((B xkeyval.sty $B$,B8:_$9$k$+$rH=Dj$7!"B8:_$9$l$PFI$_9~$`!#(B
    $B$=$7$F(B `\bxSetKeysSafe` $B$N<B8=J}K!$r$3$NCJ3,$G3NDj$5$;$k!#(B
  * `\bxSetKeysSafe{<$B%U%!%_%j(B>}{<$B%F%-%9%H(B>}`  
    `\setkeys` $B$HF1MM$@$,!"L$Dj5A$N%-!<$r%(%i!<$H$;$:!"Be$o$j$K(B
    $BL$Dj5A$N%-!<$+$i$J$k%3%s%^6h@Z$j$N%j%9%H$r(B `\bxRestKeys` $B$K(B
    $BBeF~$9$k!#(B

### $B%I%i%$%PH=JL(B

$B0J2<$N@bL@$G!V@hE7E*$J!W%I%i%$%P$H$O!"(BTeX $B<B9T;~$K;HMQ$,H=Dj$G$-$k(B
$B$b$N!J;v<B>e!V(BTeX $B%(%s%8%s$,%I%i%$%P$r7s$M$k$b$N!W$KEy$7$$!K$r;X$7!"(B
$BNc$($P(B pdfTeX$B!"(BXeTeX$B!"(BLuaTeX $B$,3:Ev$9$k!#(B

  * `\bxDriverList`  
    $B!J8eE7E*$J!K%I%i%$%PL>$N%j%9%H!#(B  
    $B"((B $B8=>u$G$O!V(B`dvips,dvipdfmx,dviout`$B!W!#(B
  * `\bxDriverInherent`  
    $B@hE7E*$J%I%i%$%PL>!JL$Dj5A$J$i6u!K$KE83+$5$l$k!#(B
  * `\bxSetDriver[<$B%U%!%$%kL>(B>]{<$B%I%i%$%PL>(B>}`  
    $B;XDj$N%U%!%$%kL>$r$b$D%b%8%e!<%k$KBP$9$k%I%i%$%PL>$r;XDj$9$k!#(B
    `<$B%U%!%$%kL>(B>` $B$,$J$$>l9g$O8=:_$N%b%8%e!<%k$KBP$9$k@_Dj!#(B
  * `\bxDriver`  
    $B8=:_$N%b%8%e!<%k$KBP$9$k%I%i%$%PL>$KE83+$5$l$k!#L$Dj5A$J$i$P(B
    `default` $B$rJV$9!#(B
  * `\bxDriverSpecifiedFor{<$B%U%!%$%kL>(B>}`  
    `\bxDriver` $B$HF1MM$@$,!";XDj$N%U%!%$%kL>$r$b$D%b%8%e!<%k$K(B
    $BBP$9$k@_Dj$rJV$9!#(B
  * `\bxDefineDDProcess{<$BL>A0(B>}{<$B%I%i%$%PL>(B>}<TeX$B%^%/%mDj5A5-=R(B*>`  
    $B%I%i%$%P0MB8%^%/%m$rDj5A$9$k!#(B
  * `\bxDefineDDProcessDefault{<$BL>A0(B>}`  
    `<$B%I%i%$%PL>(B>` $B$,(B `default` $B$N(B `\bxDefineDDProcess`$B!#(B
  * `\bxDoDDProcess{<$BL>A0(B>}`  
    $B%I%i%$%P0MB8%^%/%m$r<B9T$9$k!#(B
  * `\bxDeclareDriverOptions`  
    $B8eE7E*$J%I%i%$%PL>$N3F!9$K$D$$$F!"!V(B`\bxSetDriver{$B%I%i%$%PL>(B}`
    $B$r8F$V!W$H$$$&F0:n$N%Q%C%1!<%8!J%/%i%9!K%*%W%7%g%s$rDj5A$9$k!#(B

### bxtoolbox $B$GDj5A$5$l$k5!G=(B

#### etoolbox $B8_49L?Na(B

$B$3$3$K5s$2$kL?Na$O!"(Betoolbox $B$NL?Na$NJ#@=$G$"$j!"$=$l$>$l!"L?NaL>$N(B
$BF,$N(B bx $B$r<h$C$F@hF,$r>.J8;z$KJQ$($?L>A0!J(B`\bxCsde` $B"*(B `\csdef`$B!K(B
$B$N(B etoolbox $B$NL?Na$KBP1~$9$k!#(Be-TeX $B3HD%$r$b$D%(%s%8%s$GF0:n$5$;$k(B
$B>l9g$O!"<B:]$K(B etoolbox $B$rFI$_9~$s$G$=$l$NL?Na$N%(%$%j%"%9$H$9$k$,!"(B
$B$=$&$G$J$$>l9g$O<+A0$N<BAu$rMQ$$$k!#(B

$B3FL?Na$N@bL@$K$D$$$F$O(B etoolbox $B$N%^%K%e%"%k$r;2>H$5$l$?$$!#(B
etoolbox $B$N85$NL?Na$H;EMM$,0[$J$kItJ,$K$N$_@bL@$rIU$7$F$$$k(B
$B!J$3$N@bL@$O(B e-TeX $BHs3HD%$N%(%s%8%s$G$NF0:n;~$N$_Ev$F$O$^$k$3$H(B
$B$KCm0U!K!#(B

($B4h6/$JL?Na$NDj5A(B)

  * `\bxNewrobustcmd[*]<LaTeX$B%^%/%mDj5A5-=R(B>`  
  * `\bxRenewrobustcmd[*]<LaTeX$B%^%/%mDj5A5-=R(B>`  
  * `\bxProviderobustcommand[*]<LaTeX$B%^%/%mDj5A5-=R(B>`  
  * `\bxRobustify{<$BL?Na(B>}`  
      e-TeX $B$N(B \protected $B$NBe$o$j$K(B LaTeX $B$N(B protect $B=hM}$rMQ$$$k!#7k2L(B
      $BE*$K(B \DeclareRobustCommand $B$HF1$8=hM}$,;H$o$l$k!#(B

($B%a%$%sJ8=q%3%s%Q%$%k;~%U%C%/(B)

  * `\AfterPreamble{<$B%F%-%9%H(B>}`  
  * `\AtEndPreamble{<$B%F%-%9%H(B>}`  
  * `\AfterEndPreamble{<$B%F%-%9%H(B>}`  
  * `\AfterEndDocument{<$B%F%-%9%H(B>}`  

($B%^%/%mDj5A(B)

  * `\csdef<TeX$B%^%/%mDj5A5-=R(B*>`  
  * `\csgdef<TeX$B%^%/%mDj5A5-=R(B*>`  
  * `\csedef<TeX$B%^%/%mDj5A5-=R(B*>`  
  * `\csxdef<TeX$B%^%/%mDj5A5-=R(B*>`  

($BL?Na$N0UL#$NA`:n(B)

  * `\cslet{<$BL?NaL>(B1>}{<$BL?Na(B2>}`  
  * `\letcs{<$BL?Na(B1>}{<$BL?NaL>(B2>}`  
  * `\csletcs{<$BL?NaL>(B1>}{<$BL?NaL>(B2>}`  
  * `\bxCsuse{<$BL?NaL>(B>}`  
  * `\undef{<$BL?Na(B>}`  
  * `\csundef{<$BL?NaL>(B>}`  
  * `\bxCsshow{<$BL?NaL>(B>}`  
    `\bxCsuse` $B$H(B `\bxCsshow` $B$O!"(BLaTeX $B$N(B protect $B$r;\$7$F$$$k$,!"(B
    $BF0$/0z?t$NCf$GE83+$5$l$k$H%(%i!<$K$J$k!#(B

($B%^%/%m$NDI5-<0Dj5A(B)

  * `\appto{<$BL?Na(B>}{<$B%F%-%9%H(B>}`  
  * `\gappto{<$BL?Na(B>}{<$B%F%-%9%H(B>}`  
  * `\eappto{<$BL?Na(B>}{<$B%F%-%9%H(B>}`  
  * `\xappto{<$BL?Na(B>}{<$B%F%-%9%H(B>}`  
  * `\csappto{<$BL?NaL>(B>}{<$B%F%-%9%H(B>}`  
  * `\csgappto{<$BL?NaL>(B>}{<$B%F%-%9%H(B>}`  
  * `\cseappto{<$BL?NaL>(B>}{<$B%F%-%9%H(B>}`  
  * `\csxappto{<$BL?NaL>(B>}{<$B%F%-%9%H(B>}`  
  * `\preto{<$BL?Na(B>}{<$B%F%-%9%H(B>}`  
  * `\gpreto{<$BL?Na(B>}{<$B%F%-%9%H(B>}`  
  * `\epreto{<$BL?Na(B>}{<$B%F%-%9%H(B>}`  
  * `\xpreto{<$BL?Na(B>}{<$B%F%-%9%H(B>}`  
  * `\cspreto{<$BL?NaL>(B>}{<$B%F%-%9%H(B>}`  
  * `\csgpreto{<$BL?NaL>(B>}{<$B%F%-%9%H(B>}`  
  * `\csepreto{<$BL?NaL>(B>}{<$B%F%-%9%H(B>}`  
  * `\csxpreto{<$BL?NaL>(B>}{<$B%F%-%9%H(B>}`  

($B??M}CMJQ?t!=(Bbool$B7O(B)

  * `\newbool{<$BL>A0(B>}`  
  * `\providebool{<$BL>A0(B>}`  
  * `\booltrue{<$BL>A0(B>}`  
  * `\boolfalse{<$BL>A0(B>}`  
  * `\setbool{<$BL>A0(B>}{<$BCM(B>}`  
  * `\ifbool{<$BL>A0(B>}{<$B??(B>}{<$B56(B>}`  
  * `\notbool{<$BL>A0(B>}{<$B??(B>}{<$B56(B>}`  

($B??M}CMJQ?t!=(Btoggle$B7O(B)

  * `\newtoggle{<$BL>A0(B>}`  
  * `\providetoggle{<$BL>A0(B>}`  
  * `\toggletrue{<$BL>A0(B>}`  
  * `\togglefalse{<$BL>A0(B>}`  
  * `\settoggle{<$BL>A0(B>}{<$BCM(B>}`  
  * `\iftoggle{<$BL>A0(B>}{<$B??(B>}{<$B56(B>}`  
  * `\nottoggle{<$BL>A0(B>}{<$B??(B>}{<$B56(B>}`  

($BDj5A:QH=Dj(B)

  * `\ifdef{<$BL?Na(B>}{<$B??(B>}{<$B56(B>}`  
  * `\ifundef{<$BL?Na(B>}{<$B??(B>}{<$B56(B>}`  
  * `\bxIfcsdef{<$BL?NaL>(B>}{<$B??(B>}{<$B56(B>}`  
  * `\bxIfcsundef{<$BL?NaL>(B>}{<$B??(B>}{<$B56(B>}`  
    `\bxIfcsdef` $B$H(B `\bxIfcsdef` $B$OF0$/0z?t$NCf$GE83+$5$l$k$H%(%i!<$K(B
    $B$J$k!#(B

#### $B$=$l0J30$NL?Na(B

($B%(%s%8%s%A%'%C%/!=(Bif$B%H!<%/%s(B)

  * `\ifbxineTeX`  
  * `\ifbxinpdfTeX`  
  * `\ifbxinLuaTeX`  
  * `\ifbxinOmega`  
  * `\ifbxinAleph`  
  * `\ifbxinXeTeX`  
  * `\ifbxinpTeX`  
  * `\ifbxinupTeX`  
    $B%(%s%8%s$N%A%'%C%/!#$3$l$i$O(B TeX $B$N(B if-$B%H!<%/%s$G$"$k!#(B

($B%(%s%8%s%A%'%C%/!=(BLaTeX$B%F%9%H(B)

  * `\bxIfineTeX{<$B??(B>}{<$B56(B>}`  
  * `\bxIfinpdfTeX{<$B??(B>}{<$B56(B>}`  
  * `\bxIfinLuaTeX{<$B??(B>}{<$B56(B>}`  
  * `\bxIfinOmega{<$B??(B>}{<$B56(B>}`  
  * `\bxIfinAleph{<$B??(B>}{<$B56(B>}`  
  * `\bxIfinXeTeX{<$B??(B>}{<$B56(B>}`  
  * `\bxIfinpTeX{<$B??(B>}{<$B56(B>}`  
  * `\bxIfinupTeX{<$B??(B>}{<$B56(B>}`  
    $B%(%s%8%s$N%A%'%C%/!#$3$l$i$O(B LaTeX $B7A<0$N%F%9%H$G$"$k!#!J40A4E83+(B
    $B2DG=$G$"$k!#!K(B

($B%W%j%_%F%#%V(Bif$B%H!<%/%s$N(BLaTeX$B%F%9%HHG(B)

  * `\bxIf{<$B%F%9%H(B>}{<$B??(B>}{<$B56(B>}`  
  * `\bxIfcat{<$B%F%9%H(B>}{<$B??(B>}{<$B56(B>}`  
  * `\bxIfx{<$B%F%9%H(B>}{<$B??(B>}{<$B56(B>}`  
  * `\bxIfdim{<$B%F%9%H(B>}{<$B??(B>}{<$B56(B>}`  
  * `\bxIfnum{<$B%F%9%H(B>}{<$B??(B>}{<$B56(B>}`  
    TeX $B$N%W%j%_%F%#%V$J%F%9%H$r(B LaTeX $B7A<0$N%F%9%H$K$7$?$b$N!#Nc$($P(B
    $B0J2<$N$h$&$K$7$F;H$&!#(B  
    `\bxIfx{\somecs\relax}{\dotrue}{\dofalse}`  
    `\bxIfnum{\count@<3}{\dotrue}{\dofalse}`  
    $B!J$3$l$i$NL?Na$O40A4E83+2DG=$G$"$k!#!K(B

($B%W%j%_%F%#%VH=Dj(B)

  * `\bxIfPrimitive{<$BL?Na(B>}{<$B??(B>}{<$B56(B>}`  
  * `\bxIfPrimitiveX{<$BL?NaL>(B>}{<$B??(B>}{<$B56(B>}`  
    `<$BL?Na(B>` $B$,F1L>$N(B TeX $B%W%j%_%F%#%V$G$"$k$+$rH=Dj$9$k!#5!G=$H$7$F$O(B
    pdfTeX $B$N(B `\ifpdfprimitive` $B$HF1$8!#(B`\bxIfPrimitive` $B$O@H<e$G$"$k!#(B
    `\bxIfPrimitiveX` $B$O40A4E83+2DG=!J=>$C$F4h6/!K$G$"$k$,!"(BpdfTeX
    $B3HD%$N(B `\ifpdfprimitive` $B$,;H$($J$$;~$O=hM}$,Hs>o$K=E$$!#(B
  * `\bxIfCsPrimitive{<$BL?NaL>(B>}{<$B??(B>}{<$B56(B>}`  
    $B0z?t$,L?NaL>$G$"$k$3$H$r=|$-(B `\bxIfPrimitive` $B$HF1$8!#(B

($BJ8;zNs2=(B)

  * `\bxDetokenize{<$B%F%-%9%H(B>}`  
    e-TeX $B3HD%$N(B `\detokenize` $B$HF1$85!G=$G!"(Be-TeX $B3HD%$,M-8z$N>l9g$O(B
    `\detokenize` $B$N%(%$%j%"%9$K$J$k!#L58z$N>l9g$O<+A0$N<BAu$r;H$&$,!"(B
    $B=hM}$,Hs>o$K=E$$!#!J40A4E83+2DG=$G$"$k!#!K(B
  * `\bxStringify{<$B%F%-%9%H(B>}`  
    $B40A4E83+$7$F(B detokenize $B$7$?J8;zNs$KE83+$9$k!#8=>u$G$OA4%(%s%8%s(B
    $B$K$D$$$F<+A0$N<BAu$r;H$C$F$$$F=hM}$,Hs>o$K=E$$!#!J40A4E83+2DG=!#!K(B

($B%H!<%/%sNsHf3S(B)

  * `\bxIfExpToEqual{<$B%F%-%9%H(B1>}{<$B%F%-%9%H(B2>}{<$B??(B>}{<$B56(B>}`  
  * `\bxIfExpToEqualX{<$B%F%-%9%H(B1>}{<$B%F%-%9%H(B2>}{<$B??(B>}{<$B56(B>}`  
    2$B$D$N%F%-%9%H$K$D$$$F!"40A4E83+$7$F(B detokenize $B$7$?7k2L$NJ8;zNs$,(B
    $BEy$7$$$+$rH=Dj$9$k!#5!G=$H$7$F$O(B pdfTeX $B$N(B `\pdfstrcmp` $B$G$NEy2A(B
    $BH=Dj$HF1$8!#(B`\bxIfExpToEqual` $B$O@H<e$G$"$k!#(B`\bxIfExpToEqualX`
    $B$O40A4E83+2DG=$@$,!"(B`\pdfstrcmp` $B$,;H$($J$$;~$O=hM}$,Hs>o$K=E$$!#(B
  * `\bxIfstrequalX{<$B%F%-%9%H(B1>}{<$B%F%-%9%H(B2>}{<$B??(B>}{<$B56(B>}`  
    etoolbox $B$N(B `\ifstrequal` $B$HF1$85!G=!"$9$J$o$A(B 2 $B$D$N%F%-%9%H$K(B
    $B$D$$$FE83+$;$:$K(B detokenize $B$7$?7k2L$NJ8;zNs$,Ey$7$$$+$rH=Dj$9$k!#(B
    $B85$N(B `\ifstrequal` $B$H0[$J$j40A4E83+2DG=$G$"$k$,!"(Be-TeX $B3HD%$,L58z(B
    $B$N;~$O=hM}$,Hs>o$K=E$$!#(B

($B%W%l%"%s%V%k@lMQL?Na@k8@(B)

  * `\bxPreamble<TeX$B%^%/%mDj5AL?Na(B><TeX$B%^%/%mDj5A5-=R(B>`  
  * `\bxPreamble<LaTeX$B%^%/%mDj5AL?Na(B>[*]<LaTeX$B%^%/%mDj5A5-=R(B>`  
    `\@onlypreamble` $B$r@_Dj$7$F%^%/%m$rDj5A$9$k!#(B  
    $B"((B $B<B:]$NF0:n$OC1$K(B `\bxPreamble\$B@)8fDV(BA[*]\$B@)8fDV(BB` $B$r(B  
    `\@onlypreamble\$B@)8fDV(BB \$B@)8fDV(BA[*]\$B@)8fDV(BB`  
    $B$KCV$-49$($F$$$k$@$1$G$"$k!#(B

($BJ]8nIU%^%/%mDj5A(B)

  * `\bxRobustdef<TeX$B%^%/%mDj5A5-=R(B>`  
  * `\bxRobustgdef<TeX$B%^%/%mDj5A5-=R(B>`  
  * `\bxRobustedef<TeX$B%^%/%mDj5A5-=R(B>`  
  * `\bxRobustxdef<TeX$B%^%/%mDj5A5-=R(B>`  
    $BJ]8nIU$JL?Na$rDj5A$9$k!#(Be-TeX $B3HD%$,M-8z$G$"$l$P!"(B`\protected` $B$r(B
    $BM-8z$K$7!"L58z$G$"$l$P!"(BLaTeX $B$NJ]8n5!9=$rMQ$$$k!#A0$K(B `\long` $B$r(B
    $BIU$1$i$l$k$,(B `\global` $B$OIT2D!#(B

($B$=$NB>(B)

  * `\bxIfInMovingArg{<$B??(B>}{<$B56(B>}`  
    $B$$$o$f$kF0$/0z?t(B($B<B9T$,M^;_$5$l$?4D6-(B)$B$G$"$k$+$N%F%9%H!#<B9T$,M-8z(B
    $B$G$"$k>l9g$O!"(B<$B56(B> $B$r<B9T$7$?$N$HEy2A$K$J$k!#<B9T$,M^;_$5$l$F$$$k(B
    $B>l9g$O!VL50UL#$JBeF~J8!W$N8e$K(B <$B??(B> $B$rB3$1$?$b$N$KE83+$5$l$k!#$3$N(B
    $BL?Na$O!"F0$/0z?t$NCf$G$N;HMQ$r;vA0$K8!::$7$F%(%i!<$r=P$9$H$$$&L\E*(B
    $B$rA[Dj$7$F$$$k!#(B(`\bxCheckForMovingArg` $B$b;2>H!#(B)

  * `\bxMessageToken{<$BJ8;zNs(B>}{<$B%F%-%9%H(B>}`  
    `<$B%F%-%9%H(B>` $B$NCf$N(B `#1` $B$r@)8fDV(B `\<$BJ8;zNs(B>` $B$KCV49$7$?%F%-%9%H(B
    $B$r<B9T$9$k!#(B`\<$BJ8;zNs(B>` $B$NDj5A$OJQ2=$7$J$$!#(B`<$B%F%-%9%H(B>` $BCf$G(B
    $B%Q%i%a%?(B `#1` $BEy$r;H$&>l9g$O(B `##1` $B$N$h$&$K=q$/I,MW$,$"$k!#Nc$($P(B
    $B0J2<$N$h$&$KMQ$$$k!#(B

        \bxMessageToken{Hello TeX!}{\def\dohello{\do#1}}

    `\dohello` $B$NDj5A$O(B `\do` $B$N8e$K@)8fDV!V(B`\Hello TeX!`$B!W$,B3$$$?(B
    $B$b$N$K$J$k!#(B

  * `\bxCheckForMovingArg{<$B%F%-%9%H(B>}`  
    $BF0$/0z?t$NCf$G$"$k$+$N3NG'!#F0$/0z?t$NCf$G$J$$>l9g$O(B `<$B%F%-%9%H(B>`
    $B$,<B9T$5$l$k$,!"$"$k>l9g$O<!$N$h$&$K!VL$Dj5AL?Na$N7A!W$G%(%i!<$,(B
    $BI=<($5$l$k!#$3$3$G$O!"(B`\xx@prepare` $B$NCf$G(B `\bxCheckForMovingArg`
    $B$N%F%9%H$r9T$C$F$$$k$H$9$k!#(B

        ! Undefined control sequence.
        <argument> \ ERROR: Use in wrong place!
        <*> \protected@edef\xx@example{\xx@prepare
                                                  \xx@tmpa}

    $B"((B $B<B9T$,M^;_$5$l$F$$$k>l9g$O(B `\errmessage` $B%W%j%_%F%#%V$b<B9T(B
    $B$5$l$J$$$N$G!"IaDL$K%(%i!<I=<($,$G$-$J$$$N$G$"$k!#(B  
    $B"((B `\bxIfInMovingArg` $B$rMxMQ$7$F$$$k$N$G!"$=$3$K=R$Y$i$l$F$$$k(B
    $B$h$&$K!"F0$/0z?t$G$"$k>l9g$NE83+7k2L$K$O%4%_$,;D$k!#(B

