# Regex (Regular Expressions) Tutorial -- Matching E-mails

The purpose of this tutorial is to address what a regex expression is and how to use it. Regular Expressions (Regex) can be used when one is trying to match a specific combination of characters within a string. Simply put, a regex allows the user to search through a body of code to achieve validation or advanced methods like find and replace. the This is optimal for choosing information from a body of code as well for means of validation. This tutorial will demonstrate a snippet of code that can be used for validation puropses (e.g. an email).

## Summary

Throughout this tutorial, a regex expression will be used to reference an example email validation. The following code can be used for matching emails. One use for this code is that it can be used to validate to make sure that an email follows the correct format.

Matching Email-
`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

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
The anchor marks the start and finish of a regular expresion.

The anchors are typically the `^` (start) and the `$` (end).

Any guidlines given bewtween the start and end establish what we are looking for.

Hence the expression must match the code snippet. If not, then it is not a match.
### Quantifiers
Quantifiers specify the amount of instances of a character, group, or class in order for a match to be found.
In this regex,

`/^([a-z0-9_\.-]+)`

it will match any string that contains `a-z`, `0-9`, `_`, `.`, or `-`. The quantifier `+` means that it will look at all of the following conditions to find a match.
In the rest of the regex,

`@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

the `@` indicataes that we are looking for an email service followed by a `.com` for email validation purposes.
### OR Operator
An OR operator executes a search if one or more conditions are met. 
For example, in the following:

`[a-z0-8]{5}`

The search will be for a 5 character long string that must contain only letters `a-z` and numbers `0-8`.
### Character Classes
A character class represents an array of characters within a set of brackets. It will specify certain characters with the given parameters. In the expression

`@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

`/d` serves as the character class, indicating that the input must be a digit from 0-9.
### Flags
Flags in regex expression serve to provide a more specific means for a search. One may specify flags in this way `g , i , m , u , s , y` for example.
All this means is that we are specifically searching for these characters. In the expression

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

there are no flags.
### Grouping and Capturing
Groups in regular expressions are typically identified by a pair of parentheses. In our expression, 

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

`([a-z0-9_\.-]+)` serves as the first group which further indicates that this is where we establish the validation of the user's email name. the second group `([\da-z\.-]+)`
indicates the email service. Finally `([a-z\.]{2,6})` represents the last group which indicates that our user email and email service must be follwed by a `.com`.
### Bracket Expressions
Bracket expressions within regular expressions provide the array of specific characters we are searching for. Lets take our first group, for example.

`([a-z0-9_\.-]+)`

We can see that within the brackets, we are searching for all of the following: all characters between `a-z`, all numbers within `0-9`, or an `_`, `.`, and `-`.
### Greedy and Lazy Match
Greedy and lazy matches within regex expressions provide a means to search for the longest and shortest possible strings. 'Greedy' is the longest and 'Lazy' is the shortest.
In our expression ,

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

we can see the use of 2 `+` which indicates that our expression is greedy. There is a wide range of characters and combinations of specific parameters that we are searching for which means we are using 'Greedy' matching.
### Boundaries
Boundaries serve to look for particular words or character groups. Anything enclosed between the `^` and the `$` can be considered a boundary.
### Back-references
A back-reference is a regex command used to refer back to previous sections of the matched regex. They are specified with `\`. In our case, we can see the use of `/.` to refer back to a previous part in the regex. 
### Look-ahead and Look-behind
A Look-ahead expression involves the syntax 'X(?=Y)'. It means to look for a given expression (x), but match only if the expression if followed by another expression (y).
a Look-behind expression follows the same type of rule, but instead of looking ahead for a follow up expression, it looks behind for a preceding expression. There are no uses of these within our given expression.
## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
This E-mail regex tutorial was created by Kyle Parrish
[GitHub](https://github.com/KMParrish)