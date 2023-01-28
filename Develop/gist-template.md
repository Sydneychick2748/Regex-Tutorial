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
In the regular expression "/^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/" the anchors are the "^" and "$" symbols. These symbols are used to specify the start and end positions of the match, respectively.

The "^" anchor is placed at the beginning of the regular expression and specifies that the match must start at the beginning of the string. For example, the regular expression "/^([a-z0-9_.-]+)/" will only match a string that starts with one or more letters, numbers, underscores, dots or dashes

The "$" anchor is placed at the end of the regular expression and specifies that the match must end at the end of the string. For example, the regular expression "/([a-z.]{2,6})$/" will only match a string that ends with two to six letters.

In this case the regular expression is looking for a string that starts with one or more letters, numbers, underscores, dots or dashes, followed by an @ symbol, followed by one or more letters, numbers, dots or dashes, followed by a dot and two to six letters and end of the string. This pattern of string is used to match an email address.



### Quantifiers
In the regular expression "/^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/" the qualifiers are the "+" and "{2,6}".

The "+" symbol is a quantifier and it is used to specify that one or more of the preceding character or group is to be matched. For example, in the regular expression "/^([a-z0-9_.-]+)/" the "+" following the character class "[a-z0-9_.-]" specifies that one or more letters, numbers, underscores, dots or dashes must occur in the matching string.

The "{n,m}" symbol is another quantifier and it is used to specify a range of occurrences for the preceding character or group. For example, in the regular expression "/([a-z.]{2,6})/" the "{2,6}" following the character class "[a-z.]" specifies that the match must occur between 2 and 6 times in the matching string.

So in this regular expression, the "+" qualifier is being used to match one or more of the preceding character or group which is letters, numbers, underscores, dots or dashes, and the "{2,6}" qualifier is being used to match between 2 and 6 occurrences of the preceding character or group which is letters or dots.



### OR Operator
The OR operator is not present in the regular expression "/^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/" The OR operator is typically represented by the pipe symbol "|" and is used to match one of multiple possible patterns. In this regex, there is no use of the OR operator. Instead, the regex uses a combination of characters classes, quantifiers, and anchors to match a specific pattern of an email address.



### Character Classes
In the regular expression "/^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/" character classes are used to define the acceptable characters that can be matched in certain parts of the email address.

For example, the character class "[a-z0-9_.-]+" is used in the first capturing group and matches one or more characters that are either lowercase letters, digits, an underscore, a period, or a dash. This group is used to match the local part of the email address.

The character class "[\da-z.-]+" is used in the second capturing group and matches one or more characters that are either digits, lowercase letters, a period, or a dash. This group is used to match the domain name of the email address.

The character class "[a-z.]{2,6}" is used in the third capturing group and matches a sequence of 2 to 6 characters that are either lowercase letters or a period. This group is used to match the top-level domain of the email address.

These classes of characters make sure that the email addresses follow the correct format.




### Flags
The regular expression provided, /^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/ does not contain any flags.

A flag is a special character that modifies the behavior of the regular expression. For example, the 'g' flag is used to perform a global search, and the 'i' flag is used to perform a case-insensitive search.

The regular expression provided only contains characters and special characters that define the pattern that the regular expression is trying to match.



### Grouping and Capturing
In the regular expression "/^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/" the brackets () are used for grouping and capturing. Grouping allows you to group together certain characters and apply a quantifier to them as a whole. Capturing allows you to extract the matched text from the group. In this regex, there are three groups:

1. ([a-z0-9_\.-]+): This group captures one or more characters that are either lowercase letters, digits, underscore, period or dash.
2. ([\da-z\.-]+): This group captures one or more characters that are either digits, lowercase letters, period or dash.
3. ([a-z\.]{2,6}): This group captures two to six characters that are either lowercase letters or period.
These groups allow you to extract specific parts of the matched email address, such as the username, domain name, and top-level domain.



### Bracket Expressions
 In the regular expression /^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/, the bracket expressions are used to define character sets. For example, [a-z] matches any lowercase letter, [a-z.] matches any lowercase letter or a period, [a-z.]{2,6} matches any lowercase letter or a period between 2 and 6 times.
The first bracket expression, [a-z0-9_.-]+, matches one or more characters that are a lowercase letter, a digit, an underscore, a period, or a hyphen.
The second bracket expression, [\da-z.-]+, matches one or more characters that are a digit, a lowercase letter, a period, or a hyphen.
The third bracket expression, [a-z.]{2,6}, matches two to six lowercase letters or periods.
These bracket expressions are used to define the format of the email address being matched.


### Greedy and Lazy Match
This regular expression does not use any greedy or lazy match qualifiers. The regular expression uses anchors (^ and $), character classes (a-z, 0-9, , ., -), grouping and capturing ([a-z0-9.-]+), and bracket expressions (a-z.) to match a specific pattern of an email address. Greedy and lazy match qualifiers are used to specify whether a quantifier should match as much of the input as possible (greedy) or as little as possible (lazy) in order to find a match. They are represented by the characters *? +? {n,m}? in the regex.


### Boundaries
The regex you provided, /^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/, does not have any specific elements that pertain to boundaries.
Boundaries in regular expressions refer to specific characters or character combinations that indicate the beginning or end of a line, word, or other unit of text.
Examples of boundary characters include the caret (^) and dollar sign ($), which indicate the start and end of a line respectively, and the word boundary (\b) which matches the position between a word character and a non-word character.
Boundaries are typically used to ensure that the match occurs at a specific location within a string, rather than anywhere within the string.



### Back-references
The regular expression you provided does not use any back-references. Back-references allow you to reuse a previously captured group in the same regular expression. The syntax for a back-reference is usually a backslash followed by the group number, such as \1 for the first group, \2 for the second group, and so on. For example, the regular expression /(a)\1/ would match the string "aa" because it is looking for an "a" character followed by the same "a" character that was captured in the first group.



### Look-ahead and Look-behind
This regex does not contain any look-ahead or look-behind constructs. Look-ahead and look-behind are special types of assertions that allow you to check for a certain pattern either before or after the current position in the string, without including the matched characters in the final result. They are represented using the (?=), (?!), (?<=) and (?<!) constructs, respectively.




## Author

This tutorial was created by Ana Bennett. If you would like to contact me at anabennett77@gmail.com
 
 If you want to see more of my work visit my github: https://github.com/Sydneychick2748


