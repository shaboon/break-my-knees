# Regex Tutorial: Regex URL

Regex, or regular expression, is perplexing and even daunting at first glance. The string of regex itself doesn't make much sense at first glance. However, within this gist, I will do my best to explain it.

## Summary

The following is a regex example of a search for URLs:\

`/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/`\

Within this gist we will break down and dissect the string into its individual components.\

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

Regex itself is strings used to search and find strings inside the body of something. As such, it utilizes phrases as logic in searching for specific parts. We will break them down now.\

### Anchors

The characters "^" and "$" are anchors.\

The "^" means the start of the string and will apply all given criteria after it.\
Ex. /^[search text]

Whereas, the "$" symbolizes the end of the string and applies the characters/criteria that come before it.
Ex. [search text$/]

### Quantifiers

Quantifiers are used to set limits on matching behaviour. While the previous section covered behaviour on where it searched for

### Grouping Constructs

### Bracket Expressions

The "[]" specify the space by which criteria can be applied. While not a limit character wise, it does allow for more accurate end points without hardcoding character limits.\

### Character Classes

Characters in a regex search can be designated and limited via what is assigned. In this section we will cover how you can choose the given characters inside a regex.\

### The OR Operator

### Flags

### Character Escapes

## Author

My name is Sean Haboon, and thank you for reading through this gist.
