Computers use [[Binary|binary]] to store information, so we need a way of representing text in [[Binary|binary]]. This is often a trade-off between compactness and representation, plus there is a fair bit of history behind how and why the representations developed.

`1960`: The first and simplest system, [[ASCII|ASCII]] was created. It used 7 bits to represent every English symbol, and some control characters. However, computers use 8 bit bytes, where an additional 128 characters could be stored. 

`1980`: More and more agencies designed their own [[ASCII|ASCII]] extensions. Some examples are:
- `ISO-8859-1` - `ISO-8859-15` Encodings specialized for different parts of Europe.
- `IBM PC`: Used for expressing math, and other European accented letters.
- `KOI-8`: Contains Russian Cyrillic letters.
This quickly became unmanageable, so [[ANSI|ANSI]] was introduced. It created a **code page** identifier that operating systems can use. For example, `Windows-1252` is still a commonly used **code page** containing most western characters.

`1990`: **Code pages** were hard to switch, and simply couldn't contain some languages such as Japanese or Chinese. An agency decided that they want to create a uniform encoding of every symbol humans write, and created [[Unicode|Unicode]].
However, [[Unicode|Unicode]] simply assigns a value to each symbol, and doesn't specify how to store text. For that, the [[UTF-16]] and [[UTF-32]] were used.

`2000`: Both [[UTF-16]] and [[UTF-32]] had some downsides. They were not backwards-compatible with [[ASCII]], and wasted a lot of space for most texts. As a result, [[UTF-8]] was created. It addressed basically every problem, and is still the most widely used text representation to this day.
