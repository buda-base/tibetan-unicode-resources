# Edge cases

This file lists cases that can be encoded in Unicode but in an unsatisfying way.

### Cases not respecting reordering

In some cases an achung (`0F71`) appears before a subscribed ya (`0FB1`):

![0FB0 0FB1](images/0fb00fb1.png?raw=true)

(Derge Kangyur, vol. 87, p. 218a). 

This poses a rendering problem because layout system will reorder characters in a way defined by Unicode, and will reorder `0F71 0FB1` into `0FB1 0F71`, so that the yata gets before the achung. 

The description of 0FB0 in the [Unicode Chart](https://unicode.org/charts/PDF/U0F00.pdf) doesn't seem to correspond to the form we encounter, as it states *only used for full-sized subjoined letter*, while in our case this is clearly not a full formed letter, but a regular small achung.

### Shortened sa

Some manuscripts use a shortcut for the `གས` suffix by using a special subscript form of sa, see for instance Lhasa Kangyur, vol. 1, p. 8:

![0FB0 0FB1](images/0fb00fb1.png?raw=true)

This special form of sbuscript sa is clearly distinct from the regular subscript sa (0FB6). There is not way to distinguish the two forms in Unicode.

### Characters advertised on THL

See the [THL page on unencoded characters](http://www.thlib.org/reference/transliteration/#!essay=/thl/ewts/7/).