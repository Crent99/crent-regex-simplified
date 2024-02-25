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

In the provided regular expression snippet `/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/`, there are several quantifiers used:

1. `?`: The question mark quantifier denotes that the preceding element (in this case, `(https?:\/\/)`) is optional. It allows for zero or one occurrence of the preceding element.

2. `+`: The plus sign quantifier means "one or more" of the preceding element. It applies to `([\da-z\.-]+)`, ensuring that there must be at least one character from the set of digits, lowercase letters, dots, and hyphens.

3. `{2,6}`: The curly braces with two numbers separated by a comma denote a range quantifier. In this case, `{2,6}` specifies that the preceding element (`[a-z\.]`) must occur between 2 and 6 times. This quantifier applies to `([a-z\.]{2,6})`, ensuring that the top-level domain part of the URL contains between 2 and 6 lowercase letters or dots.

4. `*`: The asterisk quantifier means "zero or more" of the preceding element. It applies to `([\/\w \.-]*)`, allowing for an optional path part in the URL, containing zero or more characters including forward slashes, word characters, spaces, dots, and hyphens.

Overall, these quantifiers provide flexibility in matching different components of the URL while allowing for variations in their presence or repetition.

### Grouping Constructs

### Bracket Expressions

### Character Classes

### The OR Operator

### Flags

### Character Escapes

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
