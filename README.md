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

However, there may be ambiguity in encoding IDS. Therefore, tools to
normalize IDS and identify the ideographs are important.
[IDS tool](http://github.com/kawabata/ids) is one such example.

Also, IDS sequences use the full range of CJK ideographs, so fonts
that cover all encoded ideographs (such
as [HanaMin](http://fonts.jp/hanazono/)
or [Hanamin AFDKO](https://github.com/cjkvi/HanaMinAFDKO/releases) )
should be used.

## Encoding Policies

* Compatibility ideographs, whose IDSes are not equal to their
  corresponding unified ideographs, may be used as DCs. When there are
  multiple compatibility ideographs with the same IDS, then the one
  with a smaller character code will be used. (e.g.
  ⻀,並,荒,冗,叟,切,巢,廾,戛,桒,甾,𤾡,舁,蕤,貫,黾)

* The following non-ideographs may be used as DCs (for now).
  "αℓ△⺀⺄⺆⺈⺊⺌⺍⺶⺸⺻⺼〇〢キサ㇀㇉㇢㇞"

* Encircled numerics ① ～ ⑳ represent unencoded DCs. The number denotes
  its stroke count. This is useful when calculating total
  stroke counts of ideographs. Such a convention does not conform with the
  Annex I of ISO/IEC 10646, so please replace them with the wildcard
  character `？' (U+FF1F) if you need strict conformance with the
  UCS standard.

* IDS data files with name postfix "*-cdp.txt" adopt PUA characters
  from [CDP](https://www.sinica.edu.tw/~cdp) (CDP stands for "Chinese
  Document Processing lab" at Academia Sinica) as DCs. They are
  denoted as entity references like "&CDP-xxxx;".

  At the end of "ids-cdp.txt", mappings between PUA DCs and CDP
  references are enumerated. For details of usable PUA characters,
  refer to
  [an article on CDP](http://glyphwiki.org/wiki/Group:CDP%E5%A4%96%E5%AD%97) at
  GlyphWiki. CDP's hexadecmail numbers and Unicode BMP PUA character
  codepoints relationship is based on EUDC codepoints defined by by
  Microsoft
  [Big5 to PUA conversion table](http://kanji-database.sourceforge.net/charcode/big5.html).
  HanaMinAFDKO Font supports these glyphs in PUA.

* IDS of compatibility ideographs may sometimes have compatibility
  ideographs as DCs, by means of clarifying the difference of their
  structures compared with corresponding unified ideographs.

* "G", "T", "J", "K", "V", etc. signs with brackets after IDS indicate
  that such IDS is specific to each columns of UCS code charts. "A"
  indicates AJ1-6 shapes, and "X" indicates a virtual shape that does not
  actually appear in the UCS specification, but possibly matches 
  that code points according to the Annex S of UCS. Some such
  shapes may appear in OS-equipped fonts such as MingLiu, MS-Mincho or
  SimSun, or famous dictionaries such as "Dai Kanwa Jiten". "O"
  indicates "obsolete", that once appeared in an older edition of the
  UCS standard, but no longer.

## Licenses

* 'ids.txt' is derived from the [CHISE project](http://www.chise.org/).
  License follows their terms. 'ids-ext-cde.txt' is not directly based
  on [CHISE project](http://www.chise.org/), and is not restricted to the
  GPLv2 license.

* All other data are distributed under GPLv2.

## Author

* [kawabata](https://github.com/kawabata)
