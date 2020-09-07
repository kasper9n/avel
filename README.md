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

these_are_equivalent:
  - 5, "nok"
  -
    - 5
    - nok

these_are_also_equivalent:
  - name: "mac", version: "1.16"
  -
    name: "mac"
    version: "1.16"
```

## Considerations

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
