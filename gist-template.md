# regex-tutorial

A regular expression is a sequence of characters that specifies a s search pattern in text

## Summary

In this tutorial, you'll learn more about regular expressions.

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
Don't match any character. They match a position before or after characters.

### Quantifiers
Quantifiers specify how many instances of a character, group, or character class must be present in the input for a match to be found

### OR Operator
Regex recognizes range expressions inside a list. They represent those characters that fall between two elements in the current collating sequence. You form a range expression by putting a range operator between two characters.

### Character Classes
With a “character class”, also called “character set”, you can tell the regex engine to match only one out of several characters.

### Flags
Regular expressions have optional flags that allow for functionality like global searching and case-insensitive searching. These flags can be used separately or together in any order, and are included as part of the regular expression.

### Grouping and Capturing
Parentheses group the regex between them. They capture the text matched by the regex inside them into a numbered group that can be reused with a numbered backreference. They allow you to apply regex operators to the entire grouped regex.

### Bracket Expressions
A bracket expression (an expression enclosed in square brackets, "[]" ) is a regular expression that can match a specific set of single characters, and may match a specific set of multi-character collating elements, based on the non-empty set of list expressions contained in the bracket expression

### Greedy and Lazy Match
#### Greedy:
A greedy quantifier always attempts to repeat the sub-pattern as many times as possible before exploring shorter matches by backtracking.

#### Lazy:
A lazy (also called non-greedy or reluctant) quantifier always attempts to repeat the sub-pattern as few times as possible, before exploring longer matches by expansion.

### Boundaries
A word boundary, in most regex dialects, is a position between \w and \W (non-word char), or at the beginning or end of a string if it begins or ends (respectively) with a word character ([0-9A-Za-z_]).

### Back-references
Backreferences match the same text as previously matched by a capturing group. Suppose you want to match a pair of opening and closing HTML tags, and the text in between. By putting the opening tag into a backreference, we can reuse the name of the tag for the closing tag. Here’s how: <([A-Z][A-Z0-9]*)\b[^>]*>.*?</\1>. This regex contains only one pair of parentheses, which capture the string matched by [A-Z][A-Z0-9]*. This is the opening HTML tag. (Since HTML tags are case insensitive, this regex requires case insensitive matching.) The backreference \1 (backslash one) references the first capturing group. \1 matches the exact same text that was matched by the first capturing group. The / before it is a literal character. It is simply the forward slash in the closing HTML tag that we are trying to match.

### Look-ahead and Look-behind
Lookahead and lookbehind, collectively called “lookaround”, are zero-length assertions just like the start and end of line, and start and end of word anchors explained earlier in this tutorial. The difference is that lookaround actually matches characters, but then gives up the match, returning only the result: match or no match. That is why they are called “assertions”. They do not consume characters in the string, but only assert whether a match is possible or not. Lookaround allows you to create regular expressions that are impossible to create without them, or that would get very longwinded without them.

## Author

I am Motasem Diab. I'm a learning full-stack web developer. My [Github Link](https://github.com/diabm1)
