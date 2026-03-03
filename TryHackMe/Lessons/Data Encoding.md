- Characters are just numbers with agreed meanings. That agreement is called an encoding.
- Representation is the idea that data lives as bits and numbers in memory.
- At the same time, encoding is the specific, agreed-upon mapping between numbers and meanings, such as which number corresponds to the character "A".
- In text, each character is assigned a numeric code.

## ASCII
- ASCII stands for American Standard Code for Information Interchange and it is an early character encoding from 1963 that uises numbers 0-127 to represent English letters, digits, punctuations and some control characters. It was limited to seven bits.
- It is uncommon to use decimal digits. It is more common to use hexadecimal digits when we want to show the bits.
- ASCII only uses 7 bits.
- THe ISO/IEC 8859 Series created several standards, each covering a set of languages.
  - ISO-8859-1 - Covers Western European Languages
  - ISO-8859-2 - Covers Central/Eastern European Languages

## Unicode
- A universal character encoding standard. It assigns a unique code points to characters from all modern and historical writing systems worldwide.
- Supports the interchange, processing and display of text in diverse languages.
- It assigns a unique number to every character across all languages.
  
    U+0041 = Latin “A”
    U+03A9 = Greek “Ω”
    U+3042 = Japanese Hiragana “あ”

### UTF-8, UTF-16, and UTF-32
- Common on the modern web. It encodes Unicode points into 1 to 4 bytes dynamically.
- It decides on the number of bytes based on the character complexity.
- It allows to cover the Unicode standard without wasting bytes.
- UTF-16 uses either 2 or 4 bytes per character. Some rares or more complex characters, such as emoji, require a pair, two 16-bit units totaling 4 bytes. A is encoded as U+0041, while the emoji 🔥 needs two and is encoded as U+D83D U+DD25
- UTF-322 is the simplest but also the most wasteful. Every Unicode code point uses exactly 4 bytes. For example, A is encoded as U+00000041 and 🔥 is encoded as U+0001F525
