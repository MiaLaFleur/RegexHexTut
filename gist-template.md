# RegexHexTut

In this tutorial, I will give an example of a regular expression and explain each component of the expression and its purpose.

## Summary

This is a regular expression designed to match a hexadecimal. ``` /^#?([a-f0-9]{6}|[a-f0-9]{3})$/ ```. I will be going through what each symbol or digit means in this expression and what it does.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components

### Anchors

In this expression, ``` /^#?([a-f0-9]{6}|[a-f0-9]{3})$/ ```, the caret, ``` ^ ```, indicates that a match will start with the first character after the caret symbol. So, in this regular expression for hexadecimals, a matching string will start with the symbol ``` # ```. The dollar symbol, ``` $ ```, indicates what a matching string will end with, in this case, the match will end after the character grouping is matched.

### Quantifiers

In the example expression, ``` {6} ```, indicates that there will be six characters that fit the range of ``` [a-f0-9] ``` or there will be three characters that fit the range ``` [a-f0-9] ```, this is indicated by the ``` {3} ``` in the expression.

- also, the ``` ? ``` in this case, implies a boolean value, 0 or 1. Typically, this makes the preceding symbol/character optional.

### OR Operator

referencing what was said above in the quantifier section, the reason the string can have either six or three characters matching that range is because the OR operator, ``` | ```, is placed between both bracket expressions.

### Grouping and Capturing

The parentheses around ``` [a-f0-9]{6}|[a-f0-9]{3} ``` are used to wrap both bracket expressions, so that we are then able to place the ending anchor ``` $ ``` after the grouping. This then indicates that no matter if the string matches the three character expression or the six character expression, the string will still match as long as it ends with one of the two options.

### Bracket Expressions

The brackets are wrapped around two ranges, ``` a-f ``` and ``` 0-9 ```. They are used to set a guideline of what characters will pass the test and match. In this case, either a letter from a to f, that is lowercase, or a number from zero to nine.

### Greedy and Lazy Match

This expression is a greedy match, which means it will find the most matches as possible.

## Author

This tutorial was created by Mia LaFleur. 

| My Contact Info|
|----------|
|GitHub: MiaLaFleur|
|My Email: mia.lafleur@yahoo.com|
