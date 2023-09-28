# Title (MATCH AN EMAIL ADDRESS - REGEX TUTORIAL )

Introductory paragraph (The purpose of this REGEX (regular expressions) tutorial is to be able to match email addresses )

## Summary

 We'll be looking at how the following regular expression is used to match an email address:

var emailRegex = /\b([a-z])([\w\.]+)([^\W_]+)@([\da-z\.-]+)\.([a-z\.]{1,3})\b/g;

The following with be a  walk-through of each of these components to determine how they function.


## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Boundaries](#boundaries)


## Regex Components

var emailRegex = /\b([a-z])([\w\.]+)([^\W_]+)@([\da-z\.-]+)\.([a-z\.]{1,3})\b/g;


### Quantifiers

"+" This dentifies a string that contains certain characters at the beginning, followed by one or more elements at the end. For example, within our code section:

"([\w.]+) => [\w.]" will identify any character that is a word character (equivalent to \w, which includes letters, numbers, and underscores) or a period ".", repeated one or more times.

The curly brackets "{}" are used to specify either an exact number, a minimum and maximum range, or multiple occurrences of the preceding sequence before these quantifiers.

In our code section, "([a-z.]{1,3})" matches the previous pattern "([a-z.])" between 1 and 3 times, as many times as possible.


### OR Operator

"[]" is a notation that identifies a character contained within the square brackets.

For instance, within our code section, "[a-z]" identifies a character falling within the range of lowercase letters from "a" to "z."

"[^...]" represents a character that is not found within the square brackets.

In our code example, "[^\W_]" identifies any character that is absent from the specified list. "\W" stands for any non-word character, which is equivalent to "[^a-zA-Z0-9_]", and """ represents the underscore character "".




### Character Classes

\w Matches a word character, i.e. [a-zA-Z0-9_].

\d Matches a single character that is a digit.



### Flags

When crafting (Regex), the parameters are enclosed within a pair of forward slash characters /.../. After the second slash, you can specify additional modifiers, often referred to as "flags."

One such flag is "g" (global). Enabling the "g" flag permits the search to persist beyond the first match, continuing until no further matches can be located.



### Grouping and Capturing

() Captures everything enclosed within the parenthesis. 



### Boundaries
This expression identifies matches occurring at a word boundary. In this context, a word boundary signifies that one side of the match is a word character, such as \w (which includes letters, digits, and underscores), while the other side is a non-word character, such as a space.


## Author
Adriana Herrera -- Student at University of Miami Bootcamp.
https://github.com/itsadrih