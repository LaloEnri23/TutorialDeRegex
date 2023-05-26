# Tutorial de Regex en Ingles

## Intro
Bienvenido to the tutorial on regular expressions! In this tutorial, we will explore a regular expression that is commonly used to validate email addresses. Regular expressions are creative patterns used to search for and match specific patterns within text. By the end of this tutorial, you will have a clear understanding of how this regular expression works and how it can be used to validate email addresses effectively.

## Summary

Throughout this tutorial, we will dissect each component and regular expression /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/ to illustrate how different components contribute to validating email addresses. Along the way, we will explore and explain the key elements of regular expressions. By understanding each element, you will gain the knowledge to create robust email address validation logic.

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

Anchors are special characters that allow us to match positions within a string rather than actual characters. In the context of email validation, we use the `^` anchor to assert the start of a line and the `$` anchor to assert the end of a line. For example, the `^` anchor ensures that the email address starts at the beginning of the line and not somewhere in the middle.

#### Example:
For example, if we want to validate the email address john@example.com, the ^ anchor ensures that john@example.com starts at the beginning of the line and not somewhere in the middle.

### Quantifiers

Quantifiers specify the number of occurrences of certain characters. We use the `+` quantifier to match one or more characters before and after the "@" symbol, as well as before the dot leading to the domain name. Additionally, the `{2,6}` quantifier sets the range of characters allowed for the domain name. This ensures that the domain name consists of at least two characters but no more than six characters, consisting of lowercase letters and dots.

These quantifiers help define the structure and length requirements of the email address, ensuring that it follows a specific pattern.

### Grouping Constructs

Grouping constructs allow you to create logical groups within a regular expression. In the context of email validation, we use three groups enclosed in parentheses to capture the username, domain name, and top-level domain (TLD) separately. By grouping them together, we can treat each group as a single unit and apply quantifiers or operators to it. For example, (Grouping Constructor) allows you to group multiple characters or expressions within a regular expression.

- The first group captures the username.
- The second group captures the domain name.
- The third group captures the top-level domain (TLD).
### Example:
A clear example of (Grouping Constructor) is when they are represented by parentheses ( ), this allow you to group multiple characters or expressions within a regular expression. By grouping them together, we can treat the entire group as a single unit and apply quantifiers or operators to it.

### Bracket Expressions

Bracket expressions, represented by the brackets [ ], allow matching of specific characters within them to corresponding characters in the input string. In the email validation regular expression, we have the following bracket expressions:

- [a-z0-9_.-] matches any lowercase letter from "a" to "z", any digit from "0" to "9", underscore "_", hyphen "-", and dot "." within the user email name.
- [\da-z.-] matches a single character that can be a digit (0-9), a lowercase letter (a-z), a dot ".", or a hyphen "-". The backslash \ before the "d" represents an escape character used to match any digit from 0 to 9 in the email service.
- [a-z.] matches any lowercase letter from "a" to "z" and a dot "." within the domain name.

These bracket expressions provide flexibility in matching specific characters and ranges within the email pattern.

### Character Classes

Character classes are shortcuts for common bracket expressions. In our regular expression, we use \d to match any digit character. It is equivalent to the bracket expression [0-9]. Using \d simplifies the matching of digit characters in our regular expression.

### The OR Operator

The OR operator allows us to match either of two expressions. Although not explicitly used in our email validation regular expression, it is a powerful tool in regular expressions. The OR operator is represented by the pipe symbol `|` and allows for more flexible pattern matching.

### Flags

Flags are a bit different since they are optional parameters that can be added to a regular expression to modify its behavior. While the email validation regular expression provided does not include any flags, it is worth exploring different flags and how they can add extra functionality or limitations to regular expressions.

### Character Escapes

In regular expressions, certain characters have special meanings. To treat these special characters as literal characters, we use character escapes represented by a backslash (`\`). In the context of email validation, the dot character (`.`) has a special meaning, representing any character except a newline. However, to match the actual dot character itself in the email validation regular expression, we use `\.` and escape the dot with a backslash.

## Author

This tutorial was created by Eduardo Enriquez a student from the UCLA Full stack program. You can find more of my projects and code on my GitHub LaloEnri23 .
