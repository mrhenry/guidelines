# Mr. Henry - Code Style document

`✓` => YOU MUST FOLLOW THIS RULE.
`✗` => YOU MUST NEVER, EVER DO THIS.

## General

### Variable names

✓ — Variable names should NEVER be acronims.

✓ — They must scale with the lifetime of the value.

Short lifetime:
- loop index counters can be called (`i`, `j`, `k`)

```js
for (var i = 0; i < 100; i++) {
  # ...
}
```

Long lifetime:
- global variables
- constants
- class/module names
- method names
- variable names inside methods/functions

## Javascript

✓ — Always end statements with a colon

```js
console.log("Hello World");
```

✓ — Always declare your variables with the `var` statement.

```js
var my_nice_and_descriptive_variable = "Hello World";
```

✓ — When working on a Mr. Henry project, ALWAYS use Hanging Gardens to manage your javascript dependencies.

✗ — Never use global variables. (I, @fd, will make you suffer if you do.)

✗ — Never include micro-jQuery-plugins. If you can write it in 20 LOC, write it your self.
