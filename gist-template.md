# Regex Tutorial

Regular expressions (regex) are special strings that are used for searching text. They can describe not only literal text, text patterns and are a great tool in text processing. The regex can be used to find text that conforms to a specific set of rules, something that follow a pattern. The common text patterns that we encounter in everyday documents include social security and account numbers, emails, phone and credit card numbers, street addresses, dates, SKU codes, web addresses and etc. Ordinary text search can be only used to find fixed text strings, for example a specific phone number or email address. Regular expressions can be used to find any valid street addresses or only addresses from a specific area codes or locations. This is where we can use regex to narrow down.

## Summary

The purpose of this tutorial is to provide an expression to search for hex values as well put together a general understanding for regex. By the end of this tutorial you will have a undestanding on how to use regular expressions on a basic level and become more fluent with regex syntax.

 /^#?([a-f0-9]{6}|[a-f0-9]{3})$/

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

* Anchors belong to the family of regex tokens, they dont neccesarily match any of the characters but they notate something particular about the string in the matching process. In this instance we will be looking at both "^" and "$" anchors. 

* "^" Can be used to search for characters in which the ^ notates the start of the line. Example, if we had a string that stated "Baseball is the best sport" "^B" would highlight the 'B' in Baseball saying thats where the line of code starts.

* "`$`" Can be used to search for keys words that end in which ever string or character is put infront of the "`$`" tag. Example, if we wanted to search for google email(s) we could use "gmail.com$" in order to parse that specific data from the entirety of emails we were searching through. 

### Quantifiers

* In this section we will cover quantifiers. Quantifiers can be only be used in a working pair with other tags, they cannot be used by themselves. Simply put, quantifiers specify how many instances of a character, group, or character class must be present in the input for a match to be found.

* Lets take a look at the given code we have above (I'll pull it down here for you) <br>
<br>    /^#?([a-f0-9]{6}|[a-f0-9]{3})$/  
<br>    If we can pick this apart and focus on the {6} noted after the [a-f0-9]. The "6" between the curly brackets are stated we want six characters in "a-f" or "0-9". It can be used in any combination, however it must return letters between a-f and numbers 0-9 only.

* The "?" tag is the other quantifer we want to take a look at in our given code above. The "?" follows that "#" character is simply saying even if the string were looking for might not include a "#", even if its not in the string go ahead and highlight the string if everything else matches.


### OR Operator

* The tag "|" used as an OR operator, meaning it will return matching info on either side of the "|". <br>
<br>    ([a-f0-9]{6}|[a-f0-9]{3}) 
<br>

* The expression given will return 6 character length string of characters of "a" through "f"/"0" through "9" OR a 3 character string length 

### Character Classes

* "." is like an all search. It will highlight anything except for a line break (\n).
* "\d" refers to "digit". Essentially it is anything "0" through "9".
* "\s" refers to a space, line breaks, and tabs (basically any blank space).
* "\w" refers to alphanumeric characters (Uppercase and lowercase A-Z, 0-9, and the "_" or underscore).

### Flags

* A flag is an optional parameter that modifies that search condition in a regex hex value locator.<br> 
    * "g" is a global search, meaning it will try every character within a string to see if it matches the constraints.

    * "i" changes your search to be case-insensitive, so even if you search for "BALL", "ball" will still return highlight.

    * "m" is for a multiple line search.

### Grouping and Capturing

* Grouping and Capturing using "()". Parenthesis can be used to group a string for a single search. Looking at our hex value locator "([a-f0-9]{6}|[a-f0-9]{3})", we have multiple tags ("[ ]","|","{}") that we use in conjunctions inside our "()".

### Bracket Expressions

* Bracket expressions "[ ]" can note a range of characters in which we allow searching. In our sample hex value locator we have "[a-f0-9]". By using the "-" hyphen we will look for letters a through f and numbers 0 through 9. Our expression  will specifically be looking for these characters "a-f" or "0-9". 

### Greedy and Lazy Match

* Regex will return a "greedy" match by default, meaning the match will be as long as possible. We can use "?" to opt for a "lazy" match instead, meaning the match will return as short as possible. 
* Example: we have a string "abcdefghijkc" and the expression "a.*c" we're going to start at "a" through "c" a greedy match will return "abcdefghijkc" and a lazy match will return "abc" once the lazy hits the first "c" it stops.

### Boundaries

* A word boundary can occur in one of three positions: 
1. Before the first character in the string 
2. After the last character in the string
3. Between two characters in the string, notating a word character

* Example: 

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)

<!-- Greedy: Keep searching until condition is not satisfied.
Lazy: Stop searching once condition is satisfied. -->
