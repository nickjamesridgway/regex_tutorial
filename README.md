#Regex Tutorial

This a tutorial that explains how a regular expression functions work.

## Summary

This is the regex code that we will be anaylizing today is: `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)
- [Author](#author)

## Regex Components

### Anchors
Anchors indicate a position to match strings.
`^` anchor matches at the beginning of a string.
`$` ancher matches at the end of a string.


### Quantifiers
Quantifiers indicate how many instances a character to match in a string and is appended to a character or an range of characters, e.g. `[...]`, more on that later. 
```
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
```
In our example, we used:
1. `{2,6}` quantifier, we have set an range of 2 to 6 times to match what's denoted in `[...]`.
2. `+` quanifier at the end of `[...]`, this indicates we are matching between one and unlimited times. Both quantifiers matches as many time as possible giving back as needed.

### Grouping Constructs
Grouping is denoted by by parentheses, it unifies a pattern or string to be matched in a complete block. 
```
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
```
In this example we have 3 groups `([a-z0-9_\.-]+)`, `([\da-z\.-]+)` and `([a-z\.]{2,6})`. 

### Bracket Expressions
Brackets indicate a character class or range of characters that we want to match. 

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

Example:
1. `[a-z0-9_\.-]` indicates we are looking for `lowercase "a-z" a through z, "0-9" 0 through 9, and we literal match special characters "_" underscore, "\." dot, and "-" hyphen`. 
2. `[\da-z\.-]` indicates we are looking for `"\d" 0 through 9, "a-z" a through z, "\." dot, and "-" hyphen`.
3. `[a-z\.]` indicates we are looking for `"a-z" a through z, and  "\." dot`.


### Character Classes
Character classes is a range of characters denoted in `[...]` of what we want to match.


### The OR Operator
This specific regex does not have an "or" operator

### Flags
This specific regex does not have an "flag" operator


### Character Escapes
Backslash "\" is the escape character in regex, escaping a character prevents a character from beging interpreted as a literal character.

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

Example:
`"\." is in several places, using the backsplash denotes that we want to find just the dot`.


## Author

Nick Ridgway

Find me on my [GitHub](https://github.com/nickjamesridgway)!