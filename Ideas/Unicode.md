A way of assigning a [[Binary|binary]] value to text. Given [[ANSI]]'s problems, people wanted to create a **universal encoding** where every character of every language could be represented.

This was a huge undertaking, as languages are very diverse. You need to represent:
- Chinese where characters are not always in separate spaces.
- Arabic or Hindi, the direction of writing is reversed.
- Letters with accents, or letters from different languages that look very similar.
- Special symbols, punctuation, emojis, etc.

Each character gets a code point `U+1234`, where the number is [[Hexadecimal|hexadecimal]]. These are listed [here](https://home.unicode.org/). (e.g. `U+1F60A: 😊`, `U+0041: A`)

Here are some interesting features:
- The first 128 characters match [[ASCII]]'s definition.
- You can combine characters (`U+0301: combining acute accent`)
	- `U+0065: e`, `U+0065 U+0301: é`, `U+00E9: é`
	- These modifiers can be stacked
- Over one million **code points** are defined.

While **unicode** defines the values for symbols, it doesn't define how it should be encoded. That's a task for [[UTF-8]], [[UTF-16]] and [[UTF-32]].