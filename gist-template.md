# Redux Tutorial
 
In this tutorial regex , short for regular expresion is going to be explained. How this expression work and also explain key regex concepts.

## Summary

Regular expressions, are a series of special characters that define a search pattern.
the example that is going to use is regex `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`, used to match and validate if the string is in the form of a email. Below the regex is going to be broken down into section and each components are going to explained


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

The anchors use in this regex are `^` and `$`. `^` indicates the start of the string and `$` indicated the end of the string. So the anything that is contained between `^` and `$` determine how the string should look like and format that this string should be in.

### Quantifiers

Quantifiers are use to set limits on the number of characters the string can contain.

in this regex two quantifiers are used `+` and `{2,6}`

* `+` - matches the pattern one or more times
* `{n,x}` - matches the pattern with minimum of ***n*** times and maximum of ***X*** times

In two section of the expression `[a-z0-9_\.-]+` , `[\da-z\.-]+` the `+` is used. this mean there has to be a minimum of one characters with no maximum that matched the bracket. basically it mean it cant be a empty string

in the last section of the expression `[a-z\.]{2,6}`, there has to be a minimum of two characters and maximum of six chracters that match the bracket

### Grouping Constructs

In regex grouping section are done by using `()`

If the regex used in the tutorial `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` there are three groups

1. `([a-z0-9_\.-]+)`
2. `([\da-z\.-]+)`
3. `([a-z\.]{2,6})`

by removing the bracket expression and quantifer and replacing with numbers to simplify the expresion it would look like this `/^(1)@(2).(3)$/`

### Bracket Expressions

Brackets `[]` are used to defined characters that is to be matched with, or in other word the characters the string must use. Using the bracket in first group of the regex `[a-z0-9_\.-]` as an example

* `[a-z]` - the string can contain letters ***a*** to ***z***, case sensitive
* `[0-9]` - the string can contain numbers ***0*** to ***9***
* `[_\.-]` - the string can contain special letters ***_*** , ***.*** and ***-***

### Character Classes

A character class in a regex defines a set of characters

`\d` is the character class used in the regex

* `\d` - matches and Arabic numeral digit which is equivalent to `[0-9]`

### The OR Operator

The OR operator `|` in used when you want apply logic of ***or*** outside of a bracket expression. A simple example would be `(abc)` and `(a|b|c)`. in the first expression, it requires a string that is strictly ***abc*** but with the ***or*** operater in the second expression, the string can be ***a*** , ***ab***  ,***acb***  ,***cab***   

### Flags

Flags are used to give additional functionality or limit to expression. They are placed in the end of the expression, after the second slash

* `g` - Global search: the regex should be tested against all possible matches in a string.
* `i` - Case-insensitive search: case should be ignored while attempting a match in a string
* `m` - Multi-line search: a multi-line input string should be treated as multiple lines

### Character Escapes

Character escapes `\` are used so the character in regex isn't interpreted literally. For example in this regex `.` is character class without the backslash, if the string has to be matched with the character ***.*** , `\.` has to be used to escape the ***.*** 

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
