# Edge cases

This file lists cases that can be encoded in Unicode but in an unsatisfying way.

### Cases not respecting reordering

In some cases an achung (`0F71`) appears before a subscribed ya (`0FB1`):

![0FB0 0FB1](images/0fb00fb1.png?raw=true)

(Derge Kangyur, vol. 87, p. 218a). 

In some other cases it appears after a shabkyu (0F74):

![shabkyu achung](images/Kv40p70b.png?raw=true)

(Derge Kangyur, vol. 40, p. 70b, l. 1)

These pose a rendering problem because layout system will reorder characters in a way defined by Unicode, and will reorder:
- `0F71 0FB1` into `0FB1 0F71`, so that the yata gets before the achung
- `0F74 0F71` into `0F71 0F74`, so that the achung get before the shabkyu

The description of 0FB0 in the [Unicode Chart](https://unicode.org/charts/PDF/U0F00.pdf) doesn't seem to correspond to the form we encounter, as it states *only used for full-sized subjoined letter*, while in our case this is clearly not a full formed letter, but a regular small achung.