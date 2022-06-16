# Regex Expressions

## Summary

Here a Regex expression is being deconstructed into its elements and a brief description is provided for each element and what it does. The example expression `/^<([a-z]+)([^<]+)*(?:>(.*)<\/\1>|\s+\/>)$/` is used for matching an HTML tag

## Table of Contents

- [Anchors](#anchors)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Back-references](#back-references)

## Regex Components
The components are the entire code - /^<([a-z]+)([^<]+)*(?:>(.*)<\/\1>|\s+\/>)$/

### Anchors
Anchors are "^" and "$". Anchors mark the beginning and ending of an expression. In my Regex component, the anchor "^" is marking the 
beginning of my expression and "$" is marking the ending. For example: 
  
  ^A finish$   exact string match (starts and ends with A finish)

### OR Operator
OR operator acts like a boolean and matches the expression before and after "|". And the other orerator which is "[]" matches any one of the characters enclosed in these brackets. 
 
 [a-z] - this will match any characters from lowercase a to z. 
 
 <\/\1>|\s+\/> - this will match a self closing or a regular element 

### Character Classes
Character classes are used to match specific characters. /s in my code matches a whitespace character and includes tabs and line breaks. 
Other examples not included in my code are:
  /w - which matches a word character
  
### Grouping and Capturing
This helps us extract information or a string from our expression. In my expression we can see that we have two types of capturing 
groups. One is (), ie ([a-z]+) which extracts a string value between lowercase a to z. Second one is ?:, ie ?:> which helps us stop 
extracting at the ">".

### Bracket Expressions
Match the strings within []. In my example, [a-z] matches a string that has anything from lowercase a to z. Another example for this is:
 
 [A-Z] - matches a string from uppercase A to Z

### Greedy and Lazy Match
Greedy and Lazy quantifiers are  * + {}. They expand the match as far as they can through the provided text. In my example, ([a-z]+) 
matches an characters included within <>

### Back-references
Back references like \1 matches the same text that was matched by the first capturing expression. In my example, \1 will match whatever 
is inside these <> that we captured

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
