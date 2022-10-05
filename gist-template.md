# Regex Tutorials: Emails
Introductory paragraph (replace this with your text)

## Summary
```text
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
```
The regular expression above is a search function for email addresses, with the content below going over the functionality of each character.

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
The `^` at the start, and `$` at the bottom are the anchors containing this expression. 

### Quantifiers
The `+` and `{2,6}` are the quantifiers of this expression, with `+` connecting the groups together, while `{2,6}` sets a 2-6 character limit.  

### Grouping Constructs
Grouping constructs are separeted by `()`, with the first group `[a-z0-9_\.-]` capturing the name of the email. The second group `[\da-z\.-]` captures the domain/provider of the address, such as "gmail". The third group `[a-z\.]{2,6}` captures the domain extention, with ".com" being a prime example. 

### Bracket Expressions
Brack expressions contain characters classes for the regex, and much like grouping constructs, this example contains three bracket expressions. The first bracket `[a-z0-9_\.-]` includes case sensitive characters from a-z, numbers from 0-9 an underscore, periods and hyphens. The second bracket `[\da-z\.-]` includes all digits, case sensitive characters from a-z, periods and hyphens. The third bracket `[a-z\.]` includes case sensitive characters from a-z and periods. 

### Character Classes
Character classes distinguishes characters the regex should be looking for, with "a-z" representing the alphabet in lowercase characters and "0-9" representing the numbers 0 through 9. 
### The OR Operator
OR operators are alternations, declared/exhbited with a `|`.
### Flags
There is six primary flags in javascript:
- "i" searches are case-insensitive.
- "g" seaches for all matches, only the first search returned without it. 
- "m" = multiline mode.
- "s" = "dotall" mode, allows dots to match newline characters.
- "u" = enables full unicode support, allowing correct process of surrogate pairs.
- "y" = "sticky" mode, searches exact positions in text

### Character Escapes
Character escapes allow certain characters that would usually have a function in a regex be taken for their character value. This is done by prefacing a character with a "", an example of this can be found multiple times in the email regex where the character escape "." is used.

## Author
This was written by [Justin Kang](https://github.com/iinukng)