# tree-sitter-ember

Tree-sitter grammar for the current Ember language revision.

This grammar targets the new Ember syntax in this repo, not the older Ember compiler syntax.

## Current coverage

- imports
- top-level `let` / `const`
- `struct`, `interface`, and `enum` declarations
- `impl T { ... }`
- plain function declarations
- generic type/function syntax with `<T>`
- `let` / `let mut`
- `if` / `else`
- `match`
- `^T` pointer types and `?T` optionals
- array literals and indexing
- postfix `++` / `--`
- struct literals: `.{ x = 1, y = 2 }`
- field access and method calls
- `comptime` parameters and prefix expressions
- structural `struct` / `interface` / `enum` type expressions
- `!!`, `??`, `catch`

## File extension

The grammar is configured for `.em` files.

## Development

```bash
tree-sitter generate
tree-sitter test
```

To validate the grammar against the compiler sample file:

```bash
tree-sitter parse ../EmberCompiler/x_test/struct_runtime.em
```
