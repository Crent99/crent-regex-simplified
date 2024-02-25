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
- [The OR Operator](#the-or-operator)
- [Character Escapes](#character-escapes)
- [Author](#author)

## Regex Components

### Anchors

1. `^`: This is the caret symbol and it denotes the start of the string. In the context of regular expressions, it asserts that the pattern following it must occur at the very beginning of the string.

2. `$`: This is the dollar sign and it denotes the end of the string. Similar to the caret symbol, the dollar sign asserts that the pattern preceding it must occur at the very end of the string.

Together, these anchors `^` and `$` ensure that the entire regular expression pattern matches the entire string, from start to finish. This means that the string must conform to the specified URL pattern without any additional characters before or after it.

### Quantifiers

1. `?`: The question mark quantifier denotes that the preceding element (in this case, `(https?:\/\/)`) is optional. It allows for zero or one occurrence of the preceding element.

2. `+`: The plus sign quantifier means "one or more" of the preceding element. It applies to `([\da-z\.-]+)`, ensuring that there must be at least one character from the set of digits, lowercase letters, dots, and hyphens.

3. `{2,6}`: The curly braces with two numbers separated by a comma denote a range quantifier. In this case, `{2,6}` specifies that the preceding element (`[a-z\.]`) must occur between 2 and 6 times. This quantifier applies to `([a-z\.]{2,6})`, ensuring that the top-level domain part of the URL contains between 2 and 6 lowercase letters or dots.

4. `*`: The asterisk quantifier means "zero or more" of the preceding element. It applies to `([\/\w \.-]*)`, allowing for an optional path part in the URL, containing zero or more characters including forward slashes, word characters, spaces, dots, and hyphens.

Overall, these quantifiers provide flexibility in matching different components of the URL while allowing for variations in their presence or repetition.

### Grouping Constructs

1. `(...)` - Parentheses are used for creating capturing groups. These groups allow parts of the matched text to be captured and referenced later. In this regex:
   - `(https?:\/\/)?` creates a capturing group for the protocol part of the URL.
   - `([\da-z\.-]+)` creates a capturing group for the domain name part of the URL.
   - `([a-z\.]{2,6})` creates a capturing group for the top-level domain part of the URL.
   - `([\/\w \.-]*)*` creates a capturing group for the path part of the URL.

Capturing groups are useful for extracting specific components of a matched string for further processing or manipulation.

### Bracket Expressions

Bracket expressions, also known as character classes or character sets, are patterns enclosed within square brackets (`[]`) in a regular expression. They are used to match any single character from a set of characters specified within the brackets. In the provided regular expression `/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/`, there are two bracket expressions:

1. `[\da-z\.-]`: This bracket expression matches a single character that can be any of the following:

   - `\d`: Any digit (0-9).
   - `a-z`: Any lowercase letter from 'a' to 'z'.
   - `\.`: A literal dot.
   - `-`: A literal hyphen.

   It is used to match characters in the domain name part of the URL.

2. `[\/\w \.-]`: This bracket expression matches a single character that can be any of the following:

   - `\/`: A literal forward slash.
   - `\w`: Any word character (including letters, digits, and underscores).
   - ` `: A literal space.
   - `\.`: A literal dot.
   - `-`: A literal hyphen.

   It is used to match characters in the path part of the URL.

Bracket expressions offer a compact way to specify a set of characters that can be matched at a specific position in the regular expression. They are useful for defining patterns where certain characters can vary while still adhering to a general structure.

### The OR Operator

`?`: The question mark in `(https?:\/\/)?` indicates that the preceding element, `s?`, can appear zero or one time. This effectively makes the 's' in 'https' optional, allowing the expression to match both 'http://' and 'https://'.

So, in this regex, the question mark `?` serves as an OR operator, enabling the expression to match URLs with or without the 's' in 'https'.

### Character Escapes

1. `\d`: This matches any digit (0-9). It's used within the character class `[\da-z\.-]` to match digits in the domain name part of the URL.

2. `\.`: This matches a literal dot character. It's used both within character classes and outside, such as in `[\da-z\.-]` and `([a-z\.]{2,6})`, to match dots in the domain name and top-level domain parts of the URL.

3. `\w`: This matches any word character, which includes letters, digits, and underscores. It's used within the character class `[\/\w \.-]` to match word characters in the path part of the URL.

4. `\/`: This matches a literal forward slash character. It's used within the character class `[\/\w \.-]` to match forward slashes in the path part of the URL.

5. `\s`: This matches any whitespace character, including spaces, tabs, and newline characters. Although not explicitly used in the given regex, it's a common escape sequence for whitespace characters.

These escapes allow the regex to match specific characters or character classes with special meanings, such as digits, dots, and forward slashes, within the pattern.

## Author

Hello again! My name is Colin Rent or you can call me "crent" if you like but not preferred. I was born and raised in Bel Air, MD and currently reside in Oak Ridge, NC. I am an up and coming Web Developer hoping to make it my full time job in the future. I hope that this page helped you better understand "Regualar Expressions" and how they come in handy when matching a URL.

Contact info below:

- [(Email)](mailto:Crent0699@mail.com)
- [(GitHub)](https://github.com/Crent99)
