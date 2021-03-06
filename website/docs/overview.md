---
id: overview
title: Overview
---

Comby provides a lightweight way of matching syntactic structures of a program's
parse tree, like expressions and function blocks. Comby is language-aware and
understands basic syntax of code, strings, and comment syntax many languages.

<style>
blockquote {
    background-color:#00000000;
    border-left: 8px solid #ffa504;
}
</style>

> **The bottom line:** Comby lets you search and change many kinds of code structures with
greater ease than what regular expessions alone allow.


### The basic idea

Comby works by defining general parsers for code constructs like balanced `(...)`,
`{...}`, and `[...]`, as well as string literals and comments. It doesn't
implement a full parser for every language, but rather a more general grammar so
that it works on a lot of languages (just like regular expressions work on the
text of every language).

### Does it work on my language?

Comby implements basic parsers for the
following languages:

<style>
table {
    margin-left:auto;
    margin-right:auto;
}
table thead {
 visibility: collapse;
}
table td {
    border: none;
}
table tr:nth-child(2n) {
  background-color: transparent;
}

</style>


|            |            |         |            |         |      |       |       |
|------------|------------|---------|------------|---------|------|-------|-------|
| Bash       | C          | C++     | C#         | Clojure | CSS  | Dart  | Elm   |
| Elixir     | Erlang     | Fortran | F#         | Go      | Hask | HTML  | Java  |
| Javascript | JSX        | JSON    | Julia      | LaTeX   | Lisp | Nim   | OCaml |
| Pascal     | PHP        | Python  | Reason     | Ruby    | Rust | Scala | SQL   |
| Swift      | Plain Text | TSX     | Typescript |         |      |       |       |

Comby also implements a generic matcher that works as a fallback parser for data
formats similar to JSON, new languages, and existing ones that may not have
explicit support yet (like YAML or VHDL). You can also
[write your own language definition](advanced-usage#custom-language-definitions)
if the generic matcher falls short.
