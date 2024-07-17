# Regular Expressions (Regex)

## Summary

A Regular Expression or Regex for short is a sequence of characters that defines a search pattern in a body of text. The expression that I am focusing on today is /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/. This expression is used to match and validate email addresses.

## Table of Contents

- [Anchors"](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Components

### Anchors
#### `^` and `$`

- **`^`**: Asserts the position at the start of a line.
- **`$`**: Asserts the position at the end of a line.

The anchors ensure that the entire string mathes from start to finish.

### Quantifiers
#### `+` and `{2,6}`

- **`+`**:  Matches one or more of the characters in the character set.
This ensures the local part and domain part has at least one character.

- **`{2,6}`**:  Matches between 2 and 6 of the characters in the character set.
This ensures the top-level domain has between 2 to 6 characters.

### Grouping Constructs
In regular expressions group constructs are used to group parts of the regex pattern together.

1. **`([a-z0-9_\.-]+)`**: Matches any lower case character (a-z), digit (0-9), underscore, dot or hyphen before the `@`.
2. **`([\da-z\.-]+)`**: Matches any digit (\d which is equivalent to (0-9)), lowercase letter (a-z), dot, or hyphen.
3. **`([a-z\.]{2,6})`**: Matches any lowercase letter (a-z) or dot. Quantifier that matches between 2 and 6 of the preceding element.

### Bracket Expressions (aka Character Classes)
#### `[]`
Bracket expressions or character classes are used to specifiy a set of characters that you want to match. They are enclosed ing square brackets.

Example: [a-z] or [0-9]

### The OR Operator
#### `|`
The OR operator is represented by the pipe symbol above. It allows you to specify alternative patterns to match.

Example: `Mr|Mrs|Ms` searching for any string in the text matching `Mr` OR `Mrs` OR `Ms`.
### Flags
Flags modify the behavior of the regex pattern.
- **`i`**: Case-insensitive matching.
- **`g`**: Global search, finding all matches rather than stopping after the first match.
- **`m`**: Multiline matching, changing the behavior of `^` and `$`.

### Character Escapes
Character Escapes in regular expressions allow you to specify characters that have special meanings or not easily typed directly into a pattern. 

- **`@`**: Matches the literal `@` character.
- **`\.`**: Matches a literal dot.

## Author
This was created by Dameine Yang, a full-stack web developer student.  
Click the link to see my GitHub profile:
[GitHub](https://github.com/Dameine)