# Title (replace with your title)

Regex are a series of symbols,numbers, and other characters that has to be searched from within a bigger set of documents or text.

## Summary

the regex in this document will allow you too match for a url.URL can be very important where as its part of a devlopers toolkit when creating scripts that needs valdation.
the regex below are for URL Matching
/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/
## Table of Contents


## Regex Components
Regex can be very confusing for anyone's first time. however, to better understand it, one should look at each component seperately.
Every regex are wrapped with foward slashes to identify themselves. 
Backslashes in regex are basically escape character that shws the character preceding to its literal context. To better understand lets take a look at the components
### Anchors
The anchor is a special character, often referred as a token, which does not match any other character. in case of our regex, the caret is used to define the beginning of the string or line and the "$" indicates the end.
Caret - ^

Dollar Sign - $

/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/
### Quantifiers
Quantifiers
The Quantifiers "quantify" or specify the number of instances that the character(s) show up within the text.

In the case of URL matching, the following quantifiers are used:

The following ? is used to indicate that the s is not required and thus https or http are both possible matches.

https?

The following ? is used after https:// to indicate that this prefix may not be necessary in the URL.

(https?:\/\/)?

This third "?" is used at the end to indicate the forward"/" slash may or may not be present, however, both are acceptable. Note the foward slash is used to indicate that the back slash should be referenced in its literal sense.

\/?

The curly braces are also quantifiers that can be used to determine the {2,6} indicates that the web extention or top-level domain following the dot (.) may contain from 2 up to 6 characters (ex. .ca or .com, etc).

[a-z\.]{2,6}

The plus sign is used to match one or more of the preceding characters.

([\da-z\.-]+)

The asterisk is used to match zero or more of the preceding characters.

([\/\w \.-]*)*

/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/

### Character Classes
The character class matches any of the characters enclosed within the brackets.

The following includes digit, characters a through z plus it includes the period and hypen character.

[\da-z\.-]

The following includes the characters a through z plus the period character.

[a-z\.]

The following includes the back slash, any word character (\w), period, plus the hyphen character.

[\/\w \.-]

/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/

### Flags
The URL Matching Regex does not have any flags.

For reference, flags are used to present how matches are performed.

For example, the "g" flage looks for a global match, rather than just the first match. The "i" flag matches for both the uppercase and lowercase character.

### Grouping and Capturing
Grouping and Capturing is a way for regex to treat a set of characters as one unit. It is denoted by a pair of parentheses.

The following grouping is to categorize the protocol portion of the URL.

(https?:\/\/)

The following grouping categorizes the digits, letters, dots, and hyphens that could follow the http(s) protocol.

([\da-z\.-]+)

The following categorized the extension that will contain letters and dots.

([a-z\.]{2,6})

And finally, the last grouping categorizes the optional files and directories that the URL may contain.

([\/\w \.-]*)

/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/



## Author
Cuong Tran
gmail: nhoismee@gmail.com
repository: https://github.com/Tran93/Regex-Tutorial