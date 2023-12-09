# CS-regex

Regular expressions are a powerful tool to match text. They are used in many programming languages and are also used in many text editors. This tutorial will help you learn the basics of regular expressions.

## Summary

This tutorial is going to help understand the email regular expression, `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` . I will break it down into its components and explain what each of them do.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components
<div align="center">
A regax component is a part of a regular expression that is used to match a specific pattern by using a specific character and combination of characters.
<img src="./image/email-regax.png" alt="Regex Components" width="500" height="300">
</div>

### Anchors
/`^`([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})`$`/

Regular expression anchors match positions in the input string rather than matching specific characters. The archors in this tutorial are the caret `^` and the question mark `?`. The caret matches the beginning of a string and the question mark matches the end of a string.

### Quantifiers
/^([a-z0-9_\.-]`+`)@([\da-z\.-]`+`)\.([a-z\.]`{2,6}`)$/

Quantifiers are used to specify the number of times a character or group of characters should be matched by using a number or a range of numbers. The `+` quantifiers match the username and domain greedily, and the `{2,6}` quantifier limits the top level domain to between 2 and 6 characters in length. These quantifiers allow flexible matching of different length email addresses.

### OR Operator
/^(`[`a-z0-9_\.-`]`+)@(`[`\da-z\.-`]`+)\``.`(`[`a-z\.`]`{2,6})$/

The OR operator is used to match one of two or more patterns. The `.` dot meta character is used as a wildcard, and character classes defined with `[]` are used to match specific types of characters in the different parts of the email address string. Some examples of the OR operator are: `.` to match any characters in the domain and `[]` to define character classes.

### Character Classes
/^([`a-z0-9_\.-`]+)@([`\da-z\.-`]+)\.([`a-z\.`]{2,6})$/

Character classes are used to match a single character from a set of characters by using a set of characters enclosed in square brackets `[ ]`. some examples of character classes used in this regex are: `[a-z0-9_\.-]`, `[\da-z\.-]` and `[a-z\.]`.

### Flags

Flags are used to modify the behavior of a regular expression by using a pound sign `#`. This regex does not contain any flags.

### Grouping and Capturing
/^(`[a-z0-9_\.-]+`)@(`[\da-z\.-]+`)\.(`[a-z\.]{2,6}`)$/

Grouping is used to group a set of characters or groups of characters together by using a round bracket `( )`. The first group `([a-z0-9_\.-]+)` matches the username, the second group `([\da-z\.-]+)` matches the domain, and the third group `([a-z\.]+)` matches the top level domain.

### Bracket Expressions
/^(`[a-z0-9_\.-]`+)@(`[\da-z\.-]`+)\.(`[a-z\.]`{2,6})$/

Bracket expressions are used to match a single character from a set of characters by using a set of characters enclosed in square brackets `[ ]`. `[a-z0-9_\.-]` - Matches lowercase letters, digits, underscore, period, and hyphen, `[\da-z\.-]` - Matches digits, lowercase letters, period, and hyphen, and `[a-z\.]` - Matches lowercase letters and period

### Greedy and Lazy Match
/^([a-z0-9_\.-]`+`)@([\da-z\.-]`+`)\.([a-z\.]{2,6})$/

Greedy and lazy match are used to specify whether a regular expression should try to match as much text as possible by using a question mark `?` or an asterisk `*`. The `+` inside `([a-z0-9_\.-]+)` and `([a-z\.]+)` is a greedy match, which means that it tries to match as much text as possible. This regex does not contain any lazy match that would indicate that it should try to match as little text as possible.

### Boundaries
/`^`([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})`$`/

Boundaries are used to match the beginning or the end of a string by using a dollar sign `$` or a caret `^`. This regex has those two examples to help read the email address string from the beggining to the end.

### Back-references

Back-references are used to match a previously matched group by using a backslash `\` and a number. This regex does not contain any back-references.

### Look-ahead and Look-behind

Look-ahead and look-behind are used to match a specific pattern only if it is followed or preceded by another pattern by using a question mark `?` or an asterisk `*` and a round bracket `( )`. This regex does not contain any look-ahead or look-behind.

## Author

<div align="center">
    <p>This tutorial was created by</p>
    <a href="https://github.com/vromero-beltran">
    <img src="https://avatars.githubusercontent.com/vromero-beltran?=100" width="100px;" alt="Victor Romero-Beltran's Github Profile" style="border-radius: 50px"/>
    </a>
    <br>
    <a href="https://github.com/vromero-beltran" title="Github">💻 Victor Romero-Beltran 💻</a>
</div>