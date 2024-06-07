# DevNotes
Learning Notes
## June 6th, 2024
CSS notes
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
  
