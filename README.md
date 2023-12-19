# RegEx Examples

Regular expressions, commonly known as RegEx, are powerful tools for pattern matching in strings. They allow developers to define search patterns with flexibility and precision. In this guide, we'll explore the basics of RegEx, covering general syntax, flags, anchors, word boundaries, metacharacters, and provide practical examples.

## RegEx Refresher

### General

A regular expression is enclosed within slashes (`/.../`). Flags can be added to modify the search behaviour. For instance, `/pattern/gi` indicates a global search with case insensitivity.

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

Here are some commonly used single character metacharacters:

1. **`.` (Dot):** Matches any single character except for line terminators.
   - Example: `/a.c/` matches "abc," "adc," etc.

2. **`\d`:** Matches any digit (0-9).
   - Example: `/a\dc/` matches "a1c," "a2c," etc.

3. **`\D`:** Matches any non-digit.
   - Example: `/a\Dc/` matches "abc," "a#c," etc.

4. **`\w`:** Matches any word character (alphanumeric + underscore).
   - Example: `/a\wc/` matches "a1c," "a_c," etc.

5. **`\W`:** Matches any non-word character.
   - Example: `/a\Wc/` matches "a#c," "a$c," etc.

6. **`\s`:** Matches any whitespace character (space, tab, line feed).
   - Example: `/a\sc/` matches "a c," "a\tc," etc.

7. **`\S`:** Matches any non-whitespace character.
   - Example: `/a\Sc/` matches "a#c," "a$c," etc.

8. **`[...]`:** Character class. Matches any single character within the brackets.
   - Example: `/gr[aeiou]p/` matches "grape," "grip," etc.

9. **`[^...]`:** Negated character class. Matches any single character not within the brackets.
   - Example: `/gr[^aeiou]p/` matches "grip" but not "grape."

These metacharacters provide flexibility in specifying patterns for single characters in regular expressions. You can mix and match them to create complex patterns based on your requirements.

### Double Character Metacharacters

These combinations enable you to express more complex patterns in regular expressions. Here are some commonly used double character metacharacters:

1. **`*`:** Matches zero or more occurrences of the preceding character or group.
   - Example: `/ab*c/` matches "ac," "abc," "abbc," etc.

2. **`+`:** Matches one or more occurrences of the preceding character or group.
   - Example: `/ab+c/` matches "abc," "abbc," etc., but not "ac."

3. **`?`:** Matches zero or one occurrence of the preceding character or group.
   - Example: `/ab?c/` matches "ac" and "abc."

4. **`{n}`:** Matches exactly n occurrences of the preceding character or group.
   - Example: `/ab{2}c/` matches "abbc" but not "abc" or "ac."

5. **`{n,}`:** Matches n or more occurrences of the preceding character or group.
   - Example: `/ab{2,}c/` matches "abbc," "abbbc," etc.

6. **`{n,m}`:** Matches between n and m occurrences of the preceding character or group.
   - Example: `/ab{2,4}c/` matches "abbc," "abbbc," and "abbbbc" but not "abc" or "ac."

7. **`|`:** Alternation. Matches either the pattern on the left or the pattern on the right.
   - Example: `/cat|dog/` matches "cat" or "dog."

8. **`(...)`:** Capturing group. Groups patterns together and captures the matched result.
   - Example: `/(ab)+c/` matches "abc" and "ababc."

These double character metacharacters provide ways to specify the quantity and alternation of characters or groups within a regular expression. They add expressive power to regex patterns, allowing for more sophisticated matching conditions.

## Useful Examples

### Replace the Last n Characters of a String

To replace the last *n* characters of a string, use `.{n}$`.

For example, applying `.{4}$` to the string **This is a test!** changes it to **This is a t**.

---

In conclusion, mastering regular expressions empowers developers to perform intricate string manipulations efficiently. This guide covers the fundamentals, including syntax, flags, anchors, and word boundaries, providing a solid foundation for leveraging the full potential of RegEx in JavaScript.