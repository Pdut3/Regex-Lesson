# Regex Lesson

Welcome to the Regex Lesson. Whether you're a programmer, a data analyst, or someone who deals with textual data on a regular basis, understanding regex can greatly enhance your ability to process and manipulate strings efficiently. In this tutorial, we will explore the fundamentals of regular expressions, covering the syntax, components, and various patterns they can match. By the end of this tutorial, you will have a solid understanding of regex and be able to apply this knowledge to perform advanced text processing operations in your programming tasks. Let's dive in and unlock the power of regular expressions!

## Summary

 Regular expressions, commonly known as regex, are powerful patterns used to match and manipulate text. They provide a concise and flexible way to search, validate, and manipulate strings of characters. With regex, you can specify patterns that define how text should be structured or identify specific substrings within larger text data. Regex is widely used in programming languages, text editors, and other tools for tasks like data validation, string manipulation, pattern matching, and search and replace operations. Mastering regular expressions can greatly enhance your ability to work with textual data efficiently and effectively.

 const emailRegex = /^[\w-]+(\.[\w-]+)*@([\w-]+\.)+[a-zA-Z]{2,7}$/;

function validateEmail(email) {
  return emailRegex.test(email);
}

const email = 'example@example.com';
console.log(validateEmail(email)); // Output: true


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
Literal Characters: Literal characters are the simplest components of a regex and match themselves exactly as they appear. For example, the regex abc matches the string "abc" exactly.

Metacharacters: Metacharacters have special meanings in regex and allow for more advanced pattern matching. Some commonly used metacharacters include:

. (dot): Matches any single character except a newline.
* (asterisk): Matches zero or more occurrences of the preceding element.
+ (plus): Matches one or more occurrences of the preceding element.
? (question mark): Matches zero or one occurrence of the preceding element.
| (pipe): Acts as an OR operator, matching either the pattern on the left or the pattern on the right.
() (parentheses): Groups patterns together and captures matched values.
Character Classes: Character classes allow you to match specific sets of characters. They are enclosed within square brackets [ ] and define a set of characters to match. For example, [aeiou] matches any vowel character.

Quantifiers: Quantifiers specify how many times a pattern should occur. They modify the preceding element or group. Some common quantifiers include:

{n}: Matches exactly n occurrences of the preceding element.
{n,}: Matches n or more occurrences of the preceding element.
{n,m}: Matches at least n and at most m occurrences of the preceding element.
Anchors: Anchors specify positions within a string where a pattern should match. Some commonly used anchors include:

^ (caret): Matches the start of a line or string.
$ (dollar sign): Matches the end of a line or string.
\b (word boundary): Matches a position between a word character and a non-word character.
These are just a few of the fundamental components of regular expressions. Understanding these components and how to combine them allows you to create powerful and flexible patterns for matching and manipulating text.

### Anchors
Regex anchors are special characters that match specific positions within a string. They do not match any actual characters, but rather represent positions in the text. Anchors allow you to assert the presence of a pattern at a certain location or enforce specific boundaries for pattern matching. 

Anchors help you define specific positions for pattern matching, allowing you to make more precise matches within text. They are useful for enforcing constraints or boundaries in your regex patterns.

### Quantifiers
Regex quantifiers are used to specify the quantity or repetition of a preceding element in a regular expression. They allow you to define how many times a pattern should occur. Here are some commonly used quantifiers in regular expressions:

* (asterisk): Matches zero or more occurrences of the preceding element. For example, a* matches "a", "aa", "aaa", and so on.

+ (plus): Matches one or more occurrences of the preceding element. For example, a+ matches "a", "aa", "aaa", but not an empty string.

? (question mark): Matches zero or one occurrence of the preceding element. For example, colou?r matches "color" and "colour".

{n}: Matches exactly n occurrences of the preceding element. For example, a{3} matches "aaa".

{n,}: Matches n or more occurrences of the preceding element. For example, a{2,} matches "aa", "aaa", "aaaa", and so on.

{n,m}: Matches at least n and at most m occurrences of the preceding element. For example, a{2,4} matches "aa", "aaa", and "aaaa".

### Grouping Constructs
Regex grouping constructs allow you to group parts of a regular expression together and treat them as a single unit. They provide several benefits, such as capturing matched values, applying quantifiers to multiple elements, and specifying alternations.

Grouping constructs help organize and control the behavior of regular expressions. They enable capturing and referencing specific parts of a matched pattern, applying quantifiers to groups, and specifying alternatives within a group.

### Bracket Expressions
Regex bracket expressions, also known as character classes, allow you to define a set of characters that you want to match in a single position within a regular expression. They are enclosed within square brackets [ ] and provide a concise way to specify a range or a set of characters. Here are the commonly used features of regex bracket expressions. Charater Ranges: You can specify a range of characters with a hyphen '-' inside the brackets, you can do upper, lower case letters and numbers 0-9.

### Character Classes

A regex character class, also known as a character set or character bracket, is a way to define a group of characters in a regular expression. It allows you to match any single character within that defined set. Character classes are enclosed within square brackets [ ] and provide a concise way to specify a range or a set of characters to match.

Regex character classes provide a flexible and concise way to define sets of characters that you want to match within a regular expression. They allow you to match specific ranges, individual characters, negate sets, and use predefined character classes for common patterns.

### The OR Operator
The regex OR operator, denoted by the pipe symbol |, allows you to specify multiple alternatives within a regular expression pattern. It matches any one of the alternatives provided. The OR operator provides flexibility in specifying alternative patterns within a regular expression. It allows you to match different options based on the provided alternatives, expanding the matching possibilities for your regular expressions.

### Flags
Regex flags are modifiers that can be added to a regular expression to change its behavior or add additional functionality. They are appended to the end of a regex pattern using a flag symbol. Here are some commonly used regex flags:

i (ignore case): This flag enables case-insensitive matching. With the i flag, the regex will match characters regardless of their case. For example, /hello/i matches "hello", "Hello", "HELLO", and so on.

g (global): The global flag allows the regex to perform multiple matches within a string. Without the g flag, the regex stops after the first match. With the g flag, it continues searching for all matches. For example, /a/g matches all occurrences of the letter "a" in a string.

m (multiline): The multiline flag changes the behavior of anchors (^ and $). By default, anchors match the start and end of the entire string. With the m flag, they also match the start and end of individual lines within a multiline string.

s (dotall): The dotall flag makes the dot (.) match any character, including newline characters. By default, the dot does not match newline characters.

u (unicode): The unicode flag enables full Unicode matching. It allows regex to correctly handle Unicode characters and properties.

y (sticky): The sticky flag forces the regex to match from the last matched position within a string. It ensures that subsequent matches occur only after the last match.

### Character Escapes
Regex character escapes, also known as escape sequences, allow you to match specific characters that have special meanings within regular expressions. They are represented by a backslash \ followed by a character or combination of characters. Here are some commonly used regex character escapes:

\d: Matches any digit character (0-9).
\D: Matches any non-digit character.
\w: Matches any word character (alphanumeric and underscore).
\W: Matches any non-word character.
\s: Matches any whitespace character (space, tab, newline, etc.).
\S: Matches any non-whitespace character.
\b: Matches a word boundary, indicating the position between a word character and a non-word character.
\B: Matches a non-word boundary, indicating a position that is not between a word character and a non-word character.
\n: Matches a newline character.
\t: Matches a tab character.
\r: Matches a carriage return character.

Regex character escapes provide a convenient way to match specific characters with special meanings within regular expressions, helping you build more precise pattern matching rules.

## Author

My name is Paul Dutile III, I have a beautiful wife and 3 amazing kids. I'm located in the great state of Utah. I am a hardcore sports fan and love to golf. I'm enrolled in the University of Utah's Coding Bootcamp. I owe all my successes thus far to the amazing instructor group! Litterally would not be here without them. I'm looking to take this certification and parlay that with my extensive sales and business background and almost create a role for myself. Down the road add a salesforce certification and really take off. 
