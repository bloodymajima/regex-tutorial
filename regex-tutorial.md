# Regex Tutorial

In this tutorial, I will be going over the regular expression, or Regex, for URLs. 

## Summary

We will go over the Regex for matching a URL: 

`/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/`

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

Denoted with a vertical line character |, the OR operator tells the engine to allow only between the two specified characters. An example of this would be: `ap|ple` is translated to `ap` or `ple`.  We do not use this symbol in our URL regex. 

### Character Classes

Also called character sets, character classes tell the engine to match only one out of several characters. An example would be using a hyphen inside of a character class, to specify a range of characters. Example: `[e-h]` would translate into `[efgh]`. 

### Flags

Flags are used after a closing slash in regex and can change how an expression behaves. An example would be the `/i` flag, which makes the regex case insensitive. 

### Grouping and Capturing

In our regex, we use capturing groups to extract the protocol, domain, and path segments. Escaped parentheses, `\(regex\)`, capture the text matched by the regex inside them, which allows you to apply regex operators to the entire grouped regex.

### Bracket Expressions

Brackets indicate a set of characters to match. In our URL regex, `[\/\w \.-]*` matches the path segment, which can contain letters, numbers, slashes, spaces, dots, and hyphens.

### Greedy and Lazy Match

Quantifiers are greedy by default, meaning it will match as many characters as possible. In our regex, the `*` quantifier is greedy. If you want your regex to match as little as possible, you can use `*?`.

### Boundaries

Short for word boundaries in this context, boundaries match a sequence of letters or digits on their own, or at the end or beginning of a sequence of characters. For example, the regex `\bcat\b` would match `cat`, but not words like `catch`, or `locate`. If we remove one boundary, like `\bcat` or `cat\b`, it would match `catfish` or `tomcat` respectively. We do not use this in our URL regex.

### Back-references

A backreference is a way to match the same text as previously matched by a capturing group. An example would be: `(['"]).*?\1`. This will match a single or double quoted string, using a backreference to to refer to the open symbol, so it can match at the end. You can reuse the same backreference, as well. We do not use this in our URL regex.

### Look-ahead and Look-behind

Look-ahead and look-behind are used to define that particular pattern is (or isn't) ahead of or behind the current position. For example: `(?=foo)` asserts that what follows the current position in the string is `foo`. Alternatively, `(?<=foo)` means that what immediately precedes the current position in the string is foo. We do not use this in our URL regex.

## Author

My name is M, and I created this tutorial as part of a homework assignment of UofM's Full Stack Web Dev bootcamp program. 
You can find my Github [here](https://github.com/bloodymajima).
