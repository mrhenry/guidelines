[[BACK]](README.md)

# Javascript

✓ — Always end statements with a colon

```js
console.log("Hello World");
```

✓ — Always declare your variables with the `var` statement.

```js
var my_nice_and_descriptive_variable = "Hello World";
```

✓ — When working on a Mr. Henry project, ALWAYS use CommonJS to manage your javascript dependencies.

✗ — Never use global variables. ALWAYS use the `var` statement! (Or, I, @fd, will make you suffer.)

✗ — Never include micro-jQuery-plugins. If you can write it in 20 LOC, write it yourself.


## Conditions

✗ — ``if ( !(typeof foo === "undefined" ) )``

✓ — ``if ( foo !== undefined )``


## Comments

Always document your code in human understandable language. Try to write what your function / module is doing. If a function excepts paramaters and/or returns a value, describe what these are for & what you intended them to be. Use the [JSDoc syntax](http://en.wikipedia.org/wiki/JSDoc) as a reference.

If you use Sublime Text, you can install this plugin to make this easier:  
[https://github.com/spadgos/sublime-jsdocs](https://github.com/spadgos/sublime-jsdocs)


## Functions

[Best function explanation ever](http://markdaggett.com/blog/2013/02/15/functions-explained)
