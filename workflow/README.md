# Using Jig in word-level transliteration and tone display

## Word-level transliteration

Jig can be used in rule-based transliteration of tonal languages, with the help of:

* a lexicon with word-to-romanization mapping
* a defined Jig schema for the language
* Input of segmented text (or a preliminary word-segmentor implemented by longest-string matching algorithm)

The Jig schema instructs the program how to select the right tonal allophone.


## Add tonal allophones

Given an array of words in this format, add an additional field to the object that indicates the tonal label of each syllable.

**Example 1 (Hong Kong Hakka)** The first syllable is 
```json
{
    "level": "w",
    "lemma": "阿僬",
    "children": [
        { "level": "m", "lemma": "阿", "rom": "á",    "rom_alphanum": "a1" },
        { "level": "m", "lemma": "僬", "rom": "ziāu", "rom_alphanum": "ziau2" },
    ]
}
```

**To this**
```json
{
    "level": "w",
    "lemma": "阿僬",
    "children": [
        { "level": "m", "lemma": "阿", "rom": "á",    "rom_alphanum": "a1"    , "tone": "t1x"},
        { "level": "m", "lemma": "僬", "rom": "ziāu", "rom_alphanum": "ziau2" , "tone": "t2"}
    ]
}
```

## Tone Display

This JSON below will be passed to the system.

```json
{
    "level": "w",
    "lemma": "阿僬",
    "children": [
        { "level": "m", "content": "阿", "rom": "á",    "rom_alphanum": "a1"    , "tone": "t1x"},
        { "level": "m", "content": "僬", "rom": "ziāu", "rom_alphanum": "ziau2" , "tone": "t2"}
    ]
}
```

```xml
<w lemma="阿僬">
<m lemma="阿", rom="á", rom_alphanum="a1" tone="t1x">阿</m>
<m lemma="僬", rom="ziāu", rom_alphanum="ziau2" tone="t2">僬</m>
</w>
```

This which will be displayed according to values specified in the layout json.



