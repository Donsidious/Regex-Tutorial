## Regular Expression - Email Matching

Regular expressions, commonly abbreviated as regex, represent a specific string comprised of various character sets. They serve as versatile tools for querying and validating content within codebases and traditional documents. The concept of regular expressions originated in the early 1950s from the idea of regular language introduced by the mathematician Stephen Cole Kleene. They gained widespread adoption in 1968 within the field of theoretical computer science, providing a means to identify patterns in text files and facilitate lexical analysis. While regular expressions may initially appear cryptic, breaking them down reveals that they are not as complex as they may seem to inexperienced individuals. With some guidance, one can begin crafting their own regex expressions with relative ease.

## Summary

This tutorial delves into the usage of a regular expression for both email matching and validation:

`^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$`

Imagine you're a software developer tasked with identifying insecurely used email addresses within a codebase. By employing the aforementioned regular expression, you can swiftly locate all email instances. Furthermore, this regex pattern can be incorporated as a string within your codebase to validate email addresses. When users are required to input valid email addresses in certain forms, implementing this regex string ensures that they cannot proceed until they have entered a specific number of characters, followed by an "@" symbol, followed by a domain name of varying character length, and concluding with a domain name system (e.g., .com, .net, .dev, etc.) of between 2 and 6 characters.

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

The regex components that define this particular expression are anchors, quantifiers, meta escape characters, character classes, single character matches, grouping and capturing, and bracket expression. Regarding the example used in this tutorial: `^` and `$` are the anchors used, `+` and `{2, 6}` are the two quantifiers, `\d` represents the meta escape character utilized, `[a-z0-9_\.-]`, `[\da-z\.-]`, and `[a-z\.]` represent the character classes, `_`, `\.`, `-` represent the single character matches used, `()` represents the way this regex expression utilizes grouping and capturing, and `[]` delinates the bracket expression used.

### Anchors

In the realm of regex, anchors serve as markers that indicate the start and end points of an expression. In the context of this particular expression, the `^` symbol denotes the beginning of the expression, while the `$` symbol signifies its end.

### Quantifiers

Quantifiers, represented by meta-characters, modify the preceding character in a regex pattern, specifying how many consecutive occurrences should be matched.

Quantifiers enable you to define the desired number of characters or character classes to be matched:

- The `+` symbol matches one or more of the preceding character.
- `{min, max}` establishes a specific numerical range for quantification. You can observe this at the end of the regex expression mentioned above, defining a range for the domain name system.

### OR Operator

While this particular regex expression does not employ OR operators, in general, OR operations are symbolized by the pipe `|` character and are utilized in alternation within regex.

### Character Classes

Character classes are elements within a regex pattern that allow you to specify particular sets of characters to be included in a search pattern.

The character classes employed in this regex expression are `[a-z0-9_\.-]`, `[\da-z\.-]`, and `[a-z\.]`.

- `[a-z0-9_\.-]`: `a-z` matches any single character within the range of lowercase letters from 'a' to 'z' (case-sensitive), `0-9` matches any single digit from '0' to '9' (case-sensitive), `_` matches the underscore character '_', `.` matches the period character '.', and `-` matches the hyphen character '-'.

- `[\da-z\.-]`: `\d` matches any digit (0-9), `a-z` matches any single character within the range of lowercase letters from 'a' to 'z' (case-sensitive), `\.` matches the period character '.', and `-` matches the hyphen character '-'.

- `[a-z\.]`: `a-z` matches any single character within the range of lowercase letters from 'a' to 'z' (case-sensitive), and `\.` matches the period character '.'.

Other examples of single characters used in regex patterns include `\d` (matches any digit from 0 to 9), `\w` (matches any alphanumeric character, i.e., a-zA-Z0-9), and `\s` (matches white space, such as spaces or tabs).

### Flags

Regex flags are used to modify the behavior of expressions. In JavaScript, there are six flags: `i` (case-insensitive), `g` (global, to find all matches), `m` (multiline mode), `s` (dotall mode, allowing `.` to match newline characters), `u` (Unicode support), and `y` (sticky mode). Notably, the regex expression discussed in this tutorial does not utilize any flags.

### Grouping and Capturing

Parentheses `()` are used to create sequences or sub-expressions in regex, treating multiple characters as a single unit. In the tutorial's regex expression, you'll notice the use of `()` to define distinct groups of characters. The first group covers characters before the `@` symbol, the second group encompasses characters before the period '.', and the last group includes characters from the period '.' to the end.

### Bracket Expressions

Square brackets `[]` create character or group ranges, representing a single character. In the regex expression discussed here, brackets are employed to separate each character class. The character can be any of those specified within the brackets.

For instance, `[a-z0-9_\.-]` matches any lowercase letter from 'a' to 'z', any digit from '0' to '9', the underscore '_', the period '.', or the hyphen '-'.

### Greedy and Lazy Matching

Greedy matching is the default behavior of regex, where the regex engine seeks to match as much of the string as possible. In contrast, lazy matching attempts to match as little of the string as possible.

- Greedy matching continues searching until the condition is satisfied.
- Lazy matching stops searching once the condition is met.

It's worth noting that greedy matching can be slower than lazy matching since it continues searching for all possible matches, while lazy matching stops at the first match it finds.

### Boundaries

The `\b` symbol represents a word boundary in regex. It typically denotes positions where one side consists of a word character, and the other side contains a non-word character. Word boundaries are particularly useful when you want to match sequences of letters or digits at the beginning or end of specific character sequences.

### Back-references

Back-references are commands that refer to a previous part of the matched regex expression. They are usually specified using a backslash followed by a single digit, like `\2`.

### Look-ahead and Look-behind

Look-ahead, denoted as `?=foo`, represents what immediately follows the string "foo" in a regex pattern. In contrast, look-behind, written as `?<=foo`, signifies what immediately precedes the string "foo."

## Author
Alfredo Salayandia is a WebDev 

For additional inquiries, you can contact Alfredo through his GitHub account.
[Link to Github](https://github.com/Donsidious)
