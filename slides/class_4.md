This page intentionally left blank. ⬇️, ➡️, or spacebar 🛰 to start slidedeck.
---
class: center, middle

# Welcome to Class 4!

---

# Agenda

- Questions from last week?
- News of the Week
- Readings
- Introducing CSS
- Break!
- Introduction of Website Assignment
- In-class HTML and CSS project


---
## Questions?

---

## News of the Week

Drop a link on the etherpad:
<https://etherpad.wikimedia.org/p/prattsi654fa22-4>

---
# Readings
- [What is code?](http://www.bloomberg.com/graphics/2015-paul-ford-what-is-code/)
- Everything else

<!-- ---
# BREAK

.center[![](img/compacdisc.gif)]
 -->
---
# Cascading
# Style
# Sheets

.center[![](img/waterfall.gif)]

---
# Cascading

- (of water) pour downward rapidly and in large quantities.
- fall or hang in copious or luxuriant quantities.
- arrange (a number of devices or objects) in a series or sequence.


- Moment of zen: [Roadtrip Sunset](https://codepen.io/a-trost/details/pXzbbq)

.right[![](img/waterfall4.gif)]

---
# HTML is for structure, CSS is for design

One example: same content, any number of CSS style sheets:
- [CSS Zen Garden](http://www.csszengarden.com/)


---
# How to put CSS on the page

Something like this goes between your HTML `<head>` tags:

# `<link rel="stylesheet" href="style.css">`

--

(<small> there's also the `<style></style>` element, which you can use nested within the `<head></head>` element, but much better to use the above method which is called referencing an external stylesheet </small>)

---
# Applying CSS

- HTML elements
- HTML elements with a specific *class* attribute
- HTML elements with a specific *ID* attribute


---
# Basic syntax (connecting to 'hooks' in the HTML)

```html
<h1>First header</h1>
<h1 class="blue-class-header">Second header</h1>
<h1 id="specific-id-header">Third header</h1>
```
---
# Basic syntax (connecting to 'hooks' in the HTML)

```html
<h1>First header</h1> <!-- Using basic element -->
<h1 class="blue-class-header">Second header</h1> <!-- Using class property -->
<h1 id="specific-id-header">Third header</h1> <!-- Using id property -->
```

---
# Basic syntax (in CSS)

```css
/* Using an element name as a selector */

h1 {
	color: red;
}

/* Using a class name as a selector */

.blue-class-header {
	color: CornflowerBlue;
}

/* Using an ID name as a selector */

#specific-id-header {
	color: Violet;
}
```
---
# Basic syntax (Now connected to the CSS property declarations)

```html
<h1>First header</h1> <!-- Using basic element -->
<h1 class="blue-class-header">Second header</h1> <!-- Using class property -->
<h1 id="specific-id-header">Third header</h1> <!-- Using id property -->
```

--

<h1 style="color:Red;">First header</h1>
<h1 style="color:CornflowerBlue;">Second header</h1>
<h1 style="color:Violet;">Third header</h1>

---
# Basic syntax

```css
h1 {
	color: red;
}
```

- `h1` is the *selector*
- `{` and `}` hold the rules (called *declarations*)
- `color` is the property
- `red` is the value
- the semi-colon ends the declaration, and a new one can begin



---
# Multiple declarations

```css
h1 {
	color: red;
	background-color: yellow;
	border:  2px solid;
	text-align: center;
}
```
--

<h1 style="	color: red;background-color: yellow;border:  2px solid;text-align: center;">Example header</h1>


---
# Multiple selectors

```css
h1, h2 {
	color: red;
}
```

---
# Competing declarations

```css
h1 {
	color: red;
	color: pink;
}

h1 {
	color: blue;
}
```

--

## What color will this make the headers?

--
<h1 style="color: blue;">First header</h1>
<p>Text example here</p>

<h1 style="color: blue;">Second heder</h1>

---

# Another example

```css
.pull-quote-div {
	color:  HotPink;
	background-color: LightGray;
	padding: 5% 10% 5% 10%; /* order for padding and margin is top, right, bottom, left */
	float:  right;
	font-size: 150%;
}
```
--
## unstyled & unconnected

<div>
<div>Some text to show you a div floating right</div>
   <p> These are the voyages of the Starship Enterprise. Its continuing mission, to explore strange new worlds, to seek out new life and new civilizations, to boldly go where no one has gone before. We need to neutralize the homing signal. <!-- here's an example link to a totally external website on another server; how would you link to a different page within this same project? Hint: here's an article that explains the difference between "relative" and "absolute" URLs: https://www.turnwall.com/articles/all-about-relative-absolute-links/ -->  <a href="http://sils.pratt.edu">Link to Pratt SILS Page.</a> Each unit has total environmental control, gravity, temperature, atmosphere, light, in a protective field. Sensors show energy readings in your area. We had a forced chamber explosion in the resonator coil. Field strength has increased by 3,000 percent.</p></div> 


---
# Another example

```css
.pull-quote-div {
	color:  HotPink;
	background-color: LightGray;
	padding: 5% 10% 5% 10%; /* order for padding and margin is top, right, bottom, left */
	float:  right;
	font-size: 150%; 
}
```

## Styled
<div>
<div style="	color:  HotPink;background-color: LightGray; padding: 5% 10% 5% 10%; float:  right; font-size: 130%;">Some text to show you a div floating right</div>
   <p> These are the voyages of the Starship Enterprise. Its continuing mission, to explore strange new worlds, to seek out new life and new civilizations, to boldly go where no one has gone before. We need to neutralize the homing signal. <!-- here's an example link to a totally external website on another server; how would you link to a different page within this same project? Hint: here's an article that explains the difference between "relative" and "absolute" URLs: https://www.turnwall.com/articles/all-about-relative-absolute-links/ -->  <a href="http://sils.pratt.edu">Link to Pratt SILS Page.</a> Each unit has total environmental control, gravity, temperature, atmosphere, light, in a protective field. Sensors show energy readings in your area. We had a forced chamber explosion in the resonator coil. Field strength has increased by 3,000 percent.</p></div> 



---
# Comments in CSS

```css
/* this is a comment */
```

---
# Changing text

- `font-family` (serif, san serif, or names of fonts)
- `font-size` (make big or small -- see a few slides from now)
- `font-weight` (boldness or lack of)
- `font-style` (italic or lack of)
- `text-transform` (uppercase, lowercase, capitalize)

---
# Sizing things

There are a lot of options:

- pixels (`width: 700px`)
- percentage (`width: 80%`) [Note: will be x% of the size of the containing HTML element ]
- view width / view height (`width: 10vw`)

---
# Sizing text

- Em values (`4.2em`)
- pixels (`12px`)
- words (small, medium, large, xxx-large)
- points (pt), centimeters (cm), inches (in)

---
# Making space

- Everything on the web is a bunch of boxes even if it doesn't look like it
- padding (add space around element)
- border (add space around padding)
- margin (add space around border)

<div style='background-color: green;'>
<div style="padding:40px;border: 10px solid black; margin:40px; background-color: salmon;">Box example</div>

---
# Lets talk about color

- 🌈🌈🌈
- Here's a list of the 140 named colors: [htmlcolorcodes.com](https://htmlcolorcodes.com/color-names/)
- "color" means changing the attribute's foreground color (e.g. text, border)
- `background-color` will change the color of the box area

(Bonus: [A W3C CSS Working Group thread](https://github.com/w3c/csswg-drafts/issues/5284) on renaming certain colors related to historical connotatiosn)

---
# Color: lots of options

- `red`
- `rgb(255,0,0)`
- `rgb(100%,0%,0%)`
- `#ff0000`
- `#f00`
- `hsl(0,100,50)`

You can also add transparency to RGB or HSL values:
- `rgba(255,0,0,0.5)`
- `hsla(0,100,50, 0.5)`


---

# Personal Homepage project

- Assignment details [here](https://github.com/hadro/info654fa22/blob/master/assignments/personal_homepage.md)
- Questions?

---

# Use an online code editor

- [Repl.it](https://replit.com/@hadro/654-04-fall-2022#index.html) (Click "Fork" to edit, though you'll have to create an account)

This code editor gives you a code view and then a "webview" which you can refresh to see any changes you've to your code in real time.

---

# HTML

Try the following (or explore on your own):

- Within the HTML, change the title of the page to read: “My HTML and CSS Lab Assignment”
- Change the `<h3>` element on the page to be an `<h1>` element instead
- Add a `<div>` element around the “beeker.jpg” image
- Add a number of anchor tag links to your favorite sites, and make sure these links work
- Put a `<p>` text element inside of an `<aside>` html element somewhere on the page
- From there, try adding other HTML elements, and make they are nested properly and render as you expect them to

---

# CSS

Try the following (or explore on your own):

- Assign an ID to the div that contains the beeker image (in the html)
- Assign a class selector to both the second and third paragraphs of text (use the same class selector for both) (in the html)
- Make the H1 text orange (in css)
- Make the image float to the right (use the “float:” property; see general reference here: http://www.w3schools.com/cssref/) (in css)
- Give a gray background to the second and third paragraphs of text using the class selector (use either English word “grey” as a value, or choose from here: http://www.color-hex.com/) (in css)
- Add some margin and/or padding to the div and the paragraphs (in css)
- Add a sidebar div with text in it, floating left, with gray background (both html and css)

---

# Images:

- Add another image further down on the page
- Using CSS size properties on an ID attribute attached to the image, set the image to no more than 200px in height or 200px in width, whichever is the longer of the two dimensions (see dimension properties here: http://www.w3schools.com/css/css_dimension.asp)
- Using CSS ID attributes, make the images float on either side of the page to allow text to wrap around them (use the “float:” property mentioned above)


---

# More advanced next steps:

- Create a second page using the same template, and link the two pages together
	+ Hint, make a copy of the index.html page, but save with a new name
- Add a link back to the index.html page on the subsequent page you created
- Use an unordered list to create a basic navigation for your pair of pages (see here: http://www.w3schools.com/html/html_lists.asp)
- Add a properly formatted table to one of the two pages, see here: http://www.w3schools.com/html/html_tables.asp


---

# Validation!

Validate your code!

- See if you code validates according to W3C specifications: http://validator.w3.org/
- If not, use the hints there and/or in Glitch to correct any identified errors

---
class: center, middle

# Bonus Content 

---
# Getting more complex: Children selectors

```css
#red > p {
	color: red
}
```

(Every paragraph tag nested inside of an element with an ID of "red")

---
# Sibling selectors

```css
h1 ~ p {
  color: red;	
}
```

(The paragraph tags that are at the same nested level as the h1 tag, and no others)

---
# Adjacent selectors

```css
h1 + p {
  color: red;	
}
```

(The paragraph tag that comes right after the h1 tag, and no others)

---
# `!important`

```css
h1 {
	color: red !important;
}

h1 {
	color: blue;
}
```

This is not really "good practice" but it's good in an emergency


---
# Advanced investigation: Native Frameworks

- [Grid](https://css-tricks.com/snippets/css/complete-guide-grid/) - native to CSS
- [Flexbox](https://css-tricks.com/snippets/css/complete-guide-grid/) - native to CSS

---
# Advanced investigation: Library Frameworks

- [Bootstrap](https://getbootstrap.com/) - classicccccccc, very popular, used in a lot of places
- [Materialize](https://materializecss.com/) - based on Google's design language
- [Pure.css](https://purecss.io/) - basic and easy to learn
- [Tufte.css](https://edwardtufte.github.io/tufte-css/) - make your page look like Edward Tufte books 
- ... and so many more!

---
# Advanced investigation: CSS for page layouts

<iframe width="560" height="315" src="https://www.youtube.com/embed/KOvGeFUHAC0" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

- [Fast Layouts with CSS Grid](https://www.youtube.com/watch?v=KOvGeFUHAC0)

---
# Advanced investigation: Grid resources 

- [CSS Grid Garden](https://cssgridgarden.com/)
- [CSS Tricks: A complete guide to Grid](https://css-tricks.com/snippets/css/complete-guide-grid/)

---
# Advanced investigation: Flexbox resources

- [CSS Tricks: A complete guide to Flexbox](https://css-tricks.com/snippets/css/complete-guide-grid/)
- [Flexbox Defense](http://www.flexboxdefense.com/)

---
# Additional resources

- [The CSS Saga](http://www.w3.org/Style/LieBos2e/history/Overview.html)
- [Code.org: Web Development: Intro to CSS](https://www.youtube.com/watch?v=EP9QMdoXvXE) (video)
- Rachel Andrews. [The W3C at Twenty-Five](https://www.smashingmagazine.com/2019/10/happy-birthday-w3c/)
- [Old CSS, New CSS](https://eev.ee/blog/2020/02/01/old-css-new-css/)

Technical resources:
- [CSS Basics](http://www.cssbasics.com/)
- [Mozilla: Introduction to CSS](https://developer.mozilla.org/en-US/docs/Learn/CSS/Introduction_to_CSS)
- [Mozilla: CSS Selectors](https://developer.mozilla.org/en-US/docs/Learn/CSS/Introduction_to_CSS/Selectors)
- [HTML Dog: CSS Beginner Tutorial](https://www.htmldog.com/guides/css/beginner/)

Bonus:
- [How to Center in CSS](http://howtocenterincss.com/) (Because it will definitely come up!)
- Jennifer Dewalt. [180 websites in 180 days](https://jenniferdewalt.com/) ([Background talk on this project](https://www.youtube.com/watch?v=QaSbL4sRff8))
