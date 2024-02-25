# Title Crent Regex Simplified(Matching A URL)

Hello! My name is Colin Rent and I will be trying my best to explain in a thorough description of how to filter/extract information from URLs(Uniform Resource Locator) using a "Regualr Expression". Please feel free to contact me with the information below if this helped you out!

## Summary

This snippet of code below is referenced as a "Regular Expression" or simplified as a 'Regex':

```md
/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]_)_\/?$/
```

It may look extremely confusing... especially to people that have never heard of a "Regular Expression" but we are going to go over every last symbol, letter and number in that snippet and hopefully afterwards you will be a master. Lets do this together!

Lets summarize before we go in-depth, what does the regex snippet above explain?!

- It simply makes sure that its a valid URL

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

1. `^`: This is the caret symbol and it denotes the start of the string. In the context of regular expressions, it asserts that the pattern following it must occur at the very beginning of the string.

2. `$`: This is the dollar sign and it denotes the end of the string. Similar to the caret symbol, the dollar sign asserts that the pattern preceding it must occur at the very end of the string.

Together, these anchors `^` and `$` ensure that the entire regular expression pattern matches the entire string, from start to finish. This means that the string must conform to the specified URL pattern without any additional characters before or after it.

### Quantifiers

### Grouping Constructs

### Bracket Expressions

### Character Classes

### The OR Operator

### Flags

### Character Escapes

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
