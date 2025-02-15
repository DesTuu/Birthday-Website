[>Click here to check my simple project<](https://gorgeous-strudel-b7ed47.netlify.app/)

# HTML 
(Hyper Text Markup Language)

### 1. Inputs type
```
<input type="button">
<input type="checkbox">
<input type="color">
<input type="date">
<input type="datetime-local">
<input type="email">
<input type="file">
<input type="hidden">
<input type="image">
<input type="month">
<input type="number">
<input type="password">
<input type="radio">
<input type="range">
<input type="reset">
<input type="search">
<input type="submit">
<input type="tel">
<input type="text">
<input type="time">
<input type="url">
<input type="week">
```
---------------------------------------------------------------------------------------
### 2. Image
```
{% load static %}

<img src="{% static 'images/my_logo.png' %}" width= "300px" height="100px" alt="LOGO">
```
---------------------------------------------------------------------------------------
### 3. List
- Unordered (dots)
```
<ul>
	<li>
</ul>
```
- Ordered (1., 2., 3.)
```
<ol>
	<li>
</ol>
```
---------------------------------------------------------------------------------------
### 4. Span - inline
In opposite to div span makes changes in line text
```
<div>
	Underline only one <span>word</span>
</div>
```
---------------------------------------------------------------------------------------
# CSS 
(Cascading Style Sheets)

### 1. Centering image (only one thing)
```
img.my_logo {
width: 300;
height: 100;
display: block;
margin-left: auto;
margin-right: auto
}
```
display block is taking all the place in line

---------------------------------------------------------------------------------------
### 2. Centering more things
```
div.container{
display: flex;
justify-content: center
} 
```
can be also 
```
div.container{
display: flex;
justify-content: start, end, space-between, space-around
}
```
or for noobs
```
div.container{
text-align: center
} 
```
---------------------------------------------------------------------------------------
### 3. More classes in one
HTML Code
```
<div class="btn-wrapper italic">
<div class="container italic">
```
---------------------------------------------------------------------------------------
### 4. Web-saves Fonts (default)
```
body {
font-family: Verdana, Geneva, Tahoma, sans-serif;
}
```
If not Verdana: Geneva
If not Geneva: Tahoma
etc.

---------------------------------------------------------------------------------------
### 5. Margin (as clock direction)
```
body {
margin: 10 20 30 40
}
```
top right bot left
```
body {
margin: 10 auto
}
```
top/bot right/left

---------------------------------------------------------------------------------------
### 6. Image CSS Background
```
body {
background-image: url("../images/universe.png");
background-size: cover;
}
```
Don't copy absolute path, this will not work here.
Image should be in the right place, in directory of images.

---------------------------------------------------------------------------------------
### 7. Custom Fonts (link)
**Google Fonts**
[>Example Custom Font Orbitron<](https://fonts.google.com/selection/embed)
HTML
```
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400..900&display=swap" rel="stylesheet">
```
CSS
```
.orbitron-<uniquifier> {
  font-family: "Orbitron", serif;
  font-optical-sizing: auto;
  font-weight: <weight>;
  font-style: normal;
}
```
If font in body, buttons don't get them, we need to 
```
font-family: inherit;
```
---------------------------------------------------------------------------------------
### 8. Custom Fonts (downloaded)
[>1001 Fonts<](https://www.1001fonts.com/search.html?search=godfather)
```
@font-face {
src: url("../fonts/corleone/Corleone.ttf");
font-family: Corleone;
}
```
It's something like variable (pseudocode)
```
Corleone_ttf = os.get_file(path="../fonts/corleone/Corleone.ttf")
font.use(Corleone_tft)
```
---------------------------------------------------------------------------------------
### 9. Span in CSS - underline one word
```
.underline {
border-bottom: 2px solid white;
}
```
---------------------------------------------------------------------------------------
### 10. ID in CSS instead of class, when?
Only use id="name" if you want use this only **one time**
Then . in css doesn't work, use # instead
```
#named-id {
color: red;
}
```
You can overwrite previous class by using id later
HTML
```
<div class="my-class" id="my-id">
	my_text
</div>
```
CSS
```
.my-class {
	height: 400;
	# other stuff here
}

#my-id {
	height: 200;
}
```
---------------------------------------------------------------------------------------
### 11. Backgound with .webp and .gif
[>Giphy<](https://giphy.com/gifs/trippy-weird-psychedelic-3ov9k1173PdfJWRsoE)
.webp is like .gif but size of this file is much smaller
Anyway we can use both of them
Way is the same as the image in background

---------------------------------------------------------------------------------------
### 12. Text Shadow
```
.shadow {
text-shadow: 2px 2px black;
}
```
You can also put minus value to get shadow from the left of text
```
.shadow {
text-shadow: -2px -2px black;
}
```
Also it possible to make it more blurry
```
.shadow {
text-shadow: 2px 2px 10px black;
}
```
Using white color of text and white color of background doesn't mean that we will not see text
```
.shadow {
text-shadow: 0px 0px 10px black;
}
```

---------------------------------------------------------------------------------------
### 13. Color Contrast Checker
[>Userway - Color Contrast Checker<](https://userway.org/contrast/?fg=000000&bg=ffffff)
Check here if your colors collaborate well together

---------------------------------------------------------------------------------------
### 14. Multi CSS Selectors in one line
```
h1, h2, h3 {
text-shadow: 0px 0px 1px black;
}
```
---------------------------------------------------------------------------------------
### 15. Columns (not as default block html)
```
body {
display: flex;
flex-direction: column;
justify-content: center;
align-items: center;
}
```
align-items works in column (so you make place something at bottom)
justify-content works inline, in row (so you make place something on left)
if you change flex-direction into column (from default row value) these two values above work in opposite

---------------------------------------------------------------------------------------
### 16. Hover (when touched)
```
div:hover {
background: black;
}
```
```
div:hover {
background-image: url("images/example.png");
}
```

---------------------------------------------------------------------------------------
### 17. Background Gradient
```
.img {
background: linear-gradient(red, blue);
}
```
From red (top) to blue (bot)

---------------------------------------------------------------------------------------
# CSS (Summary)

### Some class stuff
```
.my-class {
	color: black; 					/\* Text color \*/
	background-color: white; 		/\* Background color \*/
	font-size: 16px; 				/\* Text size \*/
	font-family: Arial, sans-serif; /\* Font type \*/
	line-height: 1.5; 				/\* Spacing between lines of text \*/
	text-align: center; 			/\* Align text horizontally \*/
	margin: 10px; 					/\* Space outside the element \*/
	padding: 20px; 					/\* Space inside the element \*/
	border: 2px solid black; 		/\* Border properties \*/
	width: 100px; 					/\* Width of the element \*/
	height: 50px; 					/\* Height of the element \*/
	display: block; 				/\* Block-level element \*/
	position: relative; 			/\* Positioning relative to normal position \*/
}
```
### Some id stuff
```
#my-id {
	font-family: Verdana, Geneva, Tahoma, sans-serif;
	text-shadow: 0px 0px 1px black;
	background: linear-gradient(red, blue);
	display: flex;
	flex-direction: column;
	justify-content: center;
	align-items: center;
	border-bottom: 2px solid white;
	margin: 10 auto
}
```
### Not Google Font (not linked and downloaded)
```
@font-face {
src: url("../fonts/corleone/Corleone.ttf");
font-family: Corleone;
}
```