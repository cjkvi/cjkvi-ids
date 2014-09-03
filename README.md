IDS data
========

This is a collection of various IDS (Ideographic Description Sequence)
data.

## Description

IDS (Ideographic Description Sequence) is quite important information
for ideographs. Among thousands of ideographs encoded, such data can
be an useful clue to identify them.

However, as there may be ambiguity for encoding IDS, some tools to
normalize and identify the ideographs would be important.
[IDS tool](http://github.com/kawabata/ids) is one of such example.

## Encoding Policies

There are some encoding policies for IDS.

* Compatibility ideographs whose IDS is not equal to corresponding
  unified ideographs may be used as DC.

* Following non-ideographs may be used as DCs (for now).
  "αℓ△⺀⺄⺆⺈⺊⺌⺍⺶⺸⺻⺼〇〢キサ㇀㇉㇢"

* Encircled numerics ① ～ ⑳ represents unencoded DCs. Number denotes
  its stroke count. This would be useful when calculating total
  strokes of ideographs.

* '&CDP-XXXX;' notation (Chinese Document Processing Lab) is derived
  from CHISE project. For details of useable glyph, refer
  [CDP article](http://glyphwiki.org/wiki/Group:CDP%E5%A4%96%E5%AD%97)
  of GlyphWiki. They can be converted to Unicode PUAs by using
  Microsoft Big5 conversion table.

* Compatibility charactes whose IDS is not equal to its corresponding
  unified ideographs may be used as DCs.

* IDS of compatibility ideographs may sometimes have compatible
  ideographs as DCs by mean of clarifying the difference of its
  structure compared with corresponding unified ideograph.

## Licenses

* 'ids.txt' is derived from [CHISE project](http://www.chise.org/).
  License follows their terms.

* All other data are distributed uner GPLv2.

## Author

* [kawabata](https://github.com/kawabata)
