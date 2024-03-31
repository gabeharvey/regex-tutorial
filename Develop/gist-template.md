# Hexadecimal Value Regular Expression

This Regular Expression (Regex) Tutorial will focus on the use of Hexadecimal Values (Hex Values). Each section will explain in detail a specific aspect of Hex Value Regex and how it functions within the expression. Please refer to the Table of Contents to search for a particular segment.

## Summary

The following code snippet will be analyzed and explained in detail in this tutorial:

`/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`

The sections explored will include Anchors, Quantifiers, OR Operator, Character Classes, Flags, Grouping and Capturing, Bracket Expressions, Greedy and Lazy Match, Boundaries, Back-references, and Look-ahead and Look-behind.

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

### Anchors

`^` and `$` meta characters are considered anchors in Hex Value Regex. `^` notates the beginning of the string being analyzed and `$` notates the end of the string. All of the code snippet that lies between the anchors `^` and `$` is what Regex will be searching for. No additional characters that lie outside of the anchors will be considered part of the Hex Value Regex pattern.

### Quantifiers

There are several quantifiers in our code snippet. The first quantifier `#` is considered optional due to following `?` character. Here are two case examples demonstrating how `#` is optional in the string:

`#123456` matches the regex pattern because it includes `#` and is followed by 6 hexadecimal characters.

`123456` also matches the regex pattern even though it does not include a `#` because it includes 6 hexadecimal characters.

Here are two quantifiers that must be taken into consideration in the pattern:

`{6}` indicates that the expression must include 6 hexadecimal characters.

`{3}` indicates that the expression must include 3 hexadecimal characters.

### OR Operator

`|` is an example of the OR operator in our code snippet. This signifies that our expression must include either `{6}` 6 hexadecimal characters OR `{3}` 3 hexadecimal characters in the following character classes which will be explained below.

`abcdef` OR `abc` would both satisfy our regex criteria.

### Character Classes

`[a-f0-9]` are our character classes in our code snippet. This signifies that charcters must be a-f or 0-9. Here are some examples that will satisfy our regex criteria:

`b12345` OR `c67`

Here are some examples that would be INCORRECT or INVALID:

`%55555` OR `66*` as these groups include character classes that were not included in code snippet criteria.

### Flags

There are no flags present in our code snippet.

### Grouping and Capturing

The "capturing group" in our Hex Value Regex is notated by our parenthesis `()`. Our expression is looking for `[a-f0-9]{6}` OR `[a-f0-9]{3}`. Each of these examples would be considered alternative patterns.

The code snippet contains two patterns enclosed by parenthesis. These patterns are separated and distinguished by using a separating OR operator `|` within our parenthesis. The "capturing group" includes all patterns within our parenthesis. In this example, the criteria must match either the six-digit hexadecimal criteria OR the three-digit hexadecimal criteria.

The "grouping" in our Hex Value Regex groups our alternative patterns together as one unit. This allows us to apply our anchors to the entire unit as a whole. This will enable capturing of our entire Hexadecimal Code as long as it meets all `[a-f0-9]` character classes and is between `{6}` 6 or `{3}` 3 characters.

### Bracket Expressions

The Bracket Expressions in our code snippet are characters located within `[` and `]`. This code snippet includes two "range expressions" within our "bracket expressions". In the following code snippet example `[a-f0-9]`, characters `a-f` and `0-9` are part of the criteria and are each range epxressions. `[a-f0-9]` in its entirety is considered a bracket expression. If a character falls outside of these range expressions (for example `z` of `z12345`) in our bracket expression, it will make the code snippet invalid.

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)