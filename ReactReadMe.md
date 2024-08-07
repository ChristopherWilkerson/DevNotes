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



Advanced JSX
JSX Conditionals: If Statements That Don't Work
1 min

Great work! You’ve learned how to use curly braces to inject JavaScript into a JSX expression!

Here’s a rule that you need to know: you can not inject an if statement into a JSX expression.

This code will break:

(
  <h1>
    {
      if (purchase.complete) {
        'Thank you for placing an order!'
      }
    }
  </h1>
)

What if you want a JSX expression to render but only under certain circumstances? You can’t inject an if statement. What can you do?

You have lots of options. In the next few lessons, we’ll explore some simple ways to write conditionals (expressions that are only executed under certain conditions) in JSX.


Advanced JSX
JSX Conditionals: If Statements That Do Work
8 min

How can you write a conditional if you can’t inject an if statement into JSX?

One option is to write an if statement and not inject it into JSX.

Look at if.js. Follow the if statement, all the way from line 8 down to line 20.
JSX Conditionals: The Ternary Operator
6 min

There’s a more compact way to write conditionals in JSX: the ternary operator.

The ternary operator works the same way in React as it does in regular JavaScript. However, it shows up in React surprisingly often.

Recall how it works: you write x ? y : z, where x, y, and z are all JavaScript expressions. When your code is executed, x is evaluated as either “truthy” or “falsy”. If x is truthy, then the entire ternary operator returns y. If x is falsy, then the entire ternary operator returns z.

Here’s how you might use the ternary operator in a JSX expression:

const headline = (
  <h1>
    { age >= drinkingAge ? 'Buy Drink' : 'Do Teen Stuff' }
  </h1>
);

In the above example, if age is greater than or equal to drinkingAge, then headline will equal <h1>Buy Drink</h1>. Otherwise, headline will equal <h1>Do Teen Stuff</h1>.



if.js works because the words if and else are not injected in between JSX tags. The if statement is on the outside, and no JavaScript injection is necessary.

This is a common way to express conditionals in JSX.



Advanced JSX
JSX Conditionals: &&
6 min

We’re going to cover one final way of writing conditionals in React: the && operator.

Like the ternary operator, && is not React-specific, but it shows up in React very often.

In the last two exercises, you wrote statements that would sometimes render a kitty and other times render a doggy. && would not have been the best choice for that code.

&& works best for conditionals that will sometimes do an action but other times do nothing at all.

Here’s an example:

const tasty = (
  <ul>
    <li>Applesauce</li>
    { !baby && <li>Pizza</li> }
    { age > 15 && <li>Brussels Sprouts</li> }
    { age > 20 && <li>Oysters</li> }
    { age > 25 && <li>Grappa</li> }
  </ul>
);

If the expression on the left of the && evaluates as true, then the JSX on the right of the && will be rendered. If the first expression is false, however, then the JSX to the right of the && will be ignored and not rendered.
Instructions

    Checkpoint 1 Passed

    1.

    You’ve been building a React website all about your favorite foods!

    You’re excited to share your website with your friends, and yet at the same time, you fear the cruel, icy harshness of their judgment.

    On line 15, use the && operator to make it so that this expression:

    <li>Nacho Cheez Straight Out The Jar</li>

    will only appear if !judgmental. Feel free to use the example code as a guide.

    When you click Run, every time you refresh the browser, there will be a 50% chance that judgmental will be true. Refresh until you see both versions of your list.



.map in JSX
8 min

The .map() array method comes up often in React. It’s good to get in the habit of using it alongside JSX.

If you want to create a list of JSX elements, then using .map() is often the most efficient way. It can look odd at first:

const strings = ['Home', 'Shop', 'About Me'];

const listItems = strings.map(string => <li>{string}</li>);

<ul>{listItems}</ul>

In the above example, we start out with an array of strings. We call .map() on this array of strings, and the .map() call returns a new array of <li>s.

On the last line of the example, note that {listItems} will evaluate to an array, because it’s the returned value of .map()! JSX <li>s don’t have to be in an array like this, but they can be.

// This is fine in JSX, not in an explicit array:
<ul>
  <li>item 1</li>
  <li>item 2</li>
  <li>item 3</li>
</ul>

// This is also fine!
const liArray = [
  <li>item 1</li>, 
  <li>item 2</li>, 
  <li>item 3</li>
];

<ul>{liArray}</ul>


Advanced JSX
Keys
6 min

When you make a list in JSX, sometimes your list will need to include something called keys:

<ul>
  <li key="li-01">Example1</li>
  <li key="li-02">Example2</li>
  <li key="li-03">Example3</li>
</ul>

A key is a JSX attribute. The attribute’s name is key. The attribute’s value should be something unique, similar to an id attribute.

keys don’t do anything visible! React uses them internally to keep track of lists. If you don’t use keys when you’re supposed to, React might accidentally scramble your list items into the wrong order.

Not all lists need to have keys. A list needs keys if either of the following is true:

    The list items have memory from one render to the next. For instance, when a to-do list renders, each item must “remember” whether it was checked off. The items shouldn’t get amnesia when they render.
    A list’s order might be shuffled. For instance, a list of search results might be shuffled from one render to the next.

If neither of these conditions is true, then you don’t have to worry about keys. If you aren’t sure, then it never hurts to use them!


Your First React Component
Name a Functional Component
2 min

Good! Creating a JavaScript function is the way to declare a new functional component.

When you declare a new functional component, you need to give that component a name. On our finished component, our component’s name was MyComponent:

function MyComponent() {
  return <h1>Hello world</h1>;
}

Function component names must start with capitalization and are conventionally created with PascalCase! Due to how JSX tags are compiled, capitalization indicates that it is a React component rather than an HTML tag.

This is a React-specific nuance! If you are creating a component, be sure to name it starting with a capital letter so it interprets it as a React component. If it begins with a lowercase letter, React will begin looking for a built-in component such as div and input instead and fail.




Your First React Component
The Return Keyword in Functional Components
4 min

When we define a functional component, we essentially define a factory that can build the appropriate combination of elements every time we reference its name. It builds it by consulting a set of instructions that you must provide.

If you’re thinking, “That sounds just like what a regular Javascript function is for”, then you’re right! Functional components can be thought of in a very similar vein to regular Javascript functions, except that their job is to assemble a portion of the interface based on instructions given!

Let’s talk a bit more about these instructions.

For starters, these instructions should take the form of a function declaration body. That means that they will be delimited by curly braces, like this:

function Button() {
  // Instructions go here, between the curly braces.
}

Our instructions can include a combination of markup, CSS, and JavaScript to produce the desired result. The one thing we must always include is a return statement.

The function is expected to produce JSX code that can be used to render something onto the browser screen. Thus, when we define functional components, we must return a JSX element.

function BackButton() {
 return <button>Back To Home</button>;
}

Of course, this doesn’t quite make <button>Back To Home</button> render onto the browser screen yet. We’ve only defined our component.

Let’s keep going so we can see how to render it and why the return statement was necessary!


My Home
Your First React Component: Review
Narrative and Instructions
Learn
Your First React Component
Review
6 min

In this lesson, you’ve learned about a foundational React concept: components.

Before you go, here’s a recap:

    React applications are made up of components.
    Components are responsible for rendering pieces of the user interface.
    To create components and render them, react and reactDOM must be imported.
    React components can be defined with Javascript functions to make function components.
    Function component names must start with a capitalized letter, and Pascal case is the adopted naming convention.
    Function components must return some React elements in JSX syntax.
    React components can be exported and imported from file to file.
    A React component can be used by calling the component name in an HTML-like self-closing tag syntax.
    Rendering a React component requires using .createRoot() to specify a root container and calling the .render() method on it.

Phew! That was a lot, but components are at the core of React and they’re one of the reasons why React is such a powerful tool!


## July 19th, 2024 ##

Components and Advanced JSX
Putting Logic in a Function Component
11 min

A function component must have a return statement. However, that isn’t all that it can have.

You can also put simple calculations that need to happen before returning your JSX element within the function component.

Here’s an example of some calculations that can be done inside a function component:

function RandomNumber() {
  //First, some logic that must happen before returning
  const n = Math.floor(Math.random() * 10 + 1);
  //Next, a return statement using that logic: 
  return <h1>{n}</h1>
}

Watch out for this common mistake:

function RandomNumber() {
  return (
    const n = Math.floor(Math.random() * 10 + 1);
    <h1>{n}</h1>
  )
}

In the above example, the line with the const n declaration will cause a syntax error, as it should come before the return.


Event Listener and Event Handlers in a Component
6 min

Your function components can include event handlers. With event handlers, we can run some code in response to interactions with the interface, such as clicking.

function MyComponent(){
  function handleHover() {
    alert('Stop it.  Stop hovering.');
  }
  return <div onHover={handleHover}></div>;
}

In the above example, the event handler is handleHover(). It is passed as a prop to the JSX element <div>. We’ll discuss more on props in a later lesson, but for now, understand that props are information passed to a JSX tag.

The logic for what should happen when the <div> is hovered on is contained inside the handleHover() function. The function is then passed to the <div> element.

Event handler functions are defined inside the function component and, by convention, start with the word “handle” followed by the type of event it is handling.

There’s a small quirk you should watch out for. Take a look at this line again:

return <div onHover={handleHover}></div>

The handleHover() function is passed without the parentheses we would typically see when calling a function. This is because passing it as handleHover indicates it should only be called once the event has happened. Passing it as handleHover() would trigger the function immediately, so be careful!



Components Render Other Components
Returning Another Component
3 min

As we’ve seen before, each React component is responsible for one piece of the interface. As the application grows in complexity, components need to be able to interact with each other to support the features needed.

So far, we’ve explored components that return JSX elements, such as:

function PurchaseButton() {
  return <button onClick={()=>{alert("Purchase Complete")}}>Purchase</button>
}

In this example, the React component is not interacting with other components. However, you can have components interact with each other by passing information or even returning other components.

function PurchaseButton() {
  return <button onClick={()=>{alert("Purchase Complete")}}>Purchase</button>
}

function ItemBox() {
  return (
    <div>
      <h1>50% Sale</h1>
      <h2>Item: Small Shirt</h2>
      <PurchaseButton />
    </div>
  );
}

In the above example, ItemBox returns an instance of PurchaseButton. This is an example of how a component can reference other components!



Components must be capatilized! Otherwise breaks react. 
wont let you access anything (remember pokemon app lol)



## July 21st, 2024 ##

Props
Pass `props` to a Component
5 min

To take advantage of props, we need to pass information to a React component. In the previous exercise, we rendered an empty props object because we did not pass any props to our PropsDisplayer component.

How do we pass props? By giving the component an attribute:

<Greeting name="Jamel" />

Let’s say that you want to pass a component the message, "We're great!". Here’s how you can do it:

<SloganDisplay message="We're great!" />

As you can see, to pass information to a component, you need a name for the information that you want to pass.

In the above example, we used the name message. You can use any name you want.

If you want to pass information that isn’t a string, then wrap that information in curly braces. Here’s how you would pass an array:

<Greeting myInfo={["Astronaut", "Narek", "43"]} />

In this next example, we pass several pieces of information to <Greeting />. The values that aren’t strings are wrapped in curly braces:

<Greeting name="The Queen Mary" city="Long Beach, California" age={56} haunted={true} />


Props
Render a Component's props
7 min

Props allow us to customize the component by passing it information.

We’ve learned how to pass information to a component’s props object. You will often want a component to display the information that you pass.

To make sure that a function component can use the props object, define your function component with props as the parameter:

function Button(props) {
  return <button>{props.displayText}</button>;
}

In the example, props is accepted as a parameter, and the object values are accessed with the dot notation accessors pattern (object.propertyName).

Alternatively, since props is an object, you can also use destructuring syntax like so:

function Button({displayText}) {
  return <button>{displayText}</button>;
}


Props
Pass props From Component To Component
10 min

You have learned how to pass a prop to a component:

<Greeting firstName="Esmerelda" />

You have also learned how to access and display a passed-in prop:

return <h1>{props.firstName}</h1>;

The most common use of props is to pass information to a component from a different component.

Props in React travel in a one-way direction, from the top to bottom, parent to child.

Let’s explore the parent-child relationship of passing props a bit further.

function App() {
    return <Product name="Apple Watch" price = {399} rating = "4.5/5.0" />;
}

In this example, App is the parent and Product is the child. App passes three props to Product (name, price, and rating), which can then be read inside the child component.

Props passed down are immutable, meaning they cannot be changed. If a component wants new values for its props, it needs to rely on the parent component to pass it new ones.

Let’s practice this!


Props
Render Different UI Based on props
8 min

You can do more with props than just display them. You can also use props to make decisions.

function LoginMsg(props) {
  if (props.password === 'a-tough-password') {
    return <h2>Sign In Successful.</h2>
  } else {
    return <h2>Sign In Failed..</h2>
  }
}

In this example, we use the props passed in to make a decision rather than rendering the value to the screen.

If the password received is equal to 'a-tough-password', the resulting message in <h2></h2> will be different!

The passed-in password is not displayed in either case! The prop is used to decide what will be displayed. This is a common technique.


Props
handleEvent, onEvent, and props.onEvent
10 min

Let’s talk about naming things.

When you pass an event handler as a prop, as you just did, there are two names that you have to choose. Both naming choices occur in the parent component, the component that defines the event handler and passes it.

The first name that you have to choose is the name of the event handler itself.

Look at Talker.js, lines 5 through 11. This is our event handler. We chose to name it talk.

The second name that you have to choose is the name of the prop that you will use to pass the event handler. This is the same thing as the attribute name.

For our prop name, we also chose talk, as shown on line 12:

return <Button talk={talk} />;

These two names can be whatever we want. However, there is a naming convention that is commonly used.

Here’s how the naming convention works: first, think about what type of event you are listening for. In our example, the event type was “click”. If you are listening for a “click” event, then you name your event handler handleClick. If you are listening for a “hover” event, then you name your event handler handleHover:

function myClass() {
  function handleHover() {
    alert('I am an event handler.');
    alert('I will be called in response to "hover" events.');
  }
}

Your prop name should be the word on, plus your event type. If you are listening for a “click” event, then you name your prop onClick. If you are listening for a “hover” event, then you name your prop onHover:

function myClass(){
  function handleHover() {
    alert('I am an event handler.');
    alert('I will listen for a "hover" event.');
  }
   return <Child onHover={handleHover} />;
}


One major source of confusion is the fact that names like onClick have special meanings, but this is only if they’re used on HTML-like elements.

Look at Button.js. When you give the <button> element an attribute named onClick, then this onClick attribute has a special purpose. As you’ve learned, this special onClick attribute creates an event listener that listens for clicks on the <button> element:

// In Button.js: The onClick attribute creates an event listener:
<button onClick={props.onClick}>
  Click me!
</button>

Now, look at Talker.js. Here, the onClick attribute you gave to <Button /> does not create an event listener—it’s just a name of an attribute:

// In Talker.js: The onClick attribute is just a normal attribute name.
<Button onClick={handleClick} />

The reason for this is that <Button /> is not an HTML-like JSX element; it’s a component instance.

Names like onClick only create event listeners if they’re used on HTML-like JSX elements. Otherwise, they’re just ordinary prop names.

Run your program to ensure your button is working as intended.


Props
props.children
11 min

Every component’s props object has a property named children.

props.children will return everything in between a component’s opening and closing JSX tags.

So far, all of the components that you’ve seen have been self-closing tags, such as <MyFunctionComponent />. They don’t have to be! You could write <MyFunctionComponent></MyFunctionComponent>, and it would still work.

props.children would return everything in between <MyFunctionComponent> and </MyFunctionComponent>.

By using props.children, we can separate the outer component, MyFunctionComponent in this case, from the content, which makes it flexible and reusable.

Look at BigButton.js.

    In Example 1, <BigButton>‘s props.children would equal the text, “I am a child of BigButton.”
    In Example 2, <BigButton>‘s props.children would equal a <LilButton /> component.
    In Example 3, <BigButton>‘s props.children would equal undefined.

If a component has more than one child between its JSX tags, then props.children will return those children in an array. However, if a component has only one child, then props.children will return the single child, not wrapped in an array.


Props
Giving Default Values to props
7 min

Take a look at the Button component. Notice that on line 6, Button expects to receive a prop named text. The received text will be displayed inside of a <button> element.

What if nobody passes any text to Button?

If nobody passes any text to Button, then Button‘s display will be blank. It would be better if Button could display a default message instead.

You can make this happen by specifying a default value for the prop. There are three ways to do this!

The first method is adding a defaultProps static property to the component:

function Example(props) {
  return <h1>{props.text}</h1>
}

Example.defaultProps = {
  text: 'This is default text',
};

You can also specify the default value directly in the function definition:

function Example({text='This is default text'}) {
   return <h1>{text}</h1>
}

Lastly, you can also set the default value in the function body:

function Example(props) {
  const {text = 'This is default text'} = props;
  return <h1>{text}</h1>
}

If an <Example /> doesn’t get passed any text, then it will display “This is default text”.

If an <Example /> does get passed some text, then it will display that passed-in text.


## July 22nd, 2024 ##

The State Hook
Why Use Hooks?
8 min

What should we do if we want to add a state to our function component? How about if we wanted our app to respond to the changes in data?

In this lesson, we’ll learn about React Hooks and how they can help us powerfully wield function components.

React Hooks, plainly put, are functions that let us manage the internal state of components and handle post-rendering side effects directly from our function components. Using Hooks, we can determine what we want to show the users by declaring how our user interface should look based on the state.

React offers a number of built-in Hooks. A few of these include useState(), useEffect(), useContext(), useReducer(), and useRef(). See the full list in the React docs.

In this lesson, we’ll learn how to:

    Build a “stateful” function component.
    Use the State Hook.
    Initialize a state and set a state.
    Define event handlers.
    Use state setter callback functions.
    Use state with arrays and objects.

The State Hook
Initialize State
8 min

Like how you used the State Hook to manage a variable with string values, we can use the State Hook to manage the value of any primitive data type and even data collections like arrays and objects!

Have a look at the following function component. What data type does this state variable hold?

import React, { useState } from 'react';

function ToggleLoading() {
  const [isLoading, setIsLoading] = useState();

  return (
    <div>
      <p>The data is {isLoading ? 'Loading' : 'Not Loading'}</p>
      <button onClick={() => setIsLoading(true)}>
        Turn Loading On
      </button>
      <button onClick={() => setIsLoading(false)}>
        Turn Loading Off
      </button>
    </div>
  );
}

The ToggleLoading() function component above uses the simplest of all data types, a boolean. Booleans are frequently used in React applications to represent whether data has loaded or not. In the example above, we see that true and false values are passed to the state setter, setIsLoading().

This code works just fine as is, but what if we want our component to start off with isLoading set to true?

To initialize our state with any value we want, we simply pass the initial value as an argument to the useState() function call.

const [isLoading, setIsLoading] = useState(true);

There are three ways in which this code affects our component:

    During the first render, the initial state argument is used.
    When the state setter is called, React ignores the initial state argument and uses the new value.
    When the component re-renders for any other reason, React continues to use the same value from the previous render.

If we don’t pass an initial value when calling useState(), the current value of the state during the first render will be undefined. Often, this is perfectly fine for the computers running the code, but it can be unclear to the humans reading our code. So, we prefer to explicitly initialize our state. If we don’t have the value needed during the first render, we can explicitly pass null instead of passively leaving the value as undefined.


The State Hook
Use State Setter Outside of JSX
18 min

Let’s see an example of managing the changing value of a string as a user types into a text input field:

import React, { useState } from 'react';

export default function EmailTextInput() {
  const [email, setEmail] = useState('');
  const handleChange = (event) => {
    const updatedEmail = event.target.value;
    setEmail(updatedEmail);
  }

  return (
    <input value={email} onChange={handleChange} />
  );
}

Here’s a breakdown of how the above code works:

    We use array destructuring to create our local state variable email and our local setter function setEmail().
    The local variable email is assigned the current state value at index 0 from the array returned by useState().
    The local variable setEmail() is assigned a reference to the state setter function at index 1 from the array returned by useState().
    It’s a convention to name the setter variable using the current state variable (in this example, email) with “set” prepended.

The JSX input tag has an event listener called onChange. This event listener calls an event handler each time the user types something in this element. In the example above, our event handler is defined inside of the definition for our function component, but outside of our JSX. Earlier in this lesson, we wrote our event handlers right in our JSX. Those inline event handlers work perfectly fine, but when we want to do something more interesting than just calling the state setter with a static value, it’s a good practice to separate that logic from our JSX. This separation of concerns makes our code easier to read, test, and modify.

It’s common in React code to simplify this:

const handleChange = (event) => {
  const newEmail = event.target.value;
  setEmail(newEmail);
}

to this:

const handleChange = (event) => setEmail(event.target.value);

or, using object destructuring, this:

const handleChange = ({target}) => setEmail(target.value);

All three code snippets above behave the same way, so there really isn’t a right and wrong between these different code snippets. We’ll use the last, most concise version moving forward.



The State Hook
Set From Previous State
21 min

In the previous exercise, we learned to update the state by passing it a new value like this:

setState(newStateValue);

However, React state updates are asynchronous. This means that there are some scenarios where portions of your code will run before the state is finished updating.

This is a good and a bad thing! Grouping the state updates together can improve performance in your application, but it can result in outdated state values. Consequently, it is best practice to update a state with a callback function, preventing accidental outdated values.

Let’s take a look at the following code to see how it’s done:

import React, { useState } from 'react';
 
export default function Counter() {
  const [count, setCount] = useState(0);
 
  const increment = () => setCount(prevCount => prevCount + 1);
 
  return (
    <div>
      <p>Wow, you've clicked that button: {count} times</p>
      <button onClick={increment}>Click here!</button>
    </div>
  );
}

When the button is pressed, the increment() event handler is called. Inside this function, we use our setCount() state setter with a callback function.

Because the next value of count depends on the previous value of count, we pass a callback function as the argument for setCount() instead of a value (as we’ve done in previous exercises).

setCount(prevCount => prevCount + 1)

When our state setter calls the callback function, this state setter callback function takes our previous count as an argument. The value returned by this state setter callback function is used as the next value of count (in this case, prevCount + 1).

We can also just call setCount(count +1) and it would work the same in this example, but for reasons that are out of scope for this lesson, it is safer to use the callback method.


The State Hook
Objects in State
22 min

We can also use state with objects. When we work with a set of related variables, it can be very helpful to group them into an object. Let’s look at an example of this in action.

export default function Login() {
  const [formState, setFormState] = useState({});
  const handleChange = ({ target }) => {
    const { name, value } = target;
    setFormState((prev) => ({
      ...prev,
      [name]: value
    }));
  };

  return (
    <form>
      <input
        value={formState.firstName}
        onChange={handleChange}
        name="firstName"
        type="text"
      />
      <input
        value={formState.password}
        onChange={handleChange}
        type="password"
        name="password"
      />
    </form>
  );
}

A few things to notice:

    We use a state setter callback function to update a state based on the previous value.
    The spread syntax is the same for objects as for arrays: { ...oldObject, newKey: newValue }.
    We reuse our event handler across multiple inputs by using the input tag’s name attribute to identify which input the change event came from.

Once again, when updating the state with setFormState() inside a function component, we do not modify the same object. We must copy over the values from the previous object when setting the next value of a state. Thankfully, the spread syntax makes this super easy to do!

Anytime one of the input values is updated, the handleChange() function will be called. Inside this event handler, we use object destructuring to unpack the target property from our event object, then we use object destructuring again to unpack the name and value properties from the target object.

Inside our state setter callback function, we wrap our curly brackets in parentheses like so:

setFormState((prev) => ({ ...prev }))

This tells JavaScript that our curly brackets refer to a new object to be returned. We use ..., the spread operator, to fill in the corresponding fields from our previous state. Finally, we overwrite the appropriate key with its updated value.

Did you notice the square brackets around the name? This Computed Property Name allows us to use the string value stored by the name variable as a property key.

The State Hook
Separate Hooks for Separate States
11 min

While there are times when it can be helpful to store related data in a data collection, like an array or object, it can also be helpful to create different state variables for data that change separately. Managing dynamic data is much easier when we keep our data models as simple as possible.

For example, if we had a single object that held state for a subject you are studying at school, it might look something like this:

function Subject() {
  const [state, setState] = useState({
    currentGrade: 'B',
    classmates: ['Hasan', 'Sam', 'Emma'],
    classDetails: {topic: 'Math', teacher: 'Ms. Barry', room: 201},
    exams: [{unit: 1, score: 91}, {unit: 2, score: 88}]
  })}

This would work, but think about how messy it could get to copy over all the other values when we need to update something in this big state object. For example, to update the grade on an exam, we would need an event handler that did something like this:

setState((prev) => ({
 ...prev,
  exams: prev.exams.map((exam) => {
    if( exam.unit === updatedExam.unit ){
      return { 
        ...exam,
        score: updatedExam.score
      };
    } else {
      return exam;
    }
  }),
}));

Complex code like this is likely to cause bugs. It’s best to create multiple state variables based on which values tend to change together.

We can rewrite the previous example as follows:

function Subject() {
  const [currentGrade, setGrade] = useState('B');
  const [classmates, setClassmates] = useState(['Hasan', 'Sam', 'Emma']);
  const [classDetails, setClassDetails] = useState({topic: 'Math', teacher: 'Ms. Barry', room: 201});
  const [exams, setExams] = useState([{unit: 1, score: 91}, {unit: 2, score: 88}]);
  // ...
}

Managing dynamic data with separate state variables has many advantages, like making our code more simple to write, read, test, and reuse across components.

Often, we find ourselves packaging and organizing data in collections to pass between components, then separating that data within components where different parts of the data change separately. The wonderful thing about working with Hooks is that we have the freedom to organize our data in the way that makes the most sense to us!


The State Hook
Review
6 min

We can now build stateful function components using the useState React Hook!

Let’s review what we learned and practiced in this lesson:

    With React, we feed static and dynamic data models to JSX to render a view to the screen.
    Hooks are used to “hook into” the internal component state for managing dynamic data in function components.
    We employ the State Hook using the code below. The currentState references the current value of the state and initialState initializes the value of the state for the component’s first render.

const [currentState, stateSetter] = useState( initialState );

    State setters can be called in event handlers.
    We can define simple event handlers inline in our JSX and complex event handlers outside of our JSX.
    We use a state setter callback function when our next value depends on our previous value.
    We use arrays and objects to organize and manage related data that tend to change together.
    Use the spread syntax on collections of dynamic data to copy the previous state into the next state like so: setArrayState((prev) => [ ...prev ]) and setObjectState((prev) => ({ ...prev })).
    It’s best practice to have multiple, simpler states instead of having one complex state object.


## July 23rd, 2024 ##

## July 24th, 2024 ##

useState & useEffect

The Effect Hook
Why Use useEffect?
2 min

Before Hooks, function components were only used to accept data in the form of props and return some JSX to be rendered. However, as we learned in the last lesson, the State Hook allows us to manage dynamic data, in the form of component state, within our function components.

In this lesson, we’ll use the Effect Hook to run some JavaScript code after each render to:

    fetch data from a back-end service.
    subscribe to a stream of data.
    manage timers and intervals.
    read from and make changes to the DOM.

Components will re-render multiple times throughout their lifetime. These key moments present the perfect opportunity to execute these “side effects”.

There are three key moments when the Effect Hook can be utilized:

    When the component is first added, or mounted, to the DOM and renders.
    When the state or props change, causing the component to re-render.
    When the component is removed, or unmounted, from the DOM.

Later on in this lesson, we’ll learn how to further fine-tune exactly when the Effect Hook executes.


The Effect Hook
Function Component Effects
13 min

The Effect Hook tells our component to do something every time it’s rendered (or re-rendered). Combined with states, we can use the Effect Hook to create interesting dynamic changes in our web pages!

Suppose we want to allow a user to change the title of the web page tab every time they type. We can implement this with the Effect Hook (useEffect()) like so:

import React, { useState, useEffect } from 'react';
 
function PageTitle() {
  const [name, setName] = useState('');
 
  useEffect(() => {
    document.title = `Hi, ${name}`;
  });
 
  return (
    <div>
      <p>Use the input field below to rename this page!</p>
      <input onChange={({target}) => setName(target.value)} value={name} type='text' />
    </div>
  );
}

Let’s take a look at the above example in more detail. First, we import the Effect Hook from the 'react' library:

import { useEffect } from 'react';

The useEffect() function has no return value as the Effect Hook is used to call another function. We pass the callback function, or effect, to run after a component renders as the argument of the useEffect() function. In our example, the following effect runs after each time the PageTitle component renders:

() => { document.title = `Hi, ${name}`;}

Here, we assign Hi, ${name} as the value of document.title.

The onChange event listener triggers the PageTitle component to be re-rendered every time the user types in the input. Consequently, this triggers useEffect() and changes the document’s title.

Notice how we use the current state inside of our effect. Even though our effect is called after the component renders, we still have access to the variables in the scope of our function component! When React renders our component, it will update the DOM as usual, and then run our effect after the DOM has been updated. This happens for every render, including the first and last one.


The Effect Hook
Clean Up Effects
16 min

Some effects require cleanup. For example, we might want to add event listeners to some element in the DOM, beyond the JSX in our component. When we add event listeners to the DOM, it is important to remove those event listeners when we are done with them to avoid memory leaks!

Let’s consider the following effect:

useEffect(()=>{
  document.addEventListener('keydown', handleKeyPress);
  // Specify how to clean up after the effect:
  return () => {
    document.removeEventListener('keydown', handleKeyPress);
  };
})

If our effect didn’t return a cleanup function, a new event listener would be added to the DOM’s document object every time that our component re-renders. Not only would this cause bugs, but it could cause our application performance to diminish and maybe even crash!

Because effects run after every render and not just once, React calls our cleanup function before each re-render and before unmounting to clean up each effect call.

If our effect returns a function, then the useEffect() Hook always treats that as the cleanup function. React will call this cleanup function before the component re-renders or unmounts. Since this cleanup function is optional, it is our responsibility to return a cleanup function from our effect when our effect code could create memory leaks.


The Effect Hook
Clean Up Effects
16 min

Some effects require cleanup. For example, we might want to add event listeners to some element in the DOM, beyond the JSX in our component. When we add event listeners to the DOM, it is important to remove those event listeners when we are done with them to avoid memory leaks!

Let’s consider the following effect:

useEffect(()=>{
  document.addEventListener('keydown', handleKeyPress);
  // Specify how to clean up after the effect:
  return () => {
    document.removeEventListener('keydown', handleKeyPress);
  };
})

If our effect didn’t return a cleanup function, a new event listener would be added to the DOM’s document object every time that our component re-renders. Not only would this cause bugs, but it could cause our application performance to diminish and maybe even crash!

Because effects run after every render and not just once, React calls our cleanup function before each re-render and before unmounting to clean up each effect call.

If our effect returns a function, then the useEffect() Hook always treats that as the cleanup function. React will call this cleanup function before the component re-renders or unmounts. Since this cleanup function is optional, it is our responsibility to return a cleanup function from our effect when our effect code could create memory leaks.
Instructions

    Checkpoint 1 Passed

    1.

    Let’s create a program that documents how many times you’ve clicked on the page.

    Write an event handler named increment() that will be responsible for tracking how many times a user has clicked. Define this function so that it calls setClickCount() with a state setter callback function, adding 1 to the previous value of clickCount.

Our state setter callback function should accept a single argument, add 1 to it, then return that value, like so: (prev) => prev + 1.

This callback function is called by our state setter, which is called by our event handler, like so:

const increment = () => setClickCount(stateSetterCallbackFunction);

Checkpoint 2 Passed

2.

Import the useEffect() hook and call it with an effect that adds an event listener for 'mousedown' events on the document object. When a 'mousedown' event occurs anywhere on the document, we want our increment() event handler to be called.
Checkpoint 3 Passed

3.

If you haven’t already, run our code and click around the browser window. What is happening? Why is this happening?

Each time that our component renders, our effect is called, adding another event listener. With just a few clicks and rerenders, we have attached a lot of event listeners to the DOM! We need to clean up after ourselves!

Update our effect so that it returns a cleanup function that will remove our last event listener from the DOM.


import React, { useState, useEffect } from 'react';

export default function Counter() {
  const [clickCount, setClickCount] = useState(0);

  // your code here
  const increment = () => {
    setClickCount(prev => prev+ 1);
  }

  useEffect(() => {
    document.addEventListener('mousedown', increment);
    return () => {
      document.removeEventListener('mousedown', increment)
    };
});



The Effect Hook
Control When Effects Are Called
28 min

The useEffect() function calls its first argument (the effect) after each time a component renders. We’ve learned how to return a cleanup function so that we don’t create performance issues and other bugs, but sometimes we want to skip calling our effect on re-renders altogether.

It is common, when defining function components, to run an effect only when the component mounts (renders the first time), but not when the component re-renders. The Effect Hook makes this very easy for us to do! If we want to only call our effect after the first render, we pass an empty array to useEffect() as the second argument. This second argument is called the dependency array.

The dependency array is used to tell the useEffect() method when to call our effect and when to skip it. Our effect is always called after the first render but only called again if something in our dependency array has changed values between renders.

We will continue to learn more about this second argument over the next few exercises, but for now, we’ll focus on using an empty dependency array to call an effect when a component first mounts, and if a cleanup function is returned by our effect, calling that when the component unmounts.

useEffect(() => {
  alert("component rendered for the first time");
  return () => {
    alert("component is being removed from the DOM");
  };
}, []); 

Without passing an empty array as the second argument to the useEffect() above, those alerts would be displayed before and after every render of our component, which is clearly not when those messages are meant to be displayed. Simply passing [] to the useEffect() function is enough to configure when the effect and cleanup functions are called!


The Effect Hook
Fetch Data
25 min

When building software, we often start with default behaviors and then modify them to improve performance.

We’ve learned that the default behavior of the Effect Hook is to call the effect function after every single render.

Next, we learned that we can pass an empty array as the second argument for useEffect() if we only want our effect to be called after the component’s first render.

In this exercise, we’ll learn to use the dependency array to further configure exactly when we want our effect to be called!

When our effect is responsible for fetching data from a server, we pay extra close attention to when our effect is called. Unnecessary round trips back and forth between our React components and the server can be costly in terms of:

    Processing
    Performance
    Data usage for mobile users
    API service fees

When the data that our components need to render doesn’t change, we can pass an empty dependency array so that the data is fetched after the first render. When the response is received from the server, we can use a state setter from the State Hook to store the data from the server’s response in our local component state for future renders. Using the State Hook and the Effect Hook together in this way is a powerful pattern that saves our components from unnecessarily fetching new data after every render!

An empty dependency array signals to the Effect Hook that our effect never needs to be re-run, that it doesn’t depend on anything. Specifying zero dependencies means that the result of running that effect won’t change and calling our effect once is enough.

A dependency array that is not empty signals to the Effect Hook that it can skip calling our effect after re-renders unless the value of one of the variables in our dependency array has changed. If the value of a dependency has changed, then the Effect Hook will call our effect again!

Here’s a nice example from the official React docs:

useEffect(() => {
  document.title = `You clicked ${count} times`;
}, [count]); // Only re-run the effect if the value stored by count changes



The Effect Hook
Rules of Hooks
17 min

There are two main rules to keep in mind when using Hooks:

    Only call Hooks at the top level.
    Only call Hooks from React functions.

As we have been practicing with the State Hook and the Effect Hook, we’ve been following these rules with ease, but it is helpful to keep these two rules in mind as you take your new understanding of Hooks out into the wild and begin using more Hooks in your React applications.

When React builds the Virtual DOM, the library calls the functions that define our components over and over again as the user interacts with the user interface. React keeps track of the data and functions that we are managing with Hooks based on their order in the function component’s definition. For this reason, we always call our Hooks at the top level; we never call hooks inside of loops, conditions, or nested functions.

Instead of confusing React with code like this:

if (userName !== '') {
  useEffect(() => {
    localStorage.setItem('savedUserName', userName);
  });
}

We can accomplish the same goal while consistently calling our Hook every time:

useEffect(() => {
  if (userName !== '') {
    localStorage.setItem('savedUserName', userName);
  }
});

Secondly, Hooks can only be used in React Functions. We’ve been working with useState() and useEffect() in function components, and this is the most common use. The only other place where Hooks can be used is within custom hooks. Custom Hooks are incredibly useful for organizing and reusing stateful logic between function components.
The Effect Hook
Separate Hooks for Separate Effects
20 min

When multiple values are closely related and change at the same time, it can make sense to group these values in a collection like an object or array. Packaging data together can also add complexity to the code responsible for managing that data. Therefore, it is a good idea to separate concerns by managing different data with different Hooks.

Compare the complexity here, where data is bundled up into a single object:

// Handle both position and menuItems with one useEffect hook.
const [data, setData] = useState({ position: { x: 0, y: 0 } });
useEffect(() => {
  get('/menu').then((response) => {
    setData((prev) => ({ ...prev, menuItems: response.data }));
  });
  const handleMove = (event) =>
    setData((prev) => ({
      ...prev,
      position: { x: event.clientX, y: event.clientY }
    }));
  window.addEventListener('mousemove', handleMove);
  return () => window.removeEventListener('mousemove', handleMove);
}, []);

To the simplicity here, where we have separated concerns:

// Handle menuItems with one useEffect hook.
const [menuItems, setMenuItems] = useState(null);
useEffect(() => {
  get('/menu').then((response) => setMenuItems(response.data));
}, []);

// Handle position with a separate useEffect hook.
const [position, setPosition] = useState({ x: 0, y: 0 });
useEffect(() => {
  const handleMove = (event) =>
    setPosition({ x: event.clientX, y: event.clientY });
  window.addEventListener('mousemove', handleMove);
  return () => window.removeEventListener('mousemove', handleMove);
}, []);

It is not always obvious whether to bundle data together or separate it, but with practice, we get better at organizing our code so that it is easier to understand, add to, reuse, and test!



The Effect Hook
Review
1 min

In this lesson, we learned how to write effects that manage timers, manipulate the DOM, and fetch data from a server. With the Effect Hook, we can perform these types of actions in function components with ease!

Let’s review the main concepts from this lesson:

    We can import the useEffect() function from the 'react' library and call it in our function components.
    Effect refers to a function that we pass as the first argument of the useEffect() function. By default, the Effect Hook calls this effect after each render.
    The cleanup function is optionally returned by the effect. If the effect does anything that needs to be cleaned up to prevent memory leaks, then the effect returns a cleanup function, then the Effect Hook will call this cleanup function before calling the effect again as well as when the component is being unmounted.
    The dependency array is the optional second argument that the useEffect() function can be called with in order to prevent repeatedly calling the effect when this is not needed. This array should consist of all variables that the effect depends on.

The Effect Hook is all about scheduling when our effect’s code gets executed. We can use the dependency array to configure when our effect is called in the following ways:
Dependency Array 	Effect called after first render & …
undefined 	every re-render
Empty array 	no re-renders
Non-empty array 	when any value in the dependency array changes

Hooks give us the flexibility to organize our code in different ways, grouping related data as well as separating concerns to keep code simple, error-free, reusable, and testable!

  



  return (
      <h1>Document Clicks: {clickCount}</h1>
  );
}


## July 26th, 2024 ##

<>


</>

fragment that you can wrap your jsx in like a <div></div> without creating a div element in the dom

don't forget that list items need keys in React.


## July 27th, 2024 ##


.slice()
is good for arrays

kDramas.slice(0, 3) will return the first 3 elements from the array kDramas.

can also be really powerful when added to

i.e

can use map for it to

  so kDramas.slice(0,3).map(drama => {
   function()
   }) 

   will return whatever you've mapped in the function but only applies to first 3 items in array.

   so for React, you can create a page that displays only the first 3 objects on the screen instead of entire array. 
  }

## July 29th, 2024 ##

React Programming Patterns
Create Container Component
7 min

Separating container components from presentational components is a popular React programming pattern.

The functional part of a component (maintaining a state, making calculations based on props, etc.) can be separated into a container component, also known as a stateful component.

This container component will be in charge of maintaining the state (creating and updating) and passing it on (we’ll see this later) to any component it renders through props.


React Programming Patterns
Parent/Child and Sibling/Sibling Communication
11 min

We’ve seen how container components communicate with presentational components by passing their state through props, but how do presentational components communicate changes to the container?

One idea would be to update the props directly like this:

function Presentational(props) {
  const buttonClickHandler = () => {
    props.isActive = !props.isActive
  }
  // rest of code
}

But this would not be correct because components should never directly update their props. Recall that React functional components should be pure functions and updating prop values directly would violate that principle.

In order for a presentation (stateless) component to communicate changes to a container (stateful) component, the container component must define and provide a way for the presentational component to communicate with it using a change handler function passed as a prop.

For example:

function Container() {
  const [isActive, setIsActive] = useState(false);                              
                                
  return (
    <>
      <Presentational active={isActive} toggle={setIsActive}/>
      <OtherPresentational active={isActive}/>
    </>
    );                          
  }
                        
function Presentational(props) {
  return (
    <h1>Engines are {props.active}</h1>
    <button onClick={() => props.toggle(!props.active)}>Engine Toggle</button>
  );
}
                            
function OtherPresentational(props) {
  // render...
}

In the example above, Container maintains the isActive state and passes setIsActive to Presentational through the toggle prop. When Presentational needs to communicate a change to the active prop, it uses the function passed to it through the toggle prop.

Using this pattern also indirectly results in communication between sibling components (components with a common parent), as shown in the example above. When Presentational communicates a change through toggle, it causes a state update in Container, which provides the updated value for isActive to both Presentational and OtherPresentational through the active prop.



React Programming Patterns
Review
<1 min

Congrats! You’ve learned your first programming pattern to help organize your React code. You divided a complex React component into a container component and a couple of presentational components.

Here are the steps we took:

    Identified that the original component needed to be refactored: it handled calculations/logic and presentation/rendering.
    Created a container component containing all the stateful logic.
    Created a function that calls the state setter method provided by useState().
    Created and exported presentational components containing only JSX.
    Imported the presentational components into the container component.
    Used the presentational components in the return statement of the container component.
    Passed state and functions used to change state as props to the rendered presentational components.

In this programming pattern, the container component does the work of figuring out what to display using state. The presentational component does the work of actually displaying the state through props. If a component does a significant amount of work in both areas, then that’s a sign that you should use this pattern!


React Styles
Style Syntax
4 min

There are a few things to keep in mind when styling components with JSX.

Just like how we reference CSS properties in the style object of the DOM in JavaScript, we write CSS property names using camelCase in React:

const styles = {
  marginTop: '20px',
  backgroundColor: 'green'
};

This syntax comes from a small rule. A hyphen is a reserved operator in JavaScript. If we use background-color, the hyphen is then interpreted as a minus sign. Thus, we want to be consistent with the property names in the DOM style JavaScript object and use camel case.

In regular JavaScript, style values are almost always strings. Even if a style value is numeric, you usually have to write it as a string so that you can specify a unit. For example, you’d write '450px' or '20%'.

If you write a style value as a number, then the unit 'px' is assumed. For example, if you want a font size of 30px, you can write:

{ fontSize: 30 }

If you want to use units other than 'px', you can use a string:

{ fontSize: "2em" }

Specifying the 'px' unit in a string will still work, although it’s redundant.

A few specific styles will not automatically fill in the px for you. These are styles where you aren’t likely to use 'px' anyway, so you don’t really have to worry about them.


React Styles
Multiple Stylesheets
10 min

While inline styles and style object variables are valid methods of styling in React, it can become organizationally difficult to keep track of the styles being applied as your application grows.

One way to make styles modular, organized, and reusable is to create separate stylesheets for each component.

We can import a stylesheet by using the import keyword:

import './App.css'

However, if we have multiple stylesheets with the same class names, the names can collide and create style conflicts.

One way to prevent this is to use CSS modules. By importing it as a module, the styles will only be available for the component that imported the style. This is done automatically by creating unique class names for each module. This frees us from having to keep track of the class names we’ve used across stylesheets.

To use CSS modules, we begin by naming our stylesheet in this format, where fileName should be replaced with the name of the component you’re styling:

fileName.module.css

This indicates that the file should be processed as a CSS module.

Then, it must be imported into the file containing our component.

import styles from './fileName.module.css'

From this import, we can see that the styles object now holds the class selectors of fileName.module.css. To access the selectors, we use the dot notation like so:

<div className={styles.divStyle}></div>

Note that we apply styles using the className attribute rather than class. class is a reserved JavaScript keyword, so React uses className to avoid conflicts.

Although React does not have an opinion on how styles should be defined, this is the preferred method for styling in React, as it maintains the compositional philosophy of React.

