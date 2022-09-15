# Email Regular Expression Validator - How To Write: 

## Summary

When you (a developer) prompt a user to input an email for any given reason, you want to validate that what they've put in is indeed an email. This is where the email regex validator comes into play. Here is an example of what the regex email validator looks like: /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

An email typically consists of 3 parts: 

- The username - which can contain special characters, numbers, and of course letters. comes before the '@' sign.
- The domain name - This comes after the '@'. i.e: "gmail".
- The extension - this can contain any letters, anywere between 2-6 characters. i.e: '.com'

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Character Escapes](#character-escapes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)

### Anchors
 - There are two types of anchors; the '^' and the '$' anchor. The ^ anchor signifies the beginning of a string. The $ anchor signifies the end of a string. 
 
### Quantifiers
- A quantifier '{}' is the part of the regex expression which sets a limit for how many characters need to be included in the email. i.e: {2,18} would match characters between 2 and 18 characters long.

### OR Operator
- The OR operator '|' signifies a pattern of characters to match. For example [a-z1-9] would include those characters in any order, using the | operator: [1-9|a-z] the first part would match ONLY characters between 1-9 and the second would part ONLY letters between a and z. 

### Character Escapes
- the character escape '\' escapes a character that would be interpreted literally. You typically use this to "escape" parts of the expression meant for other purposes. i.e: the $ is typically an anchor, BUT if you put the \ before it, the computer would look for the character $, and not use it as an anchor.

### Character Classes
- The character classes operator defines a set of characters for which an input string can match. i.e: \1-9 would match numbers 1-9.

### Grouping and Capturing
- This is meant to group a string of characters to one part the expression. i.e: ([a-z0-9_\.-]+) from this part of the regex expression it would group characters between a-z, 1-9, _ , . - '-'. 

### Bracket Expressions
 - The [] (bracket) expression. The bracket expression tells the computer what is allowed to be passed in for the email. For example [a-zA-Z1-9] will allow any letters (capitalized or not) from a to z and any numbers from 1-9.

## Author

This was written by Kammin Avery.
- [github Profile](https://github.com/Kammina1)
