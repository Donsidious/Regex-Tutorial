

# Regular Expressions (Regex) Explained

## Introduction

This README provides an overview of key concepts related to regular expressions (regex). Regex is a powerful tool used in text processing, pattern matching, and data validation. This document breaks down various aspects of regex, making it easier for both beginners and experienced developers to understand and use regular expressions effectively.

## Table of Contents

1. [Anchors](#anchors)
2. [Quantifiers](#quantifiers)
3. [OR Operator](#or-operator)
4. [Character Classes](#character-classes)
5. [Flags](#flags)
6. [Grouping and Capturing](#grouping-and-capturing)
7. [Bracket Expressions](#bracket-expressions)
8. [Greedy and Lazy Match](#greedy-and-lazy-match)
9. [Boundaries](#boundaries)
10. [Back-references](#back-references)
11. [Look-ahead and Look-behind](#look-ahead-and-look-behind)
12. [Author](#author)

## Anchors

Anchors in regex mark the start and end points of an expression. The `^` symbol denotes the beginning, and the `$` symbol represents the end of an expression.

## Quantifiers

Quantifiers are meta-characters that modify the preceding character, specifying how many consecutive occurrences should be matched. Common quantifiers include `+` and `{min, max}`.

## OR Operator

The pipe `|` symbol represents OR operators in regex, allowing alternation within patterns.

## Character Classes

Character classes allow you to define specific sets of characters to be used in search patterns. Examples of character classes include `[a-z0-9_\.-]`, `[\da-z\.-]`, and `[a-z\.]`.

## Flags

Regex flags modify the behavior of expressions. Common flags in JavaScript include `i`, `g`, `m`, `s`, `u`, and `y`.

## Grouping and Capturing

Parentheses `()` create sequences or sub-expressions, treating multiple characters as a single unit. They are used to capture specific groups of characters.

## Bracket Expressions

Square brackets `[]` define character or group ranges, representing a single character. They are used to specify character classes.

## Greedy and Lazy Match

Greedy matching is the default behavior, seeking to match as much of the string as possible. Lazy matching aims to match as little as possible, stopping as soon as the condition is satisfied.

## Boundaries

The `\b` symbol represents word boundaries, useful for matching sequences of letters or digits at the beginning or end of character sequences.

## Back-references

Back-references refer to previous parts of the matched regex expression, often specified with a backslash and a single digit.

## Look-ahead and Look-behind

Look-ahead (`?=foo`) and look-behind (`?<=foo`) provide information about what follows or precedes a string in a regex pattern.

## Author

This document was authored by Alfredo Salayandia.

For further questions or to contact the author, you can visit Alfredo's GitHub profile [here](https://github.com/Donsidious)

---

Feel free to customize this README as needed and add any additional information or context that you think would be relevant.

