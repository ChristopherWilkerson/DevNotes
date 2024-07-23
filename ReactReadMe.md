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

