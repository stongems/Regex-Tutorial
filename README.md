# Regex-Tutorial
This tutorial breaks down the regular expressions for an email. 


## Summary
Email Regex
```
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
```


## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)


## Regex Components

```/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/```



## Anchors
/  ```^``` ([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6}) ```$``` /<br>
The characters ```^``` and ```$``` are both considered anchors.
The ```^``` character is used at the beginning to signify the start of a Regex string. While the ```$``` character, is used at the end to signifies the completion of the Regex.



## Quantifiers
```+``` — **Matches the pattern one or more times.**

/^([a-z0-9_\.-] ```+``` )@([\da-z\.-] ```+``` )\.([a-z\.]{2,6})$/ <br>

Example, ```/a+/``` matches the "a" in "candy" and all the "a"'s in "caaaandy".

```{ n, x }``` — **Matches the pattern from a minimum of n number of times to a maximum of x number of times.**<br>

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.] ```{2,6}``` )$/<br>

Example: ```/a{1,3}/``` matches nothing in "cndy", the "a" in "candy", the two "a"'s in "caandy", and the first three "a"'s in "caaaaaaandy". Notice that when matching "caaaaaaandy", the match is "aaa", even though the original string had more "a"s in it.



## Grouping Constructs

```()``` - **Way to group a section of Regex**

/^ ```([a-z0-9_\.-]+)``` @ ```([\da-z\.-]+)``` \. ```([a-z\.]{2,6})```   $/<br>

What is inside the ```()``` is known as a sub-expression. Capturing groups matches the match character sequence for possible reuse. 



## Bracket Expressions

```[]``` - **Anything inside ```[]``` represents a range of characters that we want to match.**

/^( ```[a-z0-9_\.-]``` +)@( ```[\da-z\.-]``` +)\.( ```[a-z\.]``` {2,6})$/

Example, ```[a-z]``` Includes all lowercase letter a-z. ```[0-9]``` Includes all numbers 0-9. ```[_-]``` Includes both _ and -



## Character Classes

**Character Class defines a set of characters.**<br>

/^([a-z0-9_ ```\.``` -]+)@([ ```\d``` a-z ```\.``` -]+) ```\.``` ([a-z ```\.``` ]{2,6})$/

```.``` - Find a single character, except newline or line terminator <br>
```\d``` - Find a digit<br>



## Sources
source - https://coding-boot-camp.github.io/full-stack/computer-science/regex-tutorial <br>
source - https://developer.mozilla.org/ <br>
source - http://web.mit.edu/gnu/doc/html/regex_3.html


## Author
Matthew St. Onge