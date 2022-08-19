# RegEx Examples

## RegEx Refresher

### General

**/**...**/** shows that this is a pattern

**/**...**/gi** shows that this is a pattern **with flags**

### Flags

**g** = **global**: the search will return all matches

**i** = **insensitive**: the search is case insensitive. For example, *hello*, *Hello*, and *HeLlO* are equal when the **i** flag is used

**m** = **multiline**

**u** = **Unicode**

**s** = **any whitespace character**: the search matches **spaces**, **line breaks**, and **tables**

**S** = **any non-whitespace character**

**n** = **line feed character**

### Anchors

**^** is used to start searching at the **beginning** of a line or string

**$** is used to start searching at the **end** of a line or string

### Word Boundaries

**\b** is used to match the start of a word, the end of a word, or a whole word. For example:

- **\bhello\b** will find the whole word *hello* as long as it's surrounded by whitespace characters or punctuation
- **\bhello** will find all words that **begin** with *hello* (for example, *hellomynameis...*)
- **hello\b** will find all words that **end** with *hello* (for example, *mynameishello*)

**\B** is the opposite of **\b**. For example:

- **\Bhello\B** will find nothing when searching the line *hello my name is...*. This is because the word is surrounded by whitespace characters
- **\Bell\B** will match the *ell* in *hello* because it's surrounded by letters
- **\Bello\B** will match the *ello* in *hello* because it **starts** with another letter
- **\Bhell\B** will match the *hell* in *hello* because it **ends** with another letter

## Metacharacters

### Single Character Metacharacters

*To be added*

### Double Character Metacharacters

*To be added*

## Useful Examples

### Replace the last n characters of a string

To replace the last *n* characters of a string, use `.{n}$`

For example, if you use `.{4}$` on the string **This is a test!**, the string will change to **This is a t**.
