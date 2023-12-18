# Unencoded Characters

This file lists characters appearing in Tibetan texts that cannot currently be represented by Unicode at all.

#### Sanskrit syllable length notation

The translation of a [Sanskrit prosody](https://en.wikipedia.org/wiki/Sanskrit_prosody) treatise is using a specific representation of syllable weight (light/heavy , laghu/guru) notation that differs slightly from the Devanagari one:

![syllable length notation](images/metrics.png?raw=true)

(Derge Tengyur, vol. 197, p. 361a et seq.)

In this case, we propose to use the Devanagari equivalents:
- `093D` (ऽ) for heavy syllable (`093D 0902`, ऽं when with anusvara)
- `0964` (।) for light syllable (`0964 0902`, ।ं when with anusvara)

These signs are, to the best of our knowledge, only found in Sanskrit prosody treatises, there is no equivalent for the Tibetan language.

### Terma and shorthands

For terma and shorthand characters, see the dedicated pages:
- [terma-scripts.md](terma-scripts.md)
- [shorthands/](shorthands/)

### Reversed shabkyu

The reversed shabkyu seems to be extremely rare and only a matter of style but can be found, for instance in

![what](images/what.png?raw=true)

coming from the Namgyal Canonical manuscripts (W2KG229028, volume 28, image 199).