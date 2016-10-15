## ip6words

Converts IPv6 addresses to and from a user friendly format using words.

#### Usage

```bash
$ python ip6words.py 2001:0db8:85a3:08d3:1319:8a2e:0370:7348
selecting.exporters.passively.players.rings.rustled.birds.consumable

$ python ip6words.py selecting.exporters.passively.players.rings.rustled.birds.consumable
2001:0db8:85a3:08d3:1319:8a2e:0370:7348

$ python ip6words.py -h
Usage:
        python ip6words.py ([-h] | [-d] | [-u]) (<ip6words-address-to-convert> | <ipv6-to-convert>)
         [-h] ~ This dialog
         [-u] ~ The usage dialog
         [-d] ~ Delete the dilled (pickled) word list in order to regenerate it before executing
```

#### Requirements

- Python 3.3+ (NOT tested at all on Python 2)
- nltk (*will download these packages on first run if you do not have them already, download them yourself beforehand if you'd like to choose the download directory*)
 + words - \*optional ~ see note #3
 + brown - \*optional ~ see note #3
 + abc - \*optional ~ see note #3
 + inaugural - \*optional ~ see note #3
 + genesis - \*optional ~ see note #3
- dill


#### Notes

1. This is designed to have the same words always point to the same IP and vice versa. The only thing that
would alter this would be a change in the base nltk data, causing a shift in the frequency of words.
2. Included with this tool is a dilled (or pickled) word list. If you wish to re-generate that dill you
must delete the file or run using the \[-d] argument.
3. In practice, this means you will actually never have to download the nltk packages yourself if you never
use the \[-d] argument and thus always load the wordlist from the dill.