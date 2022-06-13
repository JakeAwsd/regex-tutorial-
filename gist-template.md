# Email Matching Regex (tutorial)

Regular expressions (shortened as "regex") are special strings representing a pattern to be matched in a search operation. They are an important tool in a wide variety of computing applications, from programming languages like Java and Perl, to text processing tools like grep, sed, and the text editor vim.

## Summary

This gist will cover the how to create an Email Matching Regex as well as describe what each part of the regex is doing

```
Matching an Email: /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
```

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Components

### Anchors

Anchors. These are special sequences which match an empty substring:
```^ matches at the beginning of the target string
$ matches at the end of the target string
\b matches on a word boundary, i.e., the previous or subsequent character is not a word character

^ in the email regex is the begining of the target string and $ is the end of the string
```
### Quantifiers
A number in curly braces {n}is the simplest quantifier. 
When you append it to a character or character class, it specifies how many characters or character classes you want to match. 

In the email regex the + operator is used to add strings together. {2,6} matches 2-6 characters to the set of ```[a-z\.]```


### Grouping Constructs

```
([a-z0-9_\.-]+) is a group matching the email name. the 2nd group is grouping ([\da-z\.-]+) which matches the email provider. the 3rd group ([a-z\.]{2,6}) groups the .com 
```

### Bracket Expressions
```
[a-z0-9_\.-] matches letters a-z, integers 0-9, and symbols . (period) _ (underscore) - (hyphen)
```
### Character Classes
```
\d matches a single character that is a digit. example: it will match 1 but not 11 because 11 is not a single digit.
```

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
