## June 30th, 2024

# DOM Events with JavaScript
Event Handler Registration
12 min

You’re doing great! Now it’s time to dive into using event handler functions to create interactivity.

Using the .addEventListener() method, we can have a DOM element listen for a specific event and execute a block of code when the event is detected. The DOM element that listens for an event is called the event target and the block of code that runs when the event happens is called the event handler.

Let’s take a look at the code below:

let eventTarget = document.getElementById('targetElement');

eventTarget.addEventListener('click', function() {
  // this block of code will run when click event happens on eventTarget element
});

Let’s break this down!

    We selected our event target from the DOM using document.getElementById('targetElement').
    We used the .addEventListener() method on the eventTarget DOM element.
    The .addEventListener() method takes two arguments: an event name in string format and an event handler function. We will learn about different values we can use as event names in a later lesson.
    In this example, we used the 'click' event, which fires when the user clicks on eventTarget.
    The code block in the event handler function will execute when the 'click' event is detected.

Instead of using an anonymous function as the event handler, it’s best practice to create a named event handler function. Your code will remain organized and reusable this way, even if your code gets complex. Check out the syntax:

function eventHandlerFunction() {
  // this block of code will run when click event happens
}

eventTarget.addEventListener('click', eventHandlerFunction);

The named function eventHandlerFunction is passed as the second argument of the .addEventListener() method instead of defining an anonymous function within the method!


DOM Events with JavaScript
Adding Event Handlers
13 min

We looked at registering event handlers using the .addEventListener() method, but there is also another way!

Event Handlers can also be registered by setting an .onevent property on a DOM element (event target). The pattern for registering a specific event is to append an element with .on followed by the lowercased event type name. For instance, if we want to register a click event with this pattern, we would write:

eventTarget.onclick = eventHandlerFunction;

Here, we give the DOM element eventTarget the .onclick property and set its value as the event handler function eventHandlerFunction.

It’s important to know that this .onevent property and .addEventListener() will both register event listeners. With .onevent, it allows for one event handler function to be attached to the event target. However, with the .addEventListener() method , we can add multiple event handler functions. In the later exercises, we’ll be using the .addEventListener() syntax, but we wanted to also introduce the .onevent syntax because both are widely used.

