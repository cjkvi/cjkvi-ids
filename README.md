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

## Encoding Policies

* Compatibility ideographs whose IDS is not equal to corresponding
  unified ideographs may be used as DC.

* Following non-ideographs may be used as DCs (for now).
  "αℓ△⺀⺄⺆⺈⺊⺌⺍⺶⺸⺻⺼〇〢キサ㇀㇉㇢"

* Encircled numerics ① ～ ⑳ represents unencoded DCs. Number denotes
  its stroke count. This would be useful when calculating total
  strokes of ideographs.

* '&CDP-XXXX;' entity reference notation (CDP stands for "Chinese
  Document Processing lab") is inherited from [CHISE
  project](http://www.chise.org). For details of usable entity
  references, refer [an article on
  CDP](http://glyphwiki.org/wiki/Group:CDP%E5%A4%96%E5%AD%97) at
  GlyphWiki. They can be converted to Unicode BMP PUA (Privae Use
  Area) characters by Microsoft [Big5 to PUA conversion
  table](http://kanji-database.sourceforge.net/charcode/big5.html),
  and HanaMinAFDKO Font support these glyphs in PUA.

* Compatibility ideographs, whose IDS is not equal to its
  corresponding unified ideographs, may be used as DCs. (e.g. ⻀)

* IDS of compatibility ideographs may sometimes have compatibility
  ideographs as DCs, by mean of clarifying the difference of their
  structures compared with corresponding unified ideographs.

* "G", "T", "J", "K", "V", etc. signs with brackets after IDS indicate
  that such IDS is specific to each columns of UCS code charts. "A"
  indicates AJ1-6 shapes, and "X" indicates virtual shape that is not
  actually appeared in the UCS specification, but possibly matches to
  that code points according to Annex S of UCS. Many of them appear
  in Japanese dictionaries such as Dai-Kanwa Jiten.

## Licenses

* 'ids.txt' is derived from [CHISE project](http://www.chise.org/).
  License follows their terms.

* All other data are distributed uner GPLv2.

## Author

* [kawabata](https://github.com/kawabata)
