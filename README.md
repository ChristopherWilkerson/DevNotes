# DevNotes
Learning Notes
## June 6th, 2024
CSS notes

first line in css.style sheet if want to reset default css style sheets
* {
  margin: 0;
  padding: 0;


Can use Inline styling and using <style> in <head> to format 
Link the CSS style sheet to the HTML by using <link> in the <head>  <link href="./style.css" rel='stylesheet'/>
* selector selects all elements in the html code (e.g. change font styles)
Select by class, use . beforehand (e.g. .brand)
Can select and modify multiple classes by id'ing them as class='blank blank2' which creates the option to stylize .blank and .blank2 simultaneously.
class= can be used for multiple values across HTML code, but id= can only be used once for one value. Use #idname to utilize in CSS.
Can target specific attribute a[href*='florence']{color: lightgreen;}
:focus, :visited, :disabled, and :active are all pseudo-classes. A pseudo-class can be attached to any selector. It is always written as a colon : followed by a name. For example p:hover
Specificity heirarchy
        ID
        Class
        Type
  Chain multiple tags together by using . in between.
  In the example above, .main-list selects the element with the.main-list class (the <ul> element). The descendant <li>‘s are selected by adding li to the selector, separated by a space. This results in .main-list li as the final selector.
  space between two types will specify. But order matters. li h4 does not equal h4 li. the former will pull all h4 from li and the latter will pull all li from h4s.
  add comma between selectors to change multiple selectors without having to repeat code.
   background gradient = background: linear-gradient(-45deg, #35577D, #141E30);
  font-weight: bold or normal
  The text-align property can be set to one of the following commonly used values:

    left — aligns text to the left side of its parent element, which in this case is the browser.
    center — centers text inside of its parent element.
    right — aligns text to the right side of its parent element.
    justify— spaces out text in order to align with the right and left side of the parent element.
  opacity- 0 to 1
  background-image
  image {
  background-image: url("https://content.codecademy.com/courses/freelance-1/unit-2/soccer.jpeg");

## June 7th, 2024

  Input img using src <img src:"link">
  list-style: square;      changings bullet point list to squares.  list-style: none; to remove bullets
  img height = height&px

  button:hover for hover button in css
  button {10px 12px;}
  .button1 {border-radius: 2px;} for rounded buttons or in %
  border: 2px solid pink; for border around button

  .button2:hover {
  box-shadow: 0 12px 16px 0 rgba(0,0,0,0.24), 0 17px 50px 0 rgba(0,0,0,0.19);
}            is shadow on hover

auto scale images 
img {
  max-width: 100%;
  height: auto;
}

dope
  width: 80%;
  background-color: white;
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);


center text on image: after creating two div, one containing the img and the text and one just containg the text
}

.image-container { 
  position: relative;
  display: inline-block;
  }

.image-container img {
  display: block;
  width: 100%;
  height: auto;
}

.image-text {
  position: absolute;
  top: 50%; 
  left: 50%; 
  transform: translate(-50%, -50%); 
  background-color: rgb(102, 151, 134); 
  color: #fff; 
  padding: 5px 10px; 
  font-size: 20px; 
  text-align: center;
}

shorthand padding - top, right, bottom, left (clockwise from top)
p.content-header {
  padding: 6px 11px 4px 9px;
}

auto margins with top and bottom at 0 and centered left-right
.pull-quote {
  width: 350px;
  margin: 0 auto;

  Unlike horizontal margins, vertical margins do not add. Instead, the larger of the two vertical margins sets the distance between adjacent elements.

  min-width and min-height (also max) to preserve text and website layout across various screen types

overflow: scroll;
or : hidden;

## June 8th, 2024

css vertical text
writing-mode: vertical-lr;

can use in conjunction with display: flex;


gap, col-gap, row-gap; px;

****** !important
html {
  scroll-behavior: smooth;


.box {
  overflow: auto;
  resize: both;           or vertical and horizontal (keep a display: flex; on for centered)


gradient text:

  background: linear-gradient ()
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  create background gradient, then mask it to text

  fit image to box

  object-fit: cover;


  fade in text:

  animation: fade 1s ease-in 1s;
  pointer-events: none;
  opacity: 0;
  }

  @keyframes fade {
  0%{
    opacity: 0;
    }
  100%{
    opacity: 1;
    }
  }

  airbnb type scroll bar

  .container {
      width: 20rem;
      height: 20rem;
      background: white;
      display: flex;
      overflow-x: scroll;
      scroll-snap-type: x mandatory;       can use proximity as well for more natural scroll 
      }

  .container div {
      min-width: 20rem;


  changing box properties to auto fit content in box 
 * {box-sizing: border-box;
      display: flex;
      justify-content: center;
      align-items: center;
      font-size: 10rem;

reset style sheets in seperate reset style css file

good practice to reset styles

also, using notes to seperate sections of code
      color: white;
      scroll-snap-align: center;


The default position of an element can be changed by setting its position property. The position property can take one of five values:

    static - the default value (it does not need to be specified)
    relative
    absolute
    fixed
    sticky
.green-box {
  background-color: green;
  position: relative;
  top: 50px;
  left: 120px;

position: fixed;   for nav bars or things you want to scroll with the user.

z-index: 10;  move the nav bar to stay in front 

display: inline-block;     Good :)

## June 9th, 2024

header

.item-1 {
position: fixed;
top: 0px;
left: 0px
border-radius: 0;
width: 100%
z-index: 1;


make sticky follow immediately
position: sticky;
top: 0px 

flex-box moves items in a container along an x or y axis. Defaults to X flex-direction: row;
but can change to Y using flex-direction: column;

also, justify-content: flex-end; shifts content to end of container.
center or space-between or space-around or space-evenly. defaults to flex-start;

use align-items: in conjunction to move items in container along other axis simultaneously. 
flex-start, flex-end, center, baseline

use flex-grow on any specific item or class to grow it flex-grow: 1;

align-self in specific class to override rest of flex-box behavior.

flex-wrap: wrap;
will allow items to use more of the container than the default 1 line.

this unlocks the align-content: property which allows us to align all the items in the container.
flex-end, flex-start, center

can then use sepearte "gap" property set at ems of px


image drop shadow

filter: drop-shadow (px px px color);



nav links

<nav></nav>
<ul></ul>
<li></li>
<a href="">

where <li><a href=""></a></li>

.navbar li{
position: fixed;
display: inline-block
width: 100%;
top: 0;
padding: 10 10;
}

remove hyperlink text decoration:

.navbar a {
text-decoration: none;


using avatar image for links and stuff

background-image: url("");
background-size: cover;
height: 50px;

## June 11th, 2024

CSS

can use named-colors, hex codes, or rgb codes, but choose one and keep it consistent throughout the css file.
weight: 50px;
border-radius: 50%;
display: inline-block;
vertical-align: middle;

use <span> when don't want the full formatting of <div>


hsl = hue-saturation-lightness

      (0-360, %, %)

hsla =hsl + alpha
      (0-360, %, %, decimal 0-1)

can also use

rgba = (0-255, 0-255, 0-255, decimal 0-1)

A little unconventional, but still worth mentioning is how hex colors can also have an alpha value. By adding a two-digit hexadecimal value to the end of the six-digit representation (#52BC8280), or a one-digit hexadecimal value to the end of the three-digit representation (#F003), you can change the opacity of a hexadecimal color. Hex opacity ranges from 00 (transparent) to FF (opaque).

Multi-Word Values

When specifying a typeface with multiple words, like Times New Roman, it is recommended to use quotation marks (' ') to group the words together, like so:

h1 {
  font-family: 'Times New Roman';
}

** Web safe fonts are good fallback fonts that can be used if your preferred font is not available.

h1 {
  font-family: Caslon, Georgia, 'Times New Roman';
}

In the example above, Georgia and Times New Roman are fallback fonts to Caslon. When you specify a group of fonts, you have what is known as a font stack. A font stack usually contains a list of similar-looking fonts. Here, the browser will first try to use the Caslon font. If that’s not available, it will try to use a similar font, Georgia. And if Georgia is not available, it will try to use Times New Roman.

Text can also be styled to appear in either all uppercase or lowercase with the text-transform property.

h1 {
  text-transform: uppercase;
}

Letter Spacing

The letter-spacing property is used to set the horizontal spacing between the individual characters in an element. It’s not common to set the spacing between letters, but it can sometimes help the readability of certain fonts or styles. The letter-spacing property takes length values in units, such as 2px or 0.5em.

p {
  letter-spacing: 2px;
}


Word Spacing

You can set the space between words with the word-spacing property. It’s also not common to increase the spacing between words, but it may help enhance the readability of bolded or enlarged text. The word-spacing property also takes length values in units, such as 3px or 0.2em.

h1 {
  word-spacing: 0.3em;
}


We can use the line-height property to set how tall we want each line containing our text to be. Line height values can be a unitless number, such as 1.2, or a length value, such as 12px, 5% or 2em.

p {
  line-height: 1.4;
}



The text-align property, which you may already be familiar with from the CSS Visual Rules lesson, aligns text to its parent element.

h1 {
  text-align: right;
}

In the example above, the <h1> element is aligned to the right side, instead of the default left.


Fonts can also be added using a @font-face ruleset in your CSS stylesheet instead of using a <link> element in your HTML document. As mentioned earlier, fonts can be downloaded just like any other file on the web. They come in a few different file formats, such as:

    OTF (OpenType Font)
    TTF (TrueType Font)
    WOFF (Web Open Font Format)
    WOFF2 (Web Open Font Format 2)

The different formats are a progression of standards for how fonts will work with different browsers, with WOFF2 being the most progressive. It’s a good idea to include TTF, WOFF, and WOFF2 formats with your @font-face rule to ensure compatibility on all browsers.

## June 12th, 2024

More CSS

add an underline

text-decoration: underline;


Most browsers will display the text of a title attribute as a tooltip, meaning when a user hovers their cursor over an element, the text will appear in a small box near the cursor.

To add tooltips to a clickable element like a link, add it as the title attribute.

<p>
  <a href="https://www.codecademy.com" title="Codecademy is an online learning platform">Codecademy</a> is the best place to learn to code!
</p>

Mouse over the word “Codecademy” below to see this behavior in action!

for hand mouse icon
cursor: pointer;

Links have four main states: normal (not clicked), hover, active (clicked), and visited. These four states have associated CSS pseudo-classes: :link, :hover, :active, and :visited.

The proper order of these rules is:

    :link
    :visited
    :hover
    :active

For example, to implement a bare minimum 3-D button design, the following CSS ruleset could be used:

button {
  padding: 5px;
  border: 1px solid black;
  border-radius: 5px;
  text-decoration: none;
  box-shadow: 0px 5px;
}

button:hover {
  cursor: pointer;
}

button:active {
  margin-top: 5px;
  color: black;
  box-shadow: 0px 0px;
}

A button element can then be created with the following HTML:

<button>Click me</button>


simple breadcrumb website trail

.breadcrumb > li {
  display: inline;
}

.breadcrumb li+li::before {
	padding: 10px;
  content: ">";

}

.breadcrumb a {
  text-decoration: none;
  color: lavender;
  background-color: grey;
  font-size: .5rem;

}

.breadcrumb a:hover {
  color: orange;
  background-color: black;

}


proper anchor tag in list example

<body>
    <div class="jumbotron">
      <ul class ="breadcrumb">
        <li><a href="#">Asia</a></li>
        <li><a href="#">Singapore</a></li>
        <li><a href="#">Tourism</a></li>
        <li><a href="#">Hotels</a></li>
        </ul>


more breadcrumb styles

.breadcrumb li a::before, .breadcrumb li a::after {
  content: "";
  position: absolute;
  border-color: darkcyan;
  border-style: solid;
  border-width: 15px 5px;

  By setting a portion of the border to transparent, it creates the “tail” of the arrow:

.breadcrumb li a::before {
  left: -10px;
  border-left-color: transparent;
}


arrow  breadcrumb :)

.breadcrumb {
  text-align: left;
}
.breadcrumb li {
  float: left;
}

.breadcrumb a {
  color: #fff;
  background: darkcyan;
  text-decoration: none;
  position: relative;
  height: 30px;
  line-height: 30px;
  text-align: center;
  margin-right: 15px;
  padding: 0 5px;
}

.breadcrumb a::before,
.breadcrumb a::after {
  content: "";
  position: absolute;
  border-color: darkcyan;
  border-style: solid;
  border-width: 15px 5px;
}

.breadcrumb a::before {
  left: -10px;
  border-left-color: transparent;
}

.breadcrumb a::after {
  left: 100%;
  border-color: transparent;
  border-left-color: darkcyan;
}

.breadcrumb a:hover {
  background-color: rgb(181, 88, 48);
}

.breadcrumb a:hover::before {
  border-color: rgb(181, 88, 48);
  border-left-color: transparent;
}

.breadcrumb a:hover::after {
  border-left-color: rgb(181, 88, 48);
}

specific syntax when adding breadcrumb > in between classes located in another class. li.class+li.class::before

.breadcrumb li.location+li.location::before {
  content: ">";



wireframes = blueprints for websites or apps
	focus on usablity and function rather than aesthetics.


 html sections
  <header>
  <nav>
  <main>
  <body>
  <section>
  <footer>

## June 13th, 2024

*** Responsive grids for maximizing content across various platforms and screen sizes

desktop (12-16)
tablet (5-8)
mobile (3-4)


**container divs
<div class="container">

To designate an element as a flex container, set the element’s display property to flex or inline-flex. Once an item is a flex container, there are several properties we can use to specify how its children behave. In this lesson we will cover these properties:

    justify-content
    align-items
    flex-grow
    flex-shrink
    flex-basis
    flex
    flex-wrap
    align-content
    flex-direction
    flex-flow

Below are five commonly used values for the align-items property:

    flex-start — all elements will be positioned at the top of the parent container.
    flex-end — all elements will be positioned at the bottom of the parent container.
    center — the center of all elements will be positioned halfway between the top and bottom of the parent container.
    baseline — the bottom of the content of all items will be aligned with each other.
    stretch — if possible, the items will stretch from top to bottom of the container (this is the default value; elements with a specified height will not stretch; elements with a minimum height or no height specified will stretch).

.container {
  display: flex;
}

.side {
  width: 100px;
  flex-grow: 1;
}

.center {
  width: 100px;
  flex-grow: 2;
}

In the example above, the .container div has a display value of flex, so its three child divs will be positioned next to each other. If there is additional space in the .container div (in this case, if it is wider than 300 pixels), the flex items will grow to fill it. The .center div will stretch twice as much as the .side divs. For example, if there were 60 additional pixels of space, the center div would absorb 30 pixels and the side divs would absorb 15 pixels each.

If a max-width is set for an element, it will not grow larger than that even if there is more space for it to absorb.

All of the previous properties we have learned are declared on flex containers, or the parent elements. This property — flex-grow — is the first we have learned that is declared on flex items.
Instructions

    Checkpoint 1 Passed

    1.

    Assign .top.side and .top.center a flex-grow value of 1. Stretch and shrink the browser.

Checkpoint 2 Passed

2.

Assign .middle.center the flex-grow value of 1. Stretch and shrink the browser again.
Checkpoint 3 Enabled

3.

Assign .bottom.side a flex-grow value of 1 and .bottom.center a flex-grow value of 2. Shrink and stretch the browser again. Compare the differences in behavior of all three sections.




flex basis to lock in size of flex item before shrink or grow


flex-grow (number)
flex-shrink (number)
flex-basis (px or rem size)

flex defines all three properties easily

flex: 1 3 100px; 
     grow shrink basis;



Sometimes, we don’t want our content to shrink to fit its container. Instead, we might want flex items to move to the next line when necessary. This can be declared with the flex-wrap property. The flex-wrap property can accept three values:

    wrap — child elements of a flex container that don’t fit into a row will move down to the next line
    wrap-reverse — the same functionality as wrap, but the order of rows within a flex container is reversed (for example, in a 2-row flexbox, the first row from a wrap container will become the second in wrap-reverse and the second row from the wrap container will become the first in wrap-reverse)
    nowrap — prevents items from wrapping; this is the default value and is only necessary to override a wrap value set by a different CSS rule.

<div class='container'>
  <div class='item'>
    <h1>We're going to wrap!</h1>
  </div>
  <div class='item'>
    <h1>We're going to wrap!</h1>
  </div>
  <div class='item'>
    <h1>We're going to wrap!</h1>
  </div>
</div>

.container {
  display: inline-flex;
  flex-wrap: wrap;
  width: 250px;
}

.item {
  width: 100px;
  height: 100px;
}

In the example above, three flex items are contained by a parent flex container. The flex container is only 250 pixels wide so the three 100 pixel wide flex items cannot fit inline. The flex-wrap: wrap; setting causes the third, overflowing item to appear on a new line, below the other two items.

Note: The flex-wrap property is declared on flex containers.


align-items: aligning content for single row of flex box.

align-content: aligning content for multiple rows (ie after a flex wrap

Below are some of the more commonly used align-content values:

    flex-start — all rows of elements will be positioned at the top of the parent container with no extra space between.
    flex-end — all rows of elements will be positioned at the bottom of the parent container with no extra space between.
    center — all rows of elements will be positioned at the center of the parent element with no extra space between.
    space-between — all rows of elements will be spaced evenly from the top to the bottom of the container with no space above the first or below the last.
    space-around — all rows of elements will be spaced evenly from the top to the bottom of the container with the same amount of space at the top and bottom and between each element.
    stretch — if a minimum height or no height is specified, the rows of elements will stretch to fill the parent container from top to bottom (default value).


Note: The align-content property is declared on flex containers.

The main axis is used to position flex items with the following properties:

    justify-content
    flex-wrap
    flex-grow
    flex-shrink

The cross axis is used to position flex items with the following properties:

    align-items
    align-content

flex-direction to change axis

The flex-direction property can accept four values:

    row — elements will be positioned from left to right across the parent element starting from the top left corner (default).
    row-reverse — elements will be positioned from right to left across the parent element starting from the top right corner.
    column — elements will be positioned from top to bottom of the parent element starting from the top left corner.
    column-reverse — elements will be positioned from the bottom to the top of the parent element starting from the bottom left corner.


Like the shorthand flex property, the shorthand flex-flow property is used to declare both the flex-wrap and flex-direction properties in one line.

.container {
  display: flex;
  flex-wrap: wrap;
  flex-direction: column;
}

In the example above, we take two lines to accomplish what can be done with one.

.container {
  display: flex;
  flex-flow: column wrap;
}

## June 14th, 2024

Flex-box overlay using tranform: translate;
or postiion: relative; and moving top or left or bottom or right. 


## June 15th, 2024

#### Grids

To turn an HTML element into a grid container, you must set the element’s display property to one of two values:

    grid — for a block-level grid.
    inline-grid — for an inline grid.


We can define the columns of our grid by using the CSS property grid-template-columns. Below is an example of this property in action:

.grid {
  display: grid;
  width: 500px;
  grid-template-columns: 100px 200px;
}

We’ve learned how to define the number of columns in our grid explicitly. To specify the number and size of the rows, we are going to use the property grid-template-rows.

This property is almost identical to grid-template-columns. Take a look at the code below to see both properties in action.

.grid {
  display: grid;
  width: 1000px;
  height: 500px;
  grid-template-columns: 100px 200px;
  grid-template-rows: 10% 20% 600px;
}

This grid has two columns and three rows. 


The shorthand property, grid-template, can replace the previous two CSS properties. Both grid-template-rows and grid-template-columns are nowhere to be found in the following code!

.grid {
  display: grid;
  width: 1000px;
  height: 500px;
  grid-template: 200px 300px / 20% 10% 70%;
}

When using grid-template, the values before the slash will determine the size of each row. The values after the slash determine the size of each column. In this example, we’ve made two rows and three columns of varying sizes.


By using the fr unit, we can define the size of columns and rows as a fraction of the grid’s length and width. This unit was specifically created for use in CSS Grid. Using fr makes it easier to prevent grid items from overflowing the boundaries of the grid. Consider the code below:

.grid {
  display: grid;
  width: 1000px;
  height: 400px;
  grid-template: 2fr 1fr 1fr / 1fr 3fr 1fr;
}

In this example, the grid will have three rows and three columns. The rows are splitting up the available 400 pixels of height into four parts. The first row gets two of those parts, the second row gets one, and the third row gets one. Therefore the first row is 200 pixels tall, and the second and third rows are 100 pixels tall. 


The repeat function will duplicate the specifications for rows or columns a given number of times. In the example above, using the repeat function will make the grid have three columns that are each 100 pixels wide. It is the same as writing:

grid-template-columns: 100px 100px 100px;

Repeat is particularly useful with fr. For example, repeat(5, 1fr) would split your table into five equal rows or columns.

Finally, the second parameter of repeat() can have multiple values.

grid-template-columns: repeat(2, 20px 50px)

This code will create four columns where the first and third columns will be 20 pixels wide and the second and fourth will be 50 pixels wide.

In all of our grids so far, there hasn’t been any space between the items in our grid. The CSS properties row-gap and column-gap will put blank space between every row and column in the grid.

.grid {
  display: grid;
  width: 320px;
  grid-template-columns: repeat(3, 1fr);
  column-gap: 10px;
}

Using the CSS properties grid-row-start and grid-row-end, we can make single grid items take up multiple rows. Remember, we are no longer applying CSS to the outer grid container; we’re adding CSS to the elements sitting inside the grid!


We can use the property grid-row as shorthand for grid-row-start and grid-row-end. The following two code blocks will produce the same output:

.item {
  grid-row-start: 4;
  grid-row-end: 6;
}

.item {
  grid-row: 4 / 6;
}


When using these properties, we can use the keyword span to start or end a column or row, relative to its other end. Look at how span is used in the code below:

.item {
  grid-column: 4 / span 2;
}

This is telling the item element to begin in column four and take up two columns of space. So item would occupy columns four and five. It produces the same result as the following code blocks:

.item {
  grid-column: 4 / 6;
}

.item {
  grid-column-start: 4;
  grid-column-end: span 2;
}

.item {
  grid-column-start: span 2;
  grid-column-end: 6;
}

span is a useful keyword, because it avoids off-by-one errors (miscalculating the ending grid line) you might make when determining the ending grid line of an element. If you know where you want your grid item to start and how long it should be, use span!

We’ve already been able to use grid-row and grid-column as shorthand for properties like grid-row-start and grid-row-end. We can refactor even more using the property grid-area. This property will set the starting and ending positions for both the rows and columns of an item.

.item {
  grid-area: 2 / 3 / 4 / span 5;
}

grid-area takes four values separated by slashes. The order is important! This is how grid-area will interpret those values.

    grid-row-start
    grid-column-start
    grid-row-end
    grid-column-end

In the previous lesson, you learned all the foundational properties necessary to create a two-dimensional grid-based layout for your web pages! In this lesson, you’ll learn the following additional properties that you can use to harness the power of CSS Grid Layout:

    grid-template-areas
    justify-items
    justify-content
    justify-self
    align-items
    align-content
    align-self
    grid-auto-rows
    grid-auto-columns
    grid-auto-flow

You will also learn about the explicit and implicit grids and grid axes.


***Grid Template Areas
16 min

The grid-template-areas property allows you to name sections of your web page to use as values in the grid-row-start, grid-row-end, grid-column-start,grid-column-end, and grid-area properties. This property is declared on grid containers.

<div class="container">
  <header>Welcome!</header>
  <nav>Links!</nav>
  <section class="info">Info!</section>
  <section class="services">Services!</section>
  <footer>Contact us!</footer>
</div>

.container {
  display: grid;
  max-width: 900px;
  position: relative;
  margin: auto;
  grid-template-areas: "header header"
                       "nav nav" 
                       "info services"
                       "footer footer";
  grid-template-rows: 300px 120px 800px 120px;
  grid-template-columns: 1fr 3fr; 
}

header {
  grid-area: header;
} 

nav {
  grid-area: nav;
} 

.info {
  grid-area: info;
} 

.services {
  grid-area: services;
}

footer {
  grid-area: footer;
} 

You may want to expand this section of the website to view the code above more clearly.

    In the example above, the HTML creates a web page with five distinct parts.
    In the .container ruleset, the grid-template-areas declaration creates a 2-column, 4-row layout.
    The grid-template-rows declaration specifies the height of each of the four rows from top to bottom: 300 pixels, 120 pixels, 800 pixels, and 120 pixels.
    The grid-template-columns declaration uses the fr value to cause the left column to use one fourth of the available space on the page and the right column to use three-fourths of the available space on the page.
    In each ruleset below .container, we use the grid-area property to tell that section to cover the portion of the page specified. The header element spans the first row and both columns. The nav element spans the second row and both columns. The element with class .info spans the third row and left column. The element with class .services spans the third row and right column. The footer element spans the bottom row and both columns. 

We have referred to “two-dimensional grid-based layout” several times throughout this course.

There are two axes in a grid layout — the column (or block) axis and the row (or inline) axis.

The column axis stretches from top to bottom across the web page.

The row axis stretches from left to right across the web page.

In the following four exercises, we will learn and use properties that rely on an understanding of grid axes.

justify-items is a property that positions grid items along the inline, or row, axis. This means that it positions items from left to right across the web page. This property is declared on grid containers.

justify-items accepts these values:

    start — aligns grid items to the left side of the grid area
    end — aligns grid items to the right side of the grid area
    center — aligns grid items to the center of the grid area
    stretch — stretches all items to fill the grid area

We can use justify-content to position the entire grid along the row axis. This property is declared on grid containers.

It accepts these values:

    start — aligns the grid to the left side of the grid container
    end — aligns the grid to the right side of the grid container
    center — centers the grid horizontally in the grid container
    stretch — stretches the grid items to increase the size of the grid to expand horizontally across the container
    space-around — includes an equal amount of space on each side of a grid element, resulting in double the amount of space between elements as there is before the first and after the last element
    space-between — includes an equal amount of space between grid items and no space at either end
    space-evenly — places an even amount of space between grid items and at either end


align-items is a property that positions grid items along the block, or column axis. This means that it positions items from top to bottom. This property is declared on grid containers.

align-items accepts these values:

    start — aligns grid items to the top side of the grid area
    end — aligns grid items to the bottom side of the grid area
    center — aligns grid items to the center of the grid area
    stretch — stretches all items to fill the grid area

In the previous exercise, we positioned grid items within their rows. align-content positions the rows along the column axis, or from top to bottom, and is declared on grid containers.

It accepts these positional values:

    start — aligns the grid to the top of the grid container
    end — aligns the grid to the bottom of the grid container
    center — centers the grid vertically in the grid container
    stretch — stretches the grid items to increase the size of the grid to expand vertically across the container
    space-around — includes an equal amount of space on each side of a grid element, resulting in double the amount of space between elements as there is before the first and after the last element
    space-between — includes an equal amount of space between grid items and no space at either end
    space-evenly — places an even amount of space between grid items and at either end


The justify-items and align-items properties specify how all grid items contained within a single container will position themselves along the row and column axes, respectively.

justify-self specifies how an individual element should position itself with respect to the row axis. This property will override justify-items for any item on which it is declared.

align-self specifies how an individual element should position itself with respect to the column axis. This property will override align-items for any item on which it is declared.

These properties are declared on grid items. They both accept these four properties: 

    start — positions grid items on the left side/top of the grid area
    end — positions grid items on the right side/bottom of the grid area
    center — positions grid items on the center of the grid area
    stretch — positions grid items to fill the grid area (default)



Grid Auto Rows and Grid Auto Columns
5 min

CSS Grid provides two properties to specify the size of grid tracks added implicitly: grid-auto-rows and grid-auto-columns. These properties are declared on grid containers.

grid-auto-rows specifies the height of implicitly added grid rows. grid-auto-columns specifies the width of implicitly added grid columns.

grid-auto-rows and grid-auto-columns accept the same values as their explicit counterparts, grid-template-rows and grid-template-columns:

    pixels (px)
    percentages (%)
    fractions (fr)
    the repeat() function


In addition to setting the dimensions of implicitly-added rows and columns, we can specify the order in which they are rendered.

grid-auto-flow specifies whether new elements should be added to rows or columns, and is declared on grid containers.

grid-auto-flow accepts these values:

    row — specifies the new elements should fill rows from left to right and create new rows when there are too many elements (default)
    column — specifies the new elements should fill columns from top to bottom and create new columns when there are too many elements
    dense — this keyword invokes an algorithm that attempts to fill holes earlier in the grid layout if smaller elements are added

You can pair row or column with dense, like this: grid-auto-flow: row dense;.









