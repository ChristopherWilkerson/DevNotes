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
