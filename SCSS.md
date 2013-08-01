# SCSS

## Style by modules, not by pages

One of the eyeopeners we had last year was that styling by page can work in small sites, but can become a real hassle when updates lurking around the corner. The talk [Modular & reusable front-end code](http://youtu.be/T6-75HdADc8) by Roy Tomeij changed our point of view and made us create styles by modules.

### File structure

```
|– stylesheets
  |
	|- base
		|
		|- _base.scss
		|- _fonts.scss
		|- _variables.scss
		|- …
	|- lib
		|- _jquery-ui.scss
	|- modules
		|- _footer.scss
		|- _header.scss
	screen.scss
```


### Code formatting

Readability is king. Try to keep up with these formatting rules, because they can make everybody's life a lot easier.

```scss
// Every property on a new line & sort them alphabetically.
// Always a space between : and the property.
.selector {
	background-color: white;
	color: black;
	padding-bottom: 0;
	padding-top: 10px;
}
```

```scss
// Keep properties of a selector together to avoid redeclaration somewhere else.

// Don't do this
.selector {
	background-color: white;
	color: black;
	padding-bottom: 0;
	padding-top: 10px;
}

.selector {
	margin: 0 auto;
}

// But do this
.selector {
	background-color: white;
	color: black;
	margin: 0 auto;
	padding-bottom: 0;
	padding-top: 10px;
}
```

```scss
// Try to avoid shorthands, except for margin & padding.
.selector {
	background-color: white;
	background-image: url('/logo.png');
	background-size: cover;
	margin: 0 0 10px 0;
}
```

```scss
// Always end your property with ;
.selector {
	background-color: white;
}
```

```scss
// Includes & extends always in the beginning. Except when you explicitly want to do it after, but then comment why. 
.selector {
	@include border-radius(50%);
	@include transition(opacity 300ms);
	@extend %extendable;
	background-color: white;
	
	// Extend after config because of media-queries inside this extend
	@extend %extendable-extension;
}
```

```scss
// Declare your variables in the correct scope
$body_text_color: red; // Global

.selector {
	$body_text_color: blue; // Only in scope of .selector
}
```

### Use Compass mixins

The whole list of available Compass mixins: [http://compass-style.org/index/mixins/](http://compass-style.org/index/mixins/)

### Transitions

Always specify which property you want to animate.

✗ — ``@include transition(all 300ms);``

✓ — ``@include transition(background-color 300ms, width 300ms);``

✓
```scss
@include transition-property(background-color, width);
@include transition-timing-function(300ms);
```
