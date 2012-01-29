Konjac Dictionaries
===================

These are just some dictionaries I've added for use with
[Konjac](https://github.com/brymck/konjac). They're mostly designed to clean up
formatting and automate some of the most obvious conversions I know between the
two languages I know, Japanese and English. The files available are:

  * **alphanumeric.yml** - One-way conversion of full-width letters and numbers to
    half-width letters and numbers (e.g. `Ｎｏｖ１９８４ #=> Nov1984`)
  * **kana.yml** - One-way conversion of half-width katakana to full-width
    katakana (e.g. `ﾊﾞｯｸｱｯﾌﾟ #=> バックアップ`)      
  * **punctuation.yml** - Two-way conversion of kanji-style full-width
    punctuation to Western style half-width punctuation

Installation
------------

```bash
git clone git://github.com/brymck/konjac_yml.git
cp konjac_yml/*.yml ~/.konjac
```

Usage
-----

Convert all full-width alphanumeric characters in a Japanese plain-text to half-width:

```bash
konjac translate input.txt -o output.txt -f ja -t en -u alphanumeric
```

Convert using the alphanumeric, kana and punctuation dictionaries:

```bash
konjac translate input.txt -o output.txt -f ja -t en -u alphanumeric -u kana -u punctuation
```
