IDS data
========

This is a collection of various IDS (Ideographic Description Sequence)
data.

## Description

IDS (Ideographic Description Sequence) is a way to describe the
structure of CJK Unified ideographs.

The IDS consists of IDCs (Ideographic Description Characters), namely
"⿰" (U+2FF0) to "⿻" (U+2FFB), and DCs (Description Characters), that
are usually ideographs.

IDS is quite important information for ideographs, as it may be
possible to identify ideographs from them.

However, there may be ambiguity for encoding IDS. Therefore, tools to
normalize IDS and identify the ideographs would be important.
[IDS tool](http://github.com/kawabata/ids) is one of such example.

Also, IDS sequences use full range of CJK ideographs, so the fonts
that covers all encoded ideographs (such
as [HanaMin](http://fonts.jp/hanazono/)
or [Hanamin AFDKO](https://github.com/cjkvi/HanaMinAFDKO/releases) )
should be used.

## Encoding Policies

* Compatibility ideographs, whose IDSes are not equal to their
  corresponding unified ideographs, may be used as DCs. When there are
  multiple compatibility ideographs with the same IDS, then the one
  with smaller character code will be used. (e.g.
  ⻀,並,荒,冗,叟,切,巢,廾,戛,桒,甾,𤾡,舁,蕤,貫,黾)

* Following non-ideographs may be used as DCs (for now).
  "αℓ△⺀⺄⺆⺈⺊⺌⺍⺶⺸⺻⺼〇〢キサ㇀㇉㇢㇞"

* Encircled numerics ① ～ ⑳ represents unencoded DCs. Number denotes
  its stroke count. This would be useful when calculating total
  strokes of ideographs. Such convention does not conform with the
  Annex I of ISO/IEC 10646, so please replace them with wildcard
  character `？' (U+FF1F) if you need a strict conformance with the
  UCS standard.

* IDS data file with name postfix "*-cdp.txt" adopts PUA characters
  from [CDP](https://www.sinica.edu.tw/~cdp) (CDP stands for "Chinese
  Document Processing lab" at Academia Sinica) as DCs. They are
  deonted as entity reference like "&CDP-xxxx;".

  At the end of "ids-cdp.txt", mappings between PUA DCs and CDP
  references are enumerated. For details of usable PUA characters,
  refer
  [an article on CDP](http://glyphwiki.org/wiki/Group:CDP%E5%A4%96%E5%AD%97) at
  GlyphWiki. CDP's hexadecmail numbers and Unicode BMP PUA character
  codepoints relationship is based on EUDC codepoints defined by by
  Microsoft
  [Big5 to PUA conversion table](http://kanji-database.sourceforge.net/charcode/big5.html).
  HanaMinAFDKO Font supports these glyphs in PUA.

* IDS of compatibility ideographs may sometimes have compatibility
  ideographs as DCs, by mean of clarifying the difference of their
  structures compared with corresponding unified ideographs.

* "G", "T", "J", "K", "V", etc. signs with brackets after IDS indicate
  that such IDS is specific to each columns of UCS code charts. "A"
  indicates AJ1-6 shapes, and "X" indicates virtual shape that is not
  actually appeared in the UCS specification, but possibly matches to
  that code points according to the Annex S of UCS. Some of such
  shapes may appear in OS-equipped fonts such as MingLiu, MS-Mincho or
  SimSun, or famous dictionaries such as "Dai Kanwa Jiten". "O"
  indicates "obsolete", that was once appeared in older edition of the
  UCS standard, but no longer.

## Licenses

* 'ids.txt' is derived from [CHISE project](http://www.chise.org/).
  License follows their terms. 'ids-ext-cde.txt' is not directly based
  on [CHISE project](http://www.chise.org/), and is not restricted to
  GPLv2 license.

* All other data are distributed uner GPLv2.

## Author

* [kawabata](https://github.com/kawabata)
