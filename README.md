# RegEx Examples

Regular expressions, commonly known as RegEx, are powerful tools for pattern matching in strings. They allow developers to define search patterns with flexibility and precision. In this guide, we'll explore the basics of RegEx, covering general syntax, flags, anchors, word boundaries, metacharacters, and provide practical examples.

## RegEx Refresher

### General

A regular expression is enclosed within slashes (`/.../`). Flags can be added to modify the search behavior. For instance, `/pattern/gi` indicates a global search with case insensitivity.

### Flags

- **g (global)**: Searches for all matches in a string.
- **i (insensitive)**: Enables case-insensitive search.
- **m (multiline)**: Matches the beginning or end of each line.
- **u (Unicode)**: Enables full Unicode matching.
- **s (any whitespace)**: Matches spaces, line breaks, and tabs.
- **S (non-whitespace)**: Matches any non-whitespace character.
- **n (line feed)**: Matches line feed characters.

### Anchors

- **^ (caret)**: Used to start searching at the beginning of a line or string.
- **$ (dollar)**: Used to start searching at the end of a line or string.

### Word Boundaries

- **\b (word boundary)**: Matches the start, end, or whole word.
  - **\bhello\b**: Finds the whole word "hello" surrounded by whitespace or punctuation.
  - **\bhello**: Finds words beginning with "hello."
  - **hello\b**: Finds words ending with "hello."

- **\B (non-word boundary)**: Opposite of \b.
  - **\Bhello\B**: Finds nothing when "hello" is surrounded by whitespace.
  - **\Bell\B**: Matches "ell" in "hello" surrounded by letters.
  - **\Bello\B**: Matches "ello" in "hello" because it starts with another letter.
  - **\Bhell\B**: Matches "hell" in "hello" because it ends with another letter.

## Metacharacters

### Single Character Metacharacters

*To be added*

### Double Character Metacharacters

*To be added*

## Useful Examples

### Replace the Last n Characters of a String

To replace the last *n* characters of a string, use `.{n}$`.

For example, applying `.{4}$` to the string **This is a test!** changes it to **This is a t**.

---

In conclusion, mastering regular expressions empowers developers to perform intricate string manipulations efficiently. This guide covers the fundamentals, including syntax, flags, anchors, and word boundaries, providing a solid foundation for leveraging the full potential of RegEx in JavaScript.