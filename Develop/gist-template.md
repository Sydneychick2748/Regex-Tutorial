# REGEX_TUTORIAL

This tutorial will provide an overview of regular expressions, also known as Regex, and how they can be used to match specific character patterns within a string. Regular expressions are useful for extracting information from text and for validation purposes. One example of this is using regular expressions to match email addresses. The tutorial will also cover the different components of regular expressions, providing a deeper understanding of how they work and how to use them effectively.

## Summary

This code is a regular expression that can be used to match and validate email addresses. It can be used to check if an email follows the correct format, for example, it checks that the email address starts with one or more letters, numbers, underscores, dots or dashes, followed by an @ symbol, followed by one or more letters, numbers, dots or dashes, followed by a dot and two to six letters. It can be used throughout the tutorial as an example to show how different components of regular expressions can be used to match specific patterns in text.

Matching an Email – /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

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
In regular expressions, anchors are special characters that match the position of a string, rather than a specific character. The two most commonly used anchors are the "^" (caret) and "$" (dollar sign) characters.

The "^" anchor is used to match the start of a string, while the "$" anchor is used to match the end of a string. For example, the regular expression "^A" will match any string that starts with the letter "A", while the regular expression "z$" will match any string that ends with the letter "z".


### Quantifiers
In regular expressions, qualifiers are special characters that specify how many times a preceding character or group of characters should be matched. They are used to specify the quantity of the preceding characters, group or character class.

The most common qualifiers are:

 "" (asterisk) which matches zero or more of the preceding character or group. For example, the regular expression "a" will match zero or more occurrences of the letter "a".

"+" (plus) which matches one or more of the preceding character or group. For example, the regular expression "a+" will match one or more occurrences of the letter "a".

"?" (question mark) which matches zero or one of the preceding character or group. For example, the regular expression "a?" will match zero or one occurrences of the letter "a".

"{n}" where n is a number, which matches exactly n of the preceding character or group. For example, the regular expression "a{3}" will match exactly 3 occurrences of the letter "a".

"{n,m}" where n and m are numbers, which matches at least n and at most m of the preceding character or group. For example, the regular expression "a{2,4}" will match 2 to 4 occurrences of the letter "a".


### OR Operator
In regular expressions, the "|" (pipe) symbol is used as the "OR" operator. It is used to match one of several possible characters or patterns. The "|" operator is used to separate the different patterns that you want to match, and it will match any of the patterns that are separated by the operator.

For example, the regular expression "cat|dog" will match any string that contains the word "cat" or the word "dog".

You can also use parenthesis to group the different pattern you want to match and apply the operator on the group. For example, the regular expression "(cat|dog)s" will match any string that contains the word "cats" or the word "dogs".

### Character Classes
In regular expressions, character classes are a way to match any one character from a set of characters. They are defined within square brackets "[ ]" and they match any single character that is contained within the brackets.

For example, the regular expression "[abc]" will match any single character that is either "a", "b", or "c".

You can also specify a range of characters using a hyphen "-". For example, the regular expression "[a-z]" will match any single lowercase letter. The regular expression "[A-Z0-9]" will match any single uppercase letter or digit.

You can also negate a character class by adding a caret "^" as the first character within the brackets. This will match any single character that is not contained within the brackets. For example, the regular expression "[^abc]" will match any single character that is not "a", "b", or "c".

Regular expression engine have predefined character classes that you can use, such as \d for digits, \w for word characters (alphanumeric and underscore) and \s for whitespace characters.


### Flags
In regular expressions, flags are used to modify the behavior of the regular expression pattern. They are added after the last delimiter of the regular expression pattern, and they can be combined by concatenating them.

The most common flags are:

"i" (insensitive) flag makes the regular expression pattern case-insensitive, so it will match both uppercase and lowercase letters.

"m" (multiline) flag makes the caret (^) and dollar sign ($) characters match at the beginning and end of each line, rather than the entire string.

"s" (dotall) flag makes the dot (.) character match any character, including newline characters.

"x" (extended) flag allows the use of whitespace and comments in the regular expression pattern. This can make the regular expression pattern more readable.

"u" (unicode) flag makes the regular expression engine treat the pattern as a sequence of Unicode code points, rather than as a sequence of bytes.

For example, the regular expression pattern "/Hello/i" will match any string that contains the word "Hello" regardless of its case, while the regular expression pattern "/^Hello$/m" will match "Hello" if it appears at the beginning or end of each line in the input string.


### Grouping and Capturing
In regular expressions, grouping and capturing are ways to organize and extract parts of the matched text.

Grouping is done by enclosing a part of the regular expression pattern within parentheses "()". It groups together the enclosed characters as a single unit and allows you to apply operators and quantifiers to the entire group. For example, the regular expression "(cat|dog)s" will match "cats" or "dogs" but not "cat" or "dog" alone.

Capturing is a special form of grouping that creates a capturing group. It allows you to extract the matched text of the group for further use. The captured text can be referred to by its number or name. For example, the regular expression "(cat|dog)" will capture the matched text "cat" or "dog" and you can refer to it as $1 or $2, depending on the order they appear in the pattern.

Named capturing groups allow you to refer to the captured text by its name rather than its number. Named capturing groups are defined by enclosing the name of the group in angle brackets "< >" following the opening parenthesis. For example, the regular expression "(?<animal>cat|dog)" will capture the matched text "cat" or "dog" and you can refer to it as $<animal>.

Grouping and capturing can be used to extract certain information from a string, to validate certain patterns, or to replace certain parts of the matched text with other text.


### Bracket Expressions
Bracket expressions in regular expressions are a special type of character class that provide a concise way to match any one of a set of characters. They are defined within square brackets "[ ]" and they match any single character that is contained within the brackets.

A bracket expression can include individual characters, ranges of characters, and predefined character classes.

For example, the regular expression "[abc]" will match any single character that is either "a", "b", or "c". The regular expression "[A-Z0-9]" will match any single uppercase letter or digit.

There are several predefined character classes that can be used in bracket expressions. They are represented by a special character and match a specific set of characters.

For example, the regular expression "[\d]" will match any digit, the regular expression "[\w]" will match any word character (alphanumeric and underscore) and the regular expression "[\s]" will match any whitespace character.

Bracket expressions can be negated by adding a caret "^" as the first character within the brackets. This will match any single character that is not contained within the brackets. For example, the regular expression "[^abc]" will match any single character that is not "a", "b", or "c".

It's worth noting that bracket expressions are similar to character classes but they have some differences in the way they handle certain characters and predefined character classes.



### Greedy and Lazy Match
In regular expressions, "greedy" and "lazy" are terms used to describe the way the regular expression engine matches patterns.

A greedy match is the default behavior of the regular expression engine. It tries to match as much of the input string as possible while still satisfying the pattern. For example, the regular expression "." will match any number of any characters, including an empty string. If the input string is "Hello World", the greedy match of "." will match the entire string "Hello World".

On the other hand, a lazy match tries to match as little of the input string as possible while still satisfying the pattern. This can be achieved by adding a "?" immediately after a quantifier. For example, the regular expression ".?" will match any number of any characters, including an empty string. If the input string is "Hello World", the lazy match of ".?" will match an empty string.

The difference between greedy and lazy matching can be illustrated with a simple example. If you have the regular expression ".*foo" and the input string is "xfooxfoo", a greedy match will match the entire string "xfooxfoo" while a lazy match will match only "xfoo".

It's worth noting that greedy and lazy matching can be used in combination with other regular expression elements, such as character classes, groups, and anchors.



### Boundaries
In regular expressions, "boundaries" are special characters or character classes that represent the position of a character within a string. They are used to match the position of a character rather than the character itself.

There are several types of boundaries in regular expressions:

^: Matches the position at the start of a line.
$: Matches the position at the end of a line.
\b: Matches a word boundary (the position between a word character and a non-word character).
\B: Matches a non-word boundary (the position between two word characters or two non-word characters).
For example, the regular expression "^foo" will match the string "foo" only if it appears at the start of a line, the regular expression "bar$" will match the string "bar" only if it appears at the end of a line, the regular expression "\bcat\b" will match the word "cat" only if it appears as a whole word in the input text, and the regular expression "\Bdog\B" will match the substring "dog" only if it appears between two word characters or two non-word characters.

Boundaries can be used to match patterns at specific positions within a string and to validate the format of the input text. They are also useful for matching patterns that span multiple lines.

### Back-references
In regular expressions, "back-references" are used to match a previously matched pattern. They allow you to refer to a previously captured group within the regular expression.

Back-references are represented by a backslash followed by the group number, with the number indicating the order of the group in the pattern. For example, the regular expression "(\w+) \1" will match any word that is repeated twice in a row, with a space in between. In this case, the first group is "(\w+)", which captures any word, and the second group is " \1", which refers to the first group and matches the same word again.

Another example would be the regular expression "^([a-z]+) ([a-z]+)$" that will match any string that starts with a lowercase word, followed by a space, and end with another lowercase word. In this case, the first group is "([a-z]+)" which captures the first word, the second group is "([a-z]+)" which captures the second word, and the back-reference can be used for checking if the two words are the same or not.


Back-references can be very useful when you want to match a pattern that has a specific structure or repetition. They can also be used to validate the format of an input text or to extract specific information from a string.



### Look-ahead and Look-behind
In regular expressions, "look-ahead" and "look-behind" are special constructs that allow you to match a pattern based on the position of the characters, without including those characters in the final match.

Look-ahead is a positive assertion that specifies a pattern that must follow the current position in the input string, without consuming any characters. It is represented by the syntax (?=...) where the ... is the pattern to match. For example, the regular expression "foo(?=bar)" will match the string "foo" only if it is followed by the string "bar", but it will not include "bar" in the final match.

Look-behind is a negative assertion that specifies a pattern that must not follow the current position in the input string, without consuming any characters. It is represented by the syntax (?<=...) where the ... is the pattern to match. For example, the regular expression "(?<!foo)bar" will match the string "bar" only if it is not preceded by the string "foo", but it will not include "foo" in the final match.

It's worth noting that look-ahead and look-behind assertions must have a fixed length, meaning that the pattern that they match must have a fixed length. So, you can use them with quantifiers, such as *, +, ?, and {}.

Look-ahead and look-behind are useful when you want to match a pattern based on its context, rather than its content. They can be used to validate the format of an input text, to extract specific information from a string, or to check if a pattern appears in a specific position within a string.

## Author

This tutorial was created by Ana Bennett. If you would like to contact me at anabennett77@gmail.com
 
 If you want to see more of my work visit my github: https://github.com/Sydneychick2748


