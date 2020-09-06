# AVEL (in-development)

A Very Eh Language

AVEL is a human-friendly, minimal and sensible configuration language.

## Example

```
# This is a comment

name: "AVEL"
author: "Kasper Henningsen"
year: 2020
very_cool: true
homepage: null

tags:
  - "avel"
  - "eh"

dependencies:
  YAML: "^1.2.0"
  JSON:
    version: "^1.2.0"
    comments_enabled: true
```

## Considerations

### Lists

Dash syntax:
```
list:
  - "one"
  - "two"
```
- Easy to read
- Inconsistent with a short-form syntax

Comma syntax:
```
list: "one", "two"
```
- Easy to read
- Needs a multiline form to go with it

Multiline comma syntax:
```
list2:
  "one",
  "two"
```
- Consistent with short-form comma syntax
- Hard to read when there are both lists and objects

Bracket syntax:
```
list: [ "one", "two" ]
list2: [
  "one",
  "two"
]
```
- Consistent between forms
- Trailing comma?
- Would like to avoid brackets

### Numbers

Shoudl the following be supported?
- Hexadecimal
- Octal
- Binary
- Exponents
- Infinity
- Separators

### Strings

Double quote strings:
- Lets you escape characters

Single quote strings:
- What you see is what you get

### Multiline strings

Triple quotes syntax:
```
list:
  - """
    block
    of
    text
  """
```

Triple quotes block syntax:
```
list:
  - """
    block
    of
    text
    """
```
- Potentially problematic if your indentation is 4 characters

Triple quotes newline block syntax:
```
list:
  -
    """
    block
    of
    text
    """
```

Pipe syntax:
```
list:
  -
    | block
    | of
    | text
```
- Doesn't look great
