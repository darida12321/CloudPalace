A way of representing text in [[Binary|binary]]. Since [[ASCII]] only uses 7 bits, people realized that an additional 128 characters could be defined if a full byte is used per character. However, this led to a lot of different standards (e.g.: `IBM PC`: Math and Latin symbols, `KOI-8`: Cyrillic letters).

**ANSI** (American National Standards Institute) was a solution to all these differing standards. It introduced the concept of a **code page**. Depending on which **code page** was in use, the operating system would display text differently.
- `1250`: Western Europe. (ñ)
- `1251`: Cyrillic. (п)
- `1253`: Greek. (Ψ)
A full list is available [here](https://en.wikipedia.org/wiki/Code_page).

However this had its own problems:
- Switching **code pages** is painful.
- Languages like Chinese and Japanese didn't fit in 8 bits.