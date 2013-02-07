# General

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
