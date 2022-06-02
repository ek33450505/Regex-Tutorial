# Tutorial: Regex Matching an Email

Regular expression (or regex, for short) are patterns used to match character combination in strings or to find and replace a character or sequence of characters within a string.  In Javascript regular expressions are also objects. A regular expression pattern is composed of simple characters, such /abc/ or a combination of characters and symbols, such as /ab*c/. 

## Summary

The following regular expression can be used to verify that user input is a valid email address:

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

## Table of Contents

- [Tutorial: Regex Matching an Email](#tutorial-regex-matching-an-email)
  - [Summary](#summary)
  - [Table of Contents](#table-of-contents)
  - [Regex Components](#regex-components)
    - [Anchors](#anchors)
    - [Quantifiers](#quantifiers)
    - [Character Classes](#character-classes)
    - [Grouping and Capturing](#grouping-and-capturing)
    - [Bracket Expressions](#bracket-expressions)
    - [Greedy and Lazy Match](#greedy-and-lazy-match)
  - [Author](#author)

## Regex Components

Regular expressions are made up of several components. Although nearly illegible, regaular expressions can be better understood when broken down into smaller components. The expample regex /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/ can be broken down into the following components:

### Anchors

Anchors do not match any characters in the expression, instead they match a position before or after the remaining experession characters. They are used to "anchor" the regex match at a certian position as the first and last components.
In the email adress example the caret (^) matches the position before the first character in the string (beginning) as seen in our example: /^([a-z0-9_\.-]+. Similary, $ matches right after the last character in the string (end) as seen in our example: {2,6})$.

### Quantifiers

Quantifiers specify how many instances of a character, group, or group of character class must be present in the input for a match to be found. The traditional quantifier is contained between two curly braces, {n,m}, and contains up to two arguments. The first argument, n, is the minimum number of matches required and m, acts as the maximum number of matches for the expression to be true. In our example {2,6} is an example of a quantifier.

The other quantifier in this email example if the +. In regular expressions + stands for one or more. In this example + states that there must be one or more matching characters for the bracketted expression to return true.
 
### Character Classes

Character classes are expressions used to specify which characters to match. In our email example, the first character class is [a-z0-9_\.-]. This example includes two character ranges, a-z, which will match any lowercase letters between a and z and 0-9 which will match any digit between 0 and 9.

### Grouping and Capturing

By grouping expressions we are able to extract the characters of a given group for validation. Text between paranthesis is defined as a group. In our example we have three groups:
([a-z0-9_.-]+)
([\da-z.-]+)
([a-z.]{2,6})

### Bracket Expressions

Bracket expressions define which characters are required to be matched. Our email example provides three examples:
([a-z0-9_\.-]+) - the first group states that all characters, a through z and all numeric cheracters between 0 and 9 will be matched.
([\da-z\.-]+) - the second checks for a-z characters and checks the character \d for a matching digital digit.
([a-z\.] -= lastly, this group verifies that characters a-z will be matched.

### Greedy and Lazy Match

Greedy matches tell the search engine to match as many instances of its qualified token as possible (the longest). In contrast lazy matches (the shortest match) tell the seartch engine to match as few of the quantified tokens as needed.
In our example, the + quantifier is a greedy match. It will ensure a search of as many quantified tokens are possible.

## Author

Hello! My name is Edward Kubiak and I am a full stack web development student. Follow me below!:
GitHub: https://github.com/ek33450505
Linkdein: https://www.linkedin.com/in/edward-kubiak-048526193/
