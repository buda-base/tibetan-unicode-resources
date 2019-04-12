### Text markers (yigo)

The two characters `0F02` (༂) and `0F03` (༃) seem to have been encoded in Unicode to represent a generic yigo (text marker, usually ༄༅།) when the yigo is not the usual one and does not have a Unicode representation (see the two tables above for examples). The way to use these glyphs is with a Unicode mechanisme named *Variations Selectors* (see [Unicode FAQ](http://unicode.org/faq/vs.html) and [this doc](http://unicode.org/wg2/docs/n2468.doc)).

There are 256 of these selectors ([1](https://www.unicode.org/charts/PDF/UFE00.pdf), [2](https://www.unicode.org/charts/PDF/UE0100.pdf)), so a lot of glyphs that can be represented this way.

To use these selectors, it would be necessary to set up a registry of the variations, which does not exist for Tibetan. If such a list is made, it can be offered to the Unicode Technical Committee (UTC) as a proposal for adding to the [standardized variants](ftp://www.unicode.org/Public/12.1.0/ucd/StandardizedVariants-12.1.0d1.txt).

For instance if we consider the two yigo of the tables above, if they were registered we could encode them as `0F03 FE00` and `0F03 FE01`.

Encoding the yigo in such a way is more secure than defining glyphs in the Private Use Area (PUA, as proposed by the [EWTS spec](http://www.thlib.org/reference/transliteration/#!essay=/thl/ewts/7/)) in that it incorporates the semantic of the base glyph and then indexes a variant of that in plain text. Wheras the PUA is completely arbitrary and dependent entirely on the font used to image the data. This is vulnerable to other fonts assigning the same code point to completely different scripts. So if the font is lost, the plain text data with Variants is much less corrupted than plain text data containing PUA characters. This is better for plain text archives, databases, searching, etc.

#### Terma and non-terma

The character `0F02` (༂) is a placeholder for a non-terma yigo while `0F03` (༃) is a placeholder for a terma yigo.

##### Non-tema yigo

Here is a list of non-terma yigo :

![non-terma yigo 1](images/ntyigo1.png?raw=true) (in [འབྲི་གུང་བཀའ་བརྒྱུད་ཆོས་མཛོད་ཆེན་མོ།](http://tbrc.org/link?RID=W00JW501203))

![non-terma yigo 2](images/ntyigo2.jpg?raw=true) (in The Description of Dzongkha Letters, 1985)