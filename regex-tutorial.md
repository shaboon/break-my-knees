# Regex Tutorial: Regex URL

Regex, or regular expression, is perplexing and even daunting at first glance. The string of regex itself doesn't make much sense at first glance. However, within this gist, I will do my best to explain it.

## Summary

The following is a regex example of a search for URLs:\

`/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/`\

Within this gist we will break down and dissect the string into its individual components.\

## Table of Contents

- [Anchors](#anchors)
- [Character Classes](#character-classes)
- [Bracket Expressions](#bracket-expressions)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Components

Regex itself is strings used to search and find strings inside the body of something. As such, it utilizes phrases as logic in searching for specific parts. We will break them down now.\

### Anchors

The characters `^` and `$` are anchors.\

The `^` means the start of the string and will apply all given criteria after it.\
Ex. /^[search text]

Whereas, the `$` symbolizes the end of the string and applies the characters/criteria that come before it.
Ex. [search text$/]

### Character Classes

Characters in a regex search can be designated and limited via what is assigned. In this section we will cover how you can choose the given characters inside a regex.\

The most general class that can be used to find matching cases is the `.`\
This class will find and match with all characters, taht being alphanumeric to even whitespace characters\
Such as: A-Z, a-z, 0-9, spaces, tabs and other special characters\

The next class is `\w`:\
This class will return all matching cases that are alphabetical values. That being A-Z, or a-z.\
However, it is important to note that this class does also include the "\_" as well.

A class to find numerical values is `\d`:\
This class will allow for the regex to search for a string that uses all arabic numbers from 0-9\

The last class that will be covered in this section is the `\s` class\
This class returns all whitespace characters to the user. As such you will recieve back any spaces (or tabs) and/or\
line-breaks within the space used.\

### Bracket Expressions

The "[]" specify the space by which criteria can be applied. While not a limit character wise, it does allow for more accurate end points without hardcoding character limits.\

### Quantifiers

Quantifiers are used to set limits on matching behaviour. While the previous section covered behaviour on where it searched for

### Grouping Constructs

### The OR Operator

### Flags

### Character Escapes

## Author

My name is Sean Haboon, and thank you for reading through this gist.
