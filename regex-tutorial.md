# Regex Tutorial: Regex URL

Regex, or regular expression, is perplexing and even daunting at first glance.\
The first step to understanding it would be to first define it...\
Regex or regular expressions are a series of special characters that define a search pattern that JavaScript can use to find non-hardcoded strings.

## Summary

The following is a regex example of a search for URLs:

`/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/`

Within this gist we will break down and dissect the string into its individual components.

## Table of Contents

- [Anchors](#anchors)
- [Character Classes](#character-classes)
- [Bracket Expressions](#bracket-expressions)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)
- [Post Summary](#post-summary)

## Regex Components

Regex itself is strings captured inside of "_* / *_" used to search and find strings inside the body of something. As such, it utilizes phrases as logic in searching for specific parts. We will break them down now.

### Anchors

The characters `^` and `$` are anchors.

The `^` means the start of the string and will apply all given criteria after it.\
Ex. `/^[search text]`

Whereas, the `$` symbolizes the end of the string and applies the characters/criteria that come before it.\
Ex. `[search text$/]`

### Character Classes

Characters in a regex search can be designated and limited via what is assigned. In this section we will cover how you can choose the given characters inside a regex.

---

The most general class that can be used to find matching cases is the `.`
This class will find and match with all characters, taht being alphanumeric to even whitespace characters\
Such as: A-Z, a-z, 0-9, spaces, tabs and other special characters

---

The next class is `\w`:\
This class will return all matching cases that are alphabetical values. That being A-Z, or a-z.\
However, it is important to note that this class does also include the `"_"` as well.

---

A class to find numerical values is `\d`:\
This class will allow for the regex to search for a string that uses all arabic numbers from 0-9

---

The last class that will be covered in this section is the `\s` class\
This class returns all whitespace characters to the user. As such you will recieve back any spaces (or tabs) and/or\
line-breaks within the space used.

---

### Bracket Expressions

The `[]` specify the space by which criteria can be applied. While not a limit character wise, it does allow for more accurate end points regarding the characters it may use.

For instance, say I would like to search the space for strings that contain letters `a" to "g", I can then use the bracket\
classes as such:

Ex: `[a-g]`

Furthermore, say there is a moment where I know that the section I'm looking for contains only numbers "5" through "8"...

Just like the previous example, I can use `[5-8]` to reduce the amount of matching cases to what I actually want.

### Quantifiers

Quantifiers are used to set limits on matching behaviour. While the previous section covered behaviour on what it searched for, these classes will set a limit on how many times it may match. This is useful because regex will always match as many times as possible. To make the returned information more exact or digestable, it would be wise to control how many times it may match.

The `*` class will match the pattern as many times as possible\
For example: say you are looking for the name of a website-route that might be 3 characters long to 50. To account for that, the `*` will include any patterns that do show up, but is not required

The `+` class will match patterns one or more times\
This class be used when length cannot be feasibly assumed and needs to be present

The `?` class will match patterns only once if it exists\
This class will allow a pattern to not be required but can be captured

The `{}` class provides a specific range based on what is given inside the curly-braces\
This ties well into the URL format as this can be applied for the TLD (ex. ".com", ".net") section of a URL where length can be guessed and appropriately established

- `{ n }` will match the value at minimum of whatever _"n"_ is set to
- `{ n, x }` will match at minimum of _"n"_ and at maximum of _"x"_

### Grouping Constructs

While not present in this example, group constructs make use of `:`

As a demonstration: `(123):(abc)` will find matches only of `(123):(abc)` and would exclude `(123):(cba)` or `(321):(abc)`\
That covers capturing group constructs, however, there are also non-capturing group constructs that use `?` and `?:`

When inside parenthesis, `?:` can be used (`/(?:https?:\/\/)?(?:www\.)?example\.com/`) to match the example but cut it from the result returning only _*"example.com"*_

### The OR Operator

The _OR_ class allows for minor flexibility within the search parameters.\
The character _|_ when used inside `()` fufills this role.

As an example, in `(a|b):(1|2)`, the follwoing cases would match:

- `(ab):(12)`
- `(ba):(12)`
- `(a):(1)`
- _and some more_

### Flags

Flags are used to set the behaviour of the search regarding how characters are treated.

- `g` sets the standard of a global search. The regex will test itself against all possible matches regardless of case within a string
- `i` sets a case-insensitive expectation where alphabetical case will not be considered when matching
- `m` allows for a Multi-Line search. In that a multiple line string will be treated as multiple lines.

### Character Escapes

This class, the `\` is very important. When found outside of `[]`, it can be used to find a character as a literal.\
That means it will be hard-coded to find the next character as a match as opposed to whatever class it may be otherwise.

As an example:\
`/^...]+)\.([a-z...` will find whatever pattern comes before it and then just a `"."` and attach the next pattern\
Resulting in... `blah.blahagain`

### Post Summary

Looking back at the given URL regex, we can divide it into sections as such:

`/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/`

_Lets Start:_\
`^` means the start of the string

_Then as the first section of the query:_\
`(http)` is softly included and will be clarified furtherdown the full-breakdown\
`(s?)` indicates that matches can include an "s" thereby also matching `"https://"`\
`...\/\/)?` results in the final section that allows for the regex to include any matching cases of `"https://"` or `"http://"`

_Next Comes:_\
`([\da-z\.-]+)`

_Where:_\
`[/da-z]` sets the characters it will be looking for, that being only alphanumeric characters and the special characters "." and "-"\
`]+` sets the pattern to search for at least one matching case

_Additionally:_\
`([\/\w \.-]*)` includes any alphanumeric character that can be found at an length as to cover possible routes by which the link may have

_Finally..._\
`$` signifies the end of the string. bringing the regex to a close.

## Author

My name is Sean Haboon, and thank you for reading through this gist.

To look into my activity, go to my GitHub:\
https://github.com/shaboon
