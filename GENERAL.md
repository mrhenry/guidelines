[[BACK]](README.md)

# General

## Be nice to your collegues

When you write code, you will understand it still a day after, maybe a week or a month after. But after a couple months, it's vague. 

Now imagine that you didn't even written that code. Therefore it's important to make your code as readable & understandable as possible. 

Adding comments where needed, even just to say that a parameter has to be boolean or a string, or sum up the cases in written language. It's maybe time consuming, but debugging misty code can kill kittens!

Joh

![Kitten](http://cl.ly/image/3q3u1N1D3I1D/0027.jpg)

## Commit often & use proper messages

Committing often gives you the power to go back a few steps when needed. Commit related blocks of code.

Using proper commit messages can help debugging. Let's say you remember that everything was OK before updated that one plugin. Open up your commit history and start digging what was actually changed, find it, patch it, fistpump delightfully.

### How to commit message

✗ — ""

✗ — "Updated"

✗ — "Updated header"

✓ — "Nugded that header a few pixels up, updated jQuery plugin tralala to version x.x.x"

✓ — "Goddamn client wants me to change that thing again, I've now implemented a way that we can do blablabla"


## Variable names

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
