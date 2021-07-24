# Regex-Tutorial
This tutorial breaks down the regular expressions. 

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

```/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/```

## Anchors

The characters ```^``` and ```$``` are both considered anchors.
The ```^``` character is used at the beginning to signify the start of a Regex string. While the ```$``` character, is used at the end to signifies the completion of the Regex.


## Quantifiers

```*``` — **Matches the pattern zero or more times.**

For example, ```/bo*/``` matches "boo" in "A ghost booed" and "b" in "A bird babbled", but will not match anything in "A goat grunted".

```+``` — **Matches the pattern one or more times.**

Equivalent to ```{1,}```. For example, ```/a+/``` matches the "a" in "candy" and all the "a"'s in "caaaandy".

```?``` — **Matches the pattern zero or one time.**

For example, ```/e?le?/``` matches the "el" in "angel" and the "le" in "angle." If used immediately after any of the quantifiers ```*, +, ?, or {}``` makes the quantifier non-greedy (matching the minimum number of times), as opposed to the default, which is greedy (matching the maximum number of times).

```{}``` — **Curly brackets can provide three different ways to set limits for a match:* ```{ n } || { n, } || { n, x }```

```{ n }``` — **Matches the pattern exactly n number of times.**	

For example, ```/a{2}/``` doesn't match the "a" in "candy", but it matches all of the "a"'s in "caandy", and the first two "a"'s in "caaandy".

```{ n, }``` — **Matches the pattern at least n number of times.**

For example, ```/a{2,}/``` doesn't match the "a" in "candy", but matches all of the a's in "caandy" and in "caaaaaaandy".

```{ n, x }``` — **Matches the pattern from a minimum of n number of times to a maximum of x number of times.**

For example, ```/a{1,3}/``` matches nothing in "cndy", the "a" in "candy", the two "a"'s in "caandy", and the first three "a"'s in "caaaaaaandy". Notice that when matching "caaaaaaandy", the match is "aaa", even though the original string had more "a"s in it.

---

## Grouping Constructs

```()``` - **Way to group a section of Regex**

What is inside the ```()``` is known as a sub-expression. Capturing groups matches the match character sequence for possible reuse. 

## Bracket Expressions

```[]``` - **Anything inside ```[]``` represents a range of characters that we want to match.**

Example, ```[a-z]``` Includes all lowercase letter a-z. ```[0-9]``` Includes all numbers 0-9. ```[_-]``` Includes both _ and -


## Character Classes

**Character Class defines a set of characters.**<br>
```.``` - Find a single character, except newline or line terminator <br>
```\w``` - Find a word character<br>
```\W``` - Find a non-word character<br>
```\d``` - Find a digit<br>
```\D``` - Find a non-digit character<br>
```\s``` - Find a whitespace character<br>
```\S``` - Find a non-whitespace character<br>
```\b``` - Find a match at the beginning/end of a word, beginning like this: \bHI, end like this: HI\b<br>
```\B``` - Find a match, but not at the beginning/end of a word<br>
```\0``` - Find a NULL character<br>
```\n``` - Find a new line character<br>
```\f``` - Find a form feed character<br>
```\r``` - Find a carriage return character<br>
```\t```- Find a tab character<br>
```\v``` - Find a vertical tab character<br>
```\xxx``` - Find the character specified by an octal number xxx<br>
```\xdd``` - Find the character specified by a hexadecimal number dd<br>
```\udddd``` - Find the Unicode character specified by a hexadecimal number dddd

## The OR Operator
```|``` -  Can provide as many terms as desired, as long as they are separated with the pipe character.

Example: ^I like ```(dogs|penguins)```, but not ```(lions|tigers)```$

## Flags
Regular expressions have six optional flags that allow for functionality like global and case insensitive searching. These flags can be used separately or together in any order, and are included as part of the regular expression.

```d``` - Generate indices for substring matches. <br>
```g``` - Global search.<br>
```i``` - Case-insensitive search.<br>
```m``` - Multi-line search.<br>
```s``` - Allows . to match newline characters.<br>
```u``` - "unicode"; treat a pattern as a sequence of unicode code points.<br>
```y``` - Perform a "sticky" search that matches starting at the current position in the target string.

Example: re = /\w+\s/g creates a regular expression that looks for one or more characters followed by a space, and it looks for this combination throughout the string.

## Character Escapes
```\``` - Will match literal instead of special character.

Example: To search for the string ```/example/``` followed by one or more alphabetic characters, you'd use ```/\/example\/[a-z]+/i```

## Sources
source - https://coding-boot-camp.github.io/full-stack/computer-science/regex-tutorial <br>
source - https://developer.mozilla.org/ <br>
source - http://web.mit.edu/gnu/doc/html/regex_3.html

## Author
Matthew St. Onge