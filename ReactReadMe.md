## July 13, 2024 ## 

React notes:

classes = className


Destructuring with JavaScript

Learn a new syntax for handling objects and arrays in JavaScript.
What is Destructuring?

Destructuring, or destructuring assignment, is a JavaScript feature that makes it easier to extract data from arrays and objects, introduced in the ES6 version of JavaScript.

At this point, we assume you already know how to extract data from arrays and objects. That means that you don’t NEED destructuring: destructuring is a form of syntactic sugar, which means that it is an easier way to write certain expressions, usually by being shorter and clearer than other forms. Even if you don’t use it yourself, you’ll probably see it in someone else’s code, so it’s valuable to understand.
Destructuring Arrays

Data structures like arrays and objects can be very useful for storing large amounts of data. The process of converting individual elements of an array into individual variables can be tedious:

let cars = ['ferrari', 'tesla', 'cadillac'];

If we wanted to access these cars individually and assign them to variables we could do this:

let cars = ['ferrari', 'tesla', 'cadillac'];
let car1 = cars[0];
let car2 = cars[1];
let car3 = cars[2];
console.log(car1, car2, car3); // Prints: ferrari tesla cadillac

We can use destructuring to shorten our code and make it more concise:

let cars = ['ferrari', 'tesla', 'cadillac'];
let [car1, car2, car3] = cars;
console.log(car1, car2, car3); // Prints: ferrari tesla cadillac

In the code above, we created three variables (car1, car2, car3) that correspond to the three elements in the cars array. Each variable name in the new array will be assigned the value of the corresponding element. As you can see, we are able to achieve what we did previously with three lines of code, in one! Imagine how many lines of code we would save working with an array with 10 elements! 


Destructuring Objects

We can also use destructuring assignment with objects. Let’s look at a basic use case in which we capture an object’s properties with new variables:

let destinations = { x: 'LA', y: 'NYC', z: 'MIA' };
let x = destinations.x;
let y = destinations.y;
let z = destinations.z;
console.log(x, y, z); // Prints LA NYC MIA

With the simplified destructuring syntax, we access the values by matching the variable names to the property names.

let destinations = { x: 'LA', y: 'NYC', z: 'MIA' };
let { x, y, z } = destinations;
console.log(x, y, z); // Prints LA NYC MIA

Using destructuring syntax, we’re able to create new variables directly from an object’s properties. In this case, we took the values of destination.x, destination.y, and destination.z and stored them in new variables x, y, z, respectively.


Destructuring Function Parameters

Function arguments are another place where destructuring is useful. Instead of accepting a complete object as an argument, a function can use destructuring to capture specific properties as named parameters.

let truck = {
  model: '1977 Mustang convertible',
  maker: 'Ford',
  city: 'Detroit',
  year: '1977',
  convertible: true
};

const printCarInfo = ({model, maker, city}) => {
  console.log(`The ${model}, or ${maker}, is in the city ${city}.`);
};

printCarInfo(truck);
// Prints: The 1977 Mustang convertible, or Ford, is in the city Detroit.

The printCarInfo function uses object destructuring to create three parameter variables: model, maker, and city. When the function is invoked with the truck object, these parameters are assigned the corresponding values from that object.

Note that we don’t have to use every property from the truck object: we only create parameter variables for the values that we need.


What is JSX?
1 min

JSX is a syntax extension for JavaScript. It was written to be used with React. JSX code looks a lot like HTML.

What does “syntax extension” mean?

In this case, it means that JSX is not valid JavaScript. Web browsers can’t read it!

If a JavaScript file contains JSX code, then that file will have to be compiled. This means that before the file reaches a web browser, a JSX compiler will translate any JSX into regular JavaScript.

Codecademy’s servers already have a JSX compiler installed, so you don’t have to worry about that for now. Eventually we’ll walk through how to set up a JSX compiler on your personal computer.



Intro to JSX
Attributes In JSX
5 min

JSX elements can have attributes, just like how HTML elements can.

A JSX attribute is written using HTML-like syntax: a name, followed by an equals sign, followed by a value. The value should be wrapped in quotes, like this:

my-attribute-name="my-attribute-value"

Here are some JSX elements with attributes:

<a href='http://www.example.com'>Welcome to the Web</a>;

const title = <h1 id='title'>Introduction to React.js: Part I</h1>; 

A single JSX element can have many attributes, just like in HTML:

const panda = <img src='images/panda.jpg' alt='panda' width='500px' height='500px'>;


Intro to JSX
Nested JSX
5 min

You can nest JSX elements inside of other JSX elements, just like in HTML.

Here’s an example of a JSX <h1> element, nested inside of a JSX <a> element:

<a href="https://www.example.com"><h1>Click me!</h1></a>

To make this more readable, you can use HTML-style line breaks and indentation:

<a href="https://www.example.com">
  <h1>
    Click me!
  </h1>
</a>

If a JSX expression takes up more than one line, then you must wrap the multi-line JSX expression in parentheses. This looks strange at first, but you get used to it:

(
  <a href="https://www.example.com">
    <h1>
      Click me!
    </h1>
  </a>
)

Nested JSX expressions can be saved as variables, passed to functions, etc., just like non-nested JSX expressions can! Here’s an example of a nested JSX expression being saved as a variable:

 const theExample = (
   <a href="https://www.example.com">
     <h1>
       Click me!
     </h1>
   </a>
 );


Intro to JSX
JSX Outer Elements
3 min

There’s a rule that we haven’t mentioned: a JSX expression must have exactly one outermost element.

In other words, this code will work:

const paragraphs = (
  <div id="i-am-the-outermost-element">
    <p>I am a paragraph.</p>
    <p>I, too, am a paragraph.</p>
  </div>
);

But this code will not work:

const paragraphs = (
  <p>I am a paragraph.</p> 
  <p>I, too, am a paragraph.</p>
);

The first opening tag and the final closing tag of a JSX expression must belong to the same JSX element!

It’s easy to forget about this rule and end up with errors that are tough to diagnose.

If you notice that a JSX expression has multiple outer elements, the solution is usually simple: wrap the JSX expression in a <div> element.


## July 16th, 2024 ##


Advanced JSX
Self-Closing Tags
2 min

Another common JSX error involves self-closing tags.

What’s a self-closing tag?

Most HTML elements use two tags: an opening tag (<div>), and a closing tag (</div>). However, some HTML elements such as <img> and <input> use only one tag. The tag that belongs to a single-tag element isn’t an opening tag or a closing tag; it’s a self-closing tag.

When you write a self-closing tag in HTML, it is optional to include a forward slash immediately before the final angle bracket:

// Fine in HTML with a slash:
<br />

// Also fine, without the slash:
<br>

But, in JSX, you have to include the slash. If you write a self-closing tag in JSX and forget the slash, you will raise an error:

// Fine in JSX:
<br />

// NOT FINE AT ALL in JSX:
<br>


Curly Braces in JSX
1 min

The code in the last exercise didn’t behave as one might expect. Instead of adding 2 and 3, it printed out “2 + 3” as a string of text. Why?

This happened because 2 + 3 is located in between <h1> and </h1> tags.

Any code in between the tags of a JSX element will be read as JSX, not as regular JavaScript! JSX doesn’t add numbers—it reads them as text, just like HTML.

You need a way to write code that says, “Even though I am located in between JSX tags, treat me like ordinary JavaScript and not like JSX.”

You can do this by wrapping your code in curly braces.




