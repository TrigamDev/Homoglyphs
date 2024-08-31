# Usage
Simply download the `homoglyphs.json` to be parsed and used in your project
# Why?
Homoglyphs are unicode characters that, while looking like the original character, are a different unicode value, and therefore isn't treated the same as the original. For example, though 'a' and 'α' look similar, they are entirely different unicode characters.

Along with casuing confusion, homoglyphs can cause many problems among websites and software. If, for example, a website wanted to blacklist certain words, replacing one or more of the letters with a homoglyph could cause the word to not match the blacklist and not be filtered out. Homoglyphs can also cause text rendering to appear awkward and inconsistent in some cases.

Therefore, I've compiled a database of all the homoglyphs I can find to make working with homoglyphs easier and to help others working with them have a more complete list of them. This database of homoglyphs is based on [Wikipedia: List of Unicode Characters](https://en.wikipedia.org/wiki/List_of_Unicode_characters), [Unicode Letter Variants](http://www.gilfusion.com/unicode/variants.aspx), and [codebox/homoglyph](https://github.com/codebox/homoglyph).
# Format
`homoglyphs.json` is split into two objects: `characters` for the string representation of the characters, and `unicode` for the unicode value of the characters.

Each object is split into different objects based on the base character being checked against (`a`, `b`, `c`, etc).
Each character consists of multiple arrays:
- `variants` contains variants of the base character (ɑ, ɐ, etc).
- `diacritic` contains diacritical and accent variations of the character (á, â, ą, etc).
- `fonts` contains font style variations of the character (𝐚, 𝑎, 𝕒, ａ, etc).
- `numbers` contains numbers that look similar to the character (such as 4).
- `other` contains unicode characters that don't fit well into the other categories.
