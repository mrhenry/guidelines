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


