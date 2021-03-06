[[BACK]](README.md)

# General

## Be nice to your collegues

When you write code, you will understand it still a day after, maybe a week or a month after. But after a couple months, it's vague. 

Now imagine that you didn't even written that code...

Therefore it's important to make your code as readable & understandable as possible. 

Use describing variable names. Sometimes 10 lines of code is much more readable than that one cool fancy line you read about that will boost perfomance by a millivanillisecond. Adding comments where needed, even just to say that a parameter has to be boolean or a string, or sum up the cases in written language. It's maybe time consuming, but debugging misty code can kill kittens!

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

Variable names (all identifiers, really) should always be descriptive.
There is no sense in using *letters*, *acronyms* or *abbreviations*.  
Don't try to be clever!  
Don't try to make your code *small*!  
There are **no** performance benefits in using shorter-than-necessary names.


✗ — Letters

✗ — Acronyms

✗ — Abbreviations

✓ — Length scales with scope

### The length-scope relation

#### Short scope:

- loop index counters can be called (`i`, `j`, `k`)

```js
for (var i = 0; i < 100; i++) {
  // ...
}
```

**Note:** The only allowed *letter identifers* are:
- `i`, `j`, `k` for loop counters
- `x`, `y`, `z` for dealing with coordinate spaces.
- `m`, `n` for dealing with opaque members of a collection. (opaque here means that you will not be using the member itself).

#### Medium scope:

- variable names inside methods/functions

```js
function example_function() {
  var posts,
      authors;
  // ...
}
```

#### Long lifetime

- global variables
- constants
- class/module names
- method names

```ruby
GOOGLE_ANALYTICS_API_KEY = "..."

class Event::Location
  # ...
end

def render_comments_for_blog_post(post)
  # ...
end
```

## External dependencies (Gems, CommonJS packages, jQuery plugins, (S)CSS libraries)

✗ — Never add a dependecy unless you REALLY nead it.

✗ — Never, ever, use *micro plugins/gems/packages* ... **NOT EVER**

✓ — Use as few as possible external dependecies.

✓ — If you can, write it yourself.
