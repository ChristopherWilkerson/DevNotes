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


DOM Events with JavaScript
Removing Event Handlers
7 min

The .removeEventListener() method is used to reverse the .addEventListener() method. This method stops the event target from “listening” for an event to fire when it no longer needs to. .removeEventListener() also takes two arguments:

    The event type as a string
    The event handler function

Check out the syntax of a .removeEventListener() method with a click event:

eventTarget.removeEventListener('click', eventHandlerFunction);

Because there can be multiple event handler functions associated with a particular event, .removeEventListener() needs both the exact event type name and the name of the event handler you want to remove. If .addEventListener() was provided an anonymous function, then that event listener cannot be removed.


DOM Events with JavaScript
Event Object Properties
14 min

JavaScript stores events as Event objects with their related data and functionalities as properties and methods. When an event is triggered, the event object can be passed as an argument to the event handler function.

function eventHandlerFunction(event){
   console.log(event.timeStamp);
}

eventTarget.addEventListener('click', eventHandlerFunction);

In the example above, when the 'click' event is triggered on the eventTarget, the eventHandlerFunction receives event, the Event object, which has information related to the 'click' event. Then, we log the time it took for the event to be triggered since the document was loaded by accessing the .timeStamp property of the event object.

There are pre-determined properties associated with event objects. You can call these properties to see information about the event, for example:

    the .target property to reference the element that the event is registered to.
    the .type property to access the name of the event.
    the .timeStamp property to access the number of milliseconds that passed since the document loaded and the event was triggered.



DOM Events with JavaScript
Mouse Events
18 min

When you use a mouse device on a website, mouse events fire. You’ve seen the click and wheel events, but, there are even more mouse events to explore!

The mousedown event is fired when the user presses a mouse button down. This is different from a click event because mousedown doesn’t need the mouse button to be released to fire.
Mouse Down Event Image

The mouseup event is fired when the user releases the mouse button. This is different from the click and mousedown events because mouseup doesn’t depend on the mouse button being pressed down to fire.
Mouse Up Event Image

The mouseover event is fired when the mouse enters the content of an element.
Mouse Over Event Image

The mouseout event is fired when the mouse leaves an element.
Mouse Out Event Image
Instructions

    Checkpoint 1 Passed

    1.

    In this exercise, you’ll modify the list elements using mouse events. You can use the reset element that is already programmed to set the other list element back to their default styles.

    First, create a function called increaseWidth() that changes the .width of itemOne to a size of '401px' or greater.

Checkpoint 2 Passed

2.

Now, create an event handler for itemOne that will trigger the increaseWidth() function when the mouse hovers on it.
Checkpoint 3 Passed

3.

Next, create a function called changeBackground() that changes the .backgroundColor of itemTwo.
Checkpoint 4 Passed

4.

Let’s use the changeBackground() function we just created as an event handler for itemTwo that will be triggered when the mouse is released over the element!
Checkpoint 5 Passed

5.

Now, create a function called changeText() that changes the text of itemThree to 'The mouse has left the element'.
Checkpoint 6 Passed

6.

Create an event handler for itemThree that will fire changeText() function when the mouse leaves the element.
Checkpoint 7 Passed

7.

Finally, let’s create a function called showItem() that makes the itemFive element appear by changing the .display style property to 'block'.
Checkpoint 8 Passed

8.

Now, create an event handler for itemFour that triggers the showItem() function when the mouse is pressed down on the element.




DOM Events with JavaScript
Keyboard Events
9 min

Other popular types of events are keyboard events! keyboard events are triggered by user interaction with keyboard keys in the browser.

The keydown event is fired while a user presses a key down. Key Down Event Image

The keyup event is fired while a user releases a key. Key Up Event Image

The keypress event is fired when a user presses a key down and releases it. This is different from using keydown and keyup events together, because those are two complete events and keypress is one complete event. Key P ress Event Image

Keyboard events have unique properties assigned to their event objects like the .key property that stores the values of the key pressed by the user. You can program the event handler function to react to a specific key, or react to any interaction with the keyboard




