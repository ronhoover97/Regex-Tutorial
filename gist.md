# URL Matching with Regex in JavaScript

This guide will show you how to use regular expressions (Regex) for URL matching in JavaScript, a key skill in computer science that can aid developers of all levels. The tutorial breaks down the regex into smaller, digestible pieces to help understand.

Example Regex URL - `^(https?://)?([\da-z.-]+)\.([a-z.]{2,6})([/\w .-]*)/?$`

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Escapes](#character-escapes)

## Regex Components

### Anchors

Anchors are special characters that mark the start (`^`) and end (`$`) of a regex pattern, ensuring the URL matches the defined structure. In our regex, `^(https?://)?([\da-z.-]+)\.([a-z.]{2,6})([/\w .-]*)/?$`, everything between `^` and `$` forms the match criteria.

### Quantifiers

Quantifiers define the number of times a part of the regex should repeat. In our regex:

- `?` makes the preceding element optional.
- `+` requires the preceding element to appear at least once.
- `{2,6}` specifies that the preceding element must appear between 2 and 6 times.
- `*` allows the preceding element to appear zero or more times.

### Grouping Constructs

Grouping constructs, indicated by parentheses `()`, allow multiple characters to be treated as a single unit. For example:

- `(https?://)?` optionally matches the protocol (http or https).
- `([\da-z.-]+)` matches one or more letters, numbers, dots, or hyphens in the domain.
- `([a-z.]{2,6})` matches the top-level domain with 2 to 6 characters.
- `([/\w .-]*)` matches any number of alphanumeric characters, slashes, dots, or hyphens in the path.

### Bracket Expressions

Bracket expressions specify a range of characters to match. For example:

- `[\da-z.-]` matches any digit, lowercase letter, dot, or hyphen.
- `[a-z.]` matches any lowercase letter or dot.
- `[/\w .-]` matches any slash, alphanumeric character, dot, or hyphen.

### Character Escapes

Character escapes, typically starting with a backslash (`\`), indicate non-literal characters. For example:

- `\d` represents any digit (0-9) within `[\da-z.-]`.
- `\w` matches any alphanumeric character within `[/\w .-]`.
