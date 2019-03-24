# Best practices for Unicode Encoding

In some cases the same form can be represented by different non-equivalent Unicode character sequences:

### oM, 0F02, 0F03

These characters are composed characters that are not equivalent to their decomposition:

- `0F00` (ༀ) is not equivalent to `0F68 0F7C 0F7E` (ཨོཾ)
- `0F02` (༂) is not equivalent to `0F60 0F74 0F82 0F7F` (འུྂཿ)
- `0F03` (༃) is not equivalent to `0F60 0F74 0F82 0F14` (འུྂ༔)

See [this deprecation proposal](https://www.unicode.org/L2/L2018/18078-tibetan-depr.pdf) for more info, and [http://www.unicode.org/L2/L2018/18241-script-ad-hoc.pdf](the answer) (p.21).

In these cases, we propose to always use the decomposed form instead of the precomposed one.

### R

In some combinations, a superscribed ra (*rago*) traditionally keeps its full form instead of being shortened. This is the case of:
- `རྱ`
- `རྙ`
- `རླ`

In these cases we propose to use `\u0F62` instead of `\u0F6A`. So the proposed best practice is to use:
 - `\u0F62\u0FB1` (`རྱ`) instead of `\u0F6A\u0FB1` (`ཪྱ`)
 - `\u0F62\u0F99` (`རྙ`) instead of `\u0F6A\u0F99` (`ཪྙ`)
 - `\u0F62\u0FB3` (`རླ`) instead of `\u0F6A\u0FB3` (`ཪླ`)

For all other (rare) forms where the superscribed ra keeps its full form, we propose to always use `\u0F6A`. This includes `\u0F6A\u0FBB` (`ཪྻ`) for instance.

