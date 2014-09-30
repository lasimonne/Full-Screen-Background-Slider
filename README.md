Full-Screen-Background-Slider
=============================

A simple HTML + CSS Fullscreen Background Slider, no extra markup

## HTML

```html
<!doctype html>
<html>
    <head>
        <meta charset="utf-8">
        <meta name="viewport" content="width=device-width, initial-scale=1">
        <title>Full-Screen Background Slider</title>
    </head>
    <body>
    </body>
</html>

```


##[Sass](http://sass-lang.com/) + [Bourbon](http://bourbon.io)

```sass
body
	background: $img-1 no-repeat
	background-size: cover
	
	&::before, &::after
		content: ""
		+position(absolute, 0 0 0 0)
		z-index: -10
	&::before
		background: $img-2 no-repeat
		background-size: cover
		left: -100% 
		+animation(bg-slider 12s $ease-in-out-back infinite) 

	&::after
		background: $img-3 no-repeat
		background-size: cover
		left: -100% 
		+animation(bg-slider 12s $ease-in-out-back 6s infinite) 

+keyframes (bg-slider)
	12.5%
		left: 0 
	25%
		left: 0
	37.5%
		left: 100%
	75%
		left: 100%
	100%
		left: 100%
```

## Licensing

This code snippet is licensed under a [BY-SA Creative Commons License](http://creativecommons.org/licenses/by-sa/3.0/). You have the freedom to copy, adapt, and transmit this resource in any manner you see fit.

### Images
All images by [codeondesign](http://codeondesign.cu.cc)
