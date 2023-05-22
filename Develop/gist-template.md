# Tutorial de Regex en Ingles

## Intro
In this tutorial, we will explore a regular expression that can help us validate email addresses. Regular expressions are patterns used to find specific patterns within text. By the end of this tutorial, you will have a better understanding of how this regular expression works and how it can be used to validate email addresses.

## Summary

Throughout this tutorial, we will dissect the regular expression /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/ to illustrate how different components contribute to validating email addresses. Along the way, we will explore and explain the key elements of regular expressions.

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

Anchors are special characters that allow us to match positions within a string rather than actual characters. In the regular expression, ^ and $ are anchors:

- ^ asserts the start of a line.
$ asserts the end of a line.
- Lets explore how these anchors are used in our email validation regular expression.
#### Example:
For example, if we want to validate the email address john@example.com, the ^ anchor ensures that john@example.com starts at the beginning of the line and not somewhere in the middle.

### Quantifiers

In the  regex email, we use quantifiers to specify the number of occurrences of certain characters. The "+" quantifier means "one or more," and it ensures that there is at least one or more characters before and after the "@" symbol, as well as before the dot leading to the domain name. Additionally, the "{2,6}" quantifier sets the range of characters allowed for the domain name, requiring it to be at least two characters long but no longer than six characters, consisting of lowercase letters and dots.

These quantifiers help define the structure and length requirements of the email address, ensuring that it follows a specific pattern.

### Grouping Constructs

Grouping constructs allow you to create logical groups within a regular expression. In the regular expression, there is a three groups enclosed in parentheses:

- The first group captures the username.
- The second group captures the domain name.
- The third group captures the top-level domain (TLD).
### Example:
A clear example of (Grouping Constructor) is when they are represented by parentheses ( ), this allow you to group multiple characters or expressions within a regular expression. By grouping them together, we can treat the entire group as a single unit and apply quantifiers or operators to it.

### Bracket Expressions

In our regular expression, the brackets [ ] represent a bracket expression, allowing matching of specific characters within them to corresponding characters in the input string. In the email regex, we have the following bracket expressions:

- [a-z0-9_.-] matches any lowercase letter from "a" to "z", any digit from "0" to "9", underscore "_", hyphen "-", and dot "." within the user email name.
- [\da-z.-] matches a single character that can be a digit (0-9), a lowercase letter (a-z), a dot ".", or a hyphen "-". Here, the backslash \ before the "d" represents an escape character used to match any digit from 0 to 9 in the email service.
- [a-z.] matches any lowercase letter from "a" to "z" and a dot "." within the domain name.

These bracket expressions provide flexibility in matching specific characters and ranges within the email pattern.
### Character Classes

Character classes are shortcuts for common bracket expressions. In our regular expression, we use \d:

- \d matches any digit character.

We'll discuss how \d simplifies the matching of digit characters in our regular expression.

### The OR Operator

The OR operator allows us to match either of two expressions. Although not explicitly used in our regular expression, we'll briefly explain how the OR operator works.

### Flags

The email regex provided does not include any flags. It is enclosed within slashes ("/") to indicate that it is treated as a literal pattern. If flags were needed, they would be placed after the second slash to add extra functionality or limitations, allowing modifications such as case-insensitivity or global matching.

### Character Escapes

In regular expressions, the dot character (.) has a special meaning, representing any character except a newline. However, when the dot is inside square brackets ([]) in a regular expression, it loses its special meaning and is treated as a literal dot character. The backslash before the dot (.) is used to escape it, indicating that we want to match the dot character itself rather than its special meaning.

## Author

This tutorial was created by Eduardo Enriquez a student from the UCLA Full stack program. You can find more of my projects and code on my GitHub LaloEnri23 .
