# Regex-Tutorial
# 20210716 Regex Gist

Assigned to create a tutorial that explains a specific regular expression. 
I have selected an expression that allows you to match an email: `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

## Summary
```
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
```


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

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

### Anchors

### Quantifiers


---

x*	
Matches the preceding item "x" 0 or more times. For example, /bo*/ matches "boooo" in "A ghost booooed" and "b" in "A bird warbled", but nothing in "A goat grunted".

x+	
Matches the preceding item "x" 1 or more times. Equivalent to {1,}. For example, /a+/ matches the "a" in "candy" and all the "a"'s in "caaaaaaandy".

x?	
Matches the preceding item "x" 0 or 1 times. For example, /e?le?/ matches the "el" in "angel" and the "le" in "angle."

If used immediately after any of the quantifiers *, +, ?, or {}, makes the quantifier non-greedy (matching the minimum number of times), as opposed to the default, which is greedy (matching the maximum number of times).

x{n}	
Where "n" is a positive integer, matches exactly "n" occurrences of the preceding item "x". For example, /a{2}/ doesn't match the "a" in "candy", but it matches all of the "a"'s in "caandy", and the first two "a"'s in "caaandy".

x{n,}	
Where "n" is a positive integer, matches at least "n" occurrences of the preceding item "x". For example, /a{2,}/ doesn't match the "a" in "candy", but matches all of the a's in "caandy" and in "caaaaaaandy".

x{n,m}	
Where "n" is 0 or a positive integer, "m" is a positive integer, and m > n, matches at least "n" and at most "m" occurrences of the preceding item "x". For example, /a{1,3}/ matches nothing in "cndy", the "a" in "candy", the two "a"'s in "caandy", and the first three "a"'s in "caaaaaaandy". Notice that when matching "caaaaaaandy", the match is "aaa", even though the original string had more "a"s in it.

x*?
x+?
x??
x{n}?
x{n,}?
x{n,m}?

By default quantifiers like * and + are "greedy", meaning that they try to match as much of the string as possible. The ? character after the quantifier makes the quantifier "non-greedy": meaning that it will stop as soon as it finds a match. For example, given a string like "some <foo> <bar> new </bar> </foo> thing":

/<.*>/ will match "<foo> <bar> new </bar> </foo>"
/<.*?>/ will match "<foo>"

source - https://developer.mozilla.org/

---

### Grouping Constructs

### Bracket Expressions

### Character Classes



---

. - Find a single character, except newline or line terminator
\w - Find a word character
\W - Find a non-word character
\d - Find a digit
\D - Find a non-digit character
\s - Find a whitespace character
\S - Find a non-whitespace character
\b - Find a match at the beginning/end of a word, beginning like this: \bHI, end like this: HI\b
\B - Find a match, but not at the beginning/end of a word
\0 - Find a NULL character
\n - Find a new line character
\f - Find a form feed character
\r - Find a carriage return character
\t - Find a tab character
\v - Find a vertical tab character
\xxx - Find the character specified by an octal number xxx
\xdd - Find the character specified by a hexadecimal number dd
\udddd - Find the Unicode character specified by a hexadecimal number dddd

source - https://developer.mozilla.org/

---

### The OR Operator

### Flags

### Character Escapes

## Author
Matthew St. Onge