# Regex Tutorial

In this tutorial, I will be going over the regular expression, or Regex, for URLs. 

## Summary

We will go over the Regex for matching a URL: 

`https?:\/\/(www\.)?[-a-zA-Z0-9@:%._\+~#=]{1,256}\.[a-zA-Z0-9()]{1,6}\b([-a-zA-Z0-9()@:%_\+.~#?&//=]*)`

We will be breaking down each part of this regex and explain its function.

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

Types of  URL regex anchors are a caret `^`, and a dollar `$`. These symbols specify the start and end of the string. It is recommended that you always use anchors, even when your regex would match without them. 

### Quantifiers

A quantifier tells the engine how many instances of its quantified token or subpattern can appear. 

### OR Operator

Denoted with a vertical line character |, the OR operator tells the engine to allow only between the two specified characters. An example of this would be: `ap|ple` is translated to `ap` or `ple`.  We do not use this symbol in URL regex. 

### Character Classes



### Flags

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
