---
title: str title-case
categories: |
  strings
version: 0.103.0
strings: |
  Convert a string to Title Case.
usage: |
  Convert a string to Title Case.
editLink: false
contributors: false
---
<!-- This file is automatically generated. Please edit the command in https://github.com/nushell/nushell instead. -->

# `str title-case` for [strings](/commands/categories/strings.md)

<div class='command-title'>Convert a string to Title Case.</div>

## Signature

```> str title-case {flags} ...rest```

## Parameters

 -  `...rest`: For a data structure input, convert strings at the given cell paths.


## Input/output types:

| input        | output       |
| ------------ | ------------ |
| list\<string\> | list\<string\> |
| record       | record       |
| string       | string       |
| table        | table        |
## Examples

convert a string to Title Case
```nu
> 'nu-shell' | str title-case
Nu Shell
```

convert a string to Title Case
```nu
> 'this is a test case' | str title-case
This Is A Test Case
```

convert a column from a table to Title Case
```nu
> [[title, count]; ['nu test', 100]] | str title-case title
╭───┬─────────┬───────╮
│ # │  title  │ count │
├───┼─────────┼───────┤
│ 0 │ Nu Test │   100 │
╰───┴─────────┴───────╯

```
