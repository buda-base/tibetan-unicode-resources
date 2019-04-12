# Terma scripts

### General considerations

Some terma cycles use specific letter shapes instead of regular ones, for instance in:

![terma script](images/terma-script.png?raw=true)

Some translation tables between the terma scripts and the regular Tibetan script exist, see for instance:
- [table 1](https://www.tbrc.org/browser/ImageService?work=W1KG4941&igroup=I1KG5056&image=194&first=1&last=590&fetchimg=yes)
- [table 2](https://www.tbrc.org/browser/ImageService?work=W1KG4941&igroup=I1KG5056&image=196&first=1&last=590&fetchimg=yes)

coming from a calligraphy manual named [ཡིག་རིགས་བརྒྱ་ཡི་མ་ཕྱི་འཛམ་གླིང་མཁས་དགུའི་མཛེས་རྒྱན་ཕྱོགས་ལས་རྣམ་རྒྱལ།](http://tbrc.org/link?RID=W1KG4941).

In this case the Unicode encoding is quite unclear. This looks more than a font problem than an encoding problem. One possibility would be to encode each terma script using Variations Selectors (see [text-markers.md](text-markers.md)).