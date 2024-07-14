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


## July 1st, 2024

Introduction to Form Validation
Client-side Validation: HTML
4 min

The first technique we can use to validate form data is to prevent problematic inputs from being submitted in the first place. This is called client-side validation. The client is the process interacting with the server on behalf of a user—in the case of websites, the web browser is the client. The logic for validating the form is included with the code that displays the form on the user’s device. No interaction with the back-end is required to perform client-side validations.

Since form validation is so common, modern HTML provides some of these validation features built-in. For example, we can use HTML to make parts of a form required and others optional. We can also use HTML to set minimum and maximum values for an input or minimum or maximum lengths for a text input. We can even necessitate that the input match a particular pattern, specified by a regular expression.

If any of the rules laid out in the HTML form validation aren’t followed, the user will not be able to submit their form, and they’ll receive an error message explaining why. With these checks in place, the back-end is less likely to be sent incorrect data. HTML form validation will also benefit the user—the client provides the user immediate feedback, without having to wait for time-consuming communication with the back-end.

Introduction to Form Validation
Back-end Validation
3 min

No matter how complete the front-end validation of a website or application seems, validations must also be completed on the back-end or server-side. Front-end validations are easy to bypass—a malicious user can simply turn off JavaScript on their browser, for example. There’s also the potential for middleman attacks in which data is changed after the request is submitted by a user but before it arrives at the server. As a rule, the back-end should never trust the data it receives.

As the developer, once data is in the back-end, we have complete control over it, luckily. Back-end validation has several advantages:

    It enables us to use validation code often on machines with more computing power.
    It allows us to write validation code that a user can’t see—if malicious users can’t see exactly how we validate the data, it’s much more difficult for them to find ways around it.
    We can validate the information against other data the front-end doesn’t have access to—for example, we can check our database to see if a given username is already in use.

There are two main ways to validate inputs on the server-side. The first takes place while the user is still inputting data into the form on the front-end. We can make asynchronous requests to the server with pieces of their data and send feedback directly to the user before they’ve submitted. This is slower than front-end validation and can be a design challenge from a user-experience perspective.

The second is once the form has been submitted. Back-end form validation is our application’s last defense against problematic data, and it’s essential to verify the validity and safety of data before adding it to a database. This is also an opportunity to “sanitize” the data: in order for our database to be useful, it’s important that all data within it is formatted consistently. This means that while we may want to be flexible about the formatting we require from a user, we likely want to transform inputs into a strict format before entering them in the database.



HTML Forms
Text Input
8 min

If we want to create an input field in our <form>, we’ll need the help of the <input> element.

The <input> element has a type attribute which determines how it renders on the web page and what kind of data it can accept.

The first value for the type attribute we’re going to explore is "text". When we create an <input> element with type="text", it renders a text field that users can type into. Note that the default value of type is "text". It’s also important that we include a name attribute for the <input> — without the name attribute, information in the <input> won’t be sent when the <form> is submitted. We’ll explain more about submissions and the submit button in a later exercise. For now, let’s examine the following code that produces a text input field:

<form action="/example.html" method="POST">
  <input type="text" name="first-text-field">
</form>

Here’s a screen shot of how the rendered form looks like on a web page for the Chrome browser (different browsers have different default rendering). When initially loaded, it will be an empty box:
rendered empty text field from input element type='text'

After users type into the <input> element, the value of the value attribute becomes what is typed into the text field. The value of the value attribute is paired with the value of the name attribute and sent as text when the form is submitted. For instance, if a user typed in “important details” in the text field created by our <input> element:
rendered filled text field which reads 'important details'

When the form is submitted, the text: "first-text-field=important details" is sent to /example.html because the value of the name attribute is "first-text-field" and the value of value is "important details".

We could also assign a default value for the value attribute so that users have a pre-filled text field when they first see the rendered form like so:

<form action="/example.html" method="POST">
  <input type="text" name="first-text-field" value="already pre-filled">
</form>

Which renders:
pre-filled text box due to assigned `value` attribute

Time to put this knowledge into practice!


HTML Forms
Adding a Label
6 min

In the previous exercise we created an <input> element but we didn’t include anything to explain what the <input> is used for. For a user to properly identify an <input> we use the appropriately named <label> element.

The <label> element has an opening and closing tag and displays text that is written between the opening and closing tags. To associate a <label> and an <input>, the <input> needs an id attribute. We then assign the for attribute of the <label> element with the value of the id attribute of <input>, like so:

<form action="/example.html" method="POST">
  <label for="meal">What do you want to eat?</label>
  <br>
  <input type="text" name="food" id="meal">
</form>

The code above renders:
rendered form with labeled text field

Look, now users know what the <input> element is for! Another benefit for using the <label> element is when this element is clicked, the corresponding <input> is highlighted/selected.

Let’s see the <label> element in action!

HTML Forms
Number Input
6 min

We’ve now gone over two type attributes for <input> related to text. But, we might want our users to type in a number — in which case we can set the type attribute to… (you guessed it)… "number"!

By setting type="number" for an <input> we can restrict what users type into the input field to just numbers (and a few special characters like -, +, and .). We can also provide a step attribute which creates arrows inside the input field to increase or decrease by the value of the step attribute. Below is the code needed to render an input field for numbers:

<form>
  <label for="years"> Years of experience: </label>
  <input id="years" name="years" type="number" step="1">
</form>

Which renders:
rendered number input field with arrows to the right hand side of the field

Now it’s time to apply this knowledge.


HTML Forms
Range Input
6 min

Using an <input type="number"> is great if we want to allow users to type in any number of their choosing. But, if we wanted to limit what numbers our users could type we might consider using a different type value. Another option we could use is setting type to "range" which creates a slider.

To set the minimum and maximum values of the slider we assign values to the min and max attribute of the <input>. We could also control how smooth and fluid the slider works by assigning the step attribute a value. Smaller step values will make the slider move more fluidly, whereas larger step values will make the slider move more noticeably. Take a look at the code to create a slider:

<form>
  <label for="volume"> Volume Control</label>
  <input id="volume" name="volume" type="range" min="0" max="100" step="1">
</form>

The code above renders: rendered slider for volume control

In the example above, every time the slider moves by one, the value of the <input>‘s value attribute changes.


HTML Forms
Checkbox Input
11 min

So far the types of inputs we’ve allowed were all single choices. But, what if we presented multiple options to users and allowed them to select any number of options? Sounds like we could use checkboxes! In a <form> we would use the <input> element and set type="checkbox". Examine the code used to create multiple checkboxes:

<form>
  <p>Choose your pizza toppings:</p>
  <label for="cheese">Extra cheese</label>
  <input id="cheese" name="topping" type="checkbox" value="cheese">
  <br>
  <label for="pepperoni">Pepperoni</label>
  <input id="pepperoni" name="topping" type="checkbox" value="pepperoni">
  <br>
  <label for="anchovy">Anchovy</label>
  <input id="anchovy" name="topping" type="checkbox" value="anchovy">
</form>

Which renders: HTML form asking user to select pizza toppings and three topping selections as checkboxes

Notice in the example provided:

    there are assigned values to the value attribute of the checkboxes. These values are not visible on the form itself, that’s why it is important that we use an associated <label> to identify the checkbox.
    each <input> has the same value for the name attribute. Using the same name for each checkbox groups the <input>s together. However, each <input> has a unique id to pair with a <label>.

Alright, time to use checkboxes in our code!



HTML Forms
Radio Button Input
6 min

Checkboxes work well if we want to present users with multiple options and let them choose one or more of the options. However, there are cases where we want to present multiple options and only allow for one selection — like asking users if they agree or disagree with the terms and conditions. Let’s look over the code used to create radio buttons:

<form>
  <p>What is sum of 1 + 1?</p>
  <input type="radio" id="two" name="answer" value="2">
  <label for="two">2</label>
  <br>
  <input type="radio" id="eleven" name="answer" value="11">
  <label for="eleven">11</label>
</form>

Which renders:
rendered form containing radio buttons

Notice from the code snippet, radio buttons (like checkboxes) do not display their value. We have an associated <label> to represent the value of the radio button. To group radio buttons together, we assign them the same name and only one radio button from that group can be selected.

Let’s see this in action by creating our own radio buttons.


HTML Forms
Dropdown list
8 min

Radio buttons are great if we want our users to pick one option out of a few visible options, but imagine if we have a whole list of options! This situation could quickly lead to a lot of radio buttons to keep track of.

An alternative solution is to use a dropdown list to allow our users to choose one option from an organized list. Here’s the code to create a dropdown menu:

<form>
  <label for="lunch">What's for lunch?</label>
  <select id="lunch" name="lunch">
    <option value="pizza">Pizza</option>
    <option value="curry">Curry</option>
    <option value="salad">Salad</option>
    <option value="ramen">Ramen</option>
    <option value="tacos">Tacos</option>
  </select>
</form>

Which renders: rendered dropdown list with the first option showing

And if we click on the field containing the first option, the list is revealed: rendered dropdown list with the all options showing

Notice in the code that we’re using the element <select> to create the dropdown list. To populate the dropdown list, we add multiple <option> elements, each with a value attribute. By default, only one of these options can be selected.

The text rendered is the text included between the opening and closing <option> tags. However, it is the value of the value attribute that is used in <form> submission (notice the difference in the text and value capitalization). When the <form> is submitted, the information from this input field will be sent using the name of the <select> and the value of the chosen <option>. For instance, if a user selected Pizza from the dropdown list, the information would be sent as "lunch=pizza".



HTML Forms
Datalist Input
7 min

Even if we have an organized dropdown list, if the list has a lot of options, it could be tedious for users to scroll through the entire list to locate one option. That’s where using the <datalist> element comes in handy.

The <datalist> is used with an <input type="text"> element. The <input> creates a text field that users can type into and filter options from the <datalist>. Let’s go over a concrete example:

<form>
  <label for="city">Ideal city to visit?</label>
  <input type="text" list="cities" id="city" name="city">

  <datalist id="cities">
    <option value="New York City"></option>
    <option value="Tokyo"></option>
    <option value="Barcelona"></option>
    <option value="Mexico City"></option>
    <option value="Melbourne"></option>
    <option value="Other"></option>  
  </datalist>
</form>

Notice, in the code above, we have an <input> that has a list attribute. The <input> is associated to the <datalist> via the <input>‘s list attribute and the id of the <datalist>.

From the code provided, the following form is rendered: input field with a label 'Ideal city to visit?'

And when field is selected: clicking on the input field reveals a dropdown list

While <select> and <datalist> share some similarities, there are some major differences. In the associated <input> element, users can type in the input field to search for a particular option. If none of the <option>s match, the user can still use what they typed in. When the form is submitted, the value of the <input>‘s name and the value of the option selected, or what the user typed in, is sent as a pair.

Now it’s time to make a <datalist> of our own!


HTML Forms
Textarea element
6 min

An <input> element with type="text" creates a single row input field for users to type in information. However, there are cases where users need to write in more information, like a blog post. In such cases, instead of using an <input>, we could use <textarea>.

The <textarea> element is used to create a bigger text field for users to write more text. We can add the attributes rows and cols to determine the amount of rows and columns for the <textarea>. Take a look:

<form>
  <label for="blog">New Blog Post: </label>
  <br>
  <textarea id="blog" name="blog" rows="5" cols="30">
  </textarea>
</form>

In the code above, an empty <textarea> that is 5 rows by 30 columns is rendered to the page like so:
rendered empty textarea element

If we wanted an even bigger text field, we could click and drag on the bottom right corner to expand it.

When we submit the form, the value of <textarea> is the text written inside the box. If we want to add a default value to <textarea> we would include it within the opening and closing tags like so:

<textarea>Adding default text</textarea>

This code will render a <textarea> that contains pre-filled text: “Adding default text”.

But don’t just take our word for it, let’s test it out!


Submit Form
3 min

Remember, the purpose of a form is to collect information that will be submitted. That’s the role of the submit button — users click on it when they are finished with filling out information in the <form> and they’re ready to send it off. Now that we’ve gone over how to create various input elements, let’s now go over how to create a submit button!

To make a submit button in a <form>, we’re going to use the reliable <input> element and set the type to "submit". For instance:

<form>
  <input type="submit" value="Send">
</form>

Which renders:
rendered submit button

Notice in the code snippet that the value assigned to the <input> shows up as text on the submit button. If there isn’t a value attribute, the default text, Submit shows up on the button.

Let’s now add this element to make our <form>s complete!


Form Validation
Requiring an Input
4 min

Sometimes we have fields in our <form>s which are not optional, i.e. there must be information provided before we can submit it. To enforce this rule, we can add the required attribute to an <input> element.

Take for example:

<form action="/example.html" method="POST">
  <label for="allergies">Do you have any dietary restrictions?</label>
  <br>
  <input id="allergies" name="allergies" type="text" required>
  <br>
  <input type="submit" value="Submit">
</form>

This renders a text box, and if we try to submit the <form> without filling it out we get this message:

message pop up prompting user to fill in the field

The styling of the message varies from browser to browser, the picture above depicts the message in a Chrome browser. We’ll also continue to show these messages as they appear in Chrome in later exercises.

Let’s see how it shows up in your browser!


Set a Minimum and Maximum
2 min

Another built-in validation we can use is to assign a minimum or maximum value for a number field, e.g. <input type="number"> and <input type="range">. To set a minimum acceptable value, we use the min attribute and assign a value. On the flip side, to set a maximum acceptable value, we assign the max attribute a value. Let’s see this in code:

<form action="/example.html" method="POST">
  <label for="guests">Enter # of guests:</label>
  <input id="guests" name="guests" type="number" min="1" max="4">
  <input type="submit" value="Submit">
</form>

If a user tries to submit an input that is less than 1 a warning will appear: prompt on a number field for user to input a value greater than or equal to 1

A similar message will appear if a user tries to input a number greater than 4. Let’s now see this action.


Form Validation
Checking Text Length
4 min

In the previous exercise, we were able to use min and max to set acceptable minimum and maximum values in a number field. But what about text fields? There are certainly cases where we wouldn’t want our users typing more than a certain number of characters (think about the character cap for messages on Twitter). We might even want to set a minimum number of characters. Conveniently, there are built-in HTML5 validations for these situations.

To set a minimum number of characters for a text field, we add the minlength attribute and a value to set a minimum value. Similarly, to set the maximum number of characters for a text field, we use the maxlength attribute and set a maximum value. Let’s take a look at these attributes in code:

<form action="/example.html" method="POST">
  <label for="summary">Summarize your feelings in less than 250 characters</label>
  <input id="summary" name="summary" type="text" minlength="5" maxlength="250" required>
  <input type="submit" value="Submit">
</form>

If a user tries to submit the <form> with less than the set minimum, this message appears:

prompt on a number field for user to length the input

And if a user tries to type in more than the maximum allowed number of characters, they don’t get a warning message, but they can’t type it in!

Let’s add this validation to our <form>.


Form Validation
Matching a Pattern
4 min

In addition to checking the length of a text, we could also add a validation to check how the text was provided. For cases when we want user input to follow specific guidelines, we use the pattern attribute and assign it a regular expression, or regex. Regular expressions are a sequence of characters that make up a search pattern. If the input matches the regex, the form can be submitted.

Let’s say we wanted to check for a valid credit card number (a 14 to 16 digit number). We could use the regex: [0-9]{14,16} which checks that the user provided only numbers and that they entered at least 14 digits and at most 16 digits.

To add this to a form:

<form action="/example.html" method="POST">
  <label for="payment">Credit Card Number (no spaces):</label>
  <br>
  <input id="payment" name="payment" type="text" required pattern="[0-9]{14,16}">
  <input type="submit" value="Submit">
</form>

With the pattern in place, users can’t submit the <form> with a number that doesn’t follow the regex. When they try, they’ll see a validation message like so:
message prompting user to follow the requested format

If you want to find out more about Regex, read more at the Docs RegEx entry.

To see it in practice, let’s use the pattern attribute in our HTML!



Accessible Design
Headings Hierarchy
3 min

Heading elements should be used in order and it is considered best practice not to skip heading elements when possible.

Let’s take a look at an example:

<h1>Main Site Header</h1>
<section>
  <h2>Section Header</h2>
</section>
<section>
  <h2>Section Header</h2>
  <h3>Section Sub-Header</h3>
</section>  
<footer>
  <h2>Footer Header</h2>
</footer>

In this example, we have one main site heading. This content uses the <h1> element and is assigned the highest rank as it is the most important. Note that each web page should only contain one <h1> element.

This <h1> is considered the label for the entire document and it should clearly define the purpose of the web page. After that, we use the <h2> element to assign the same level of importance to each sibling section.

This provides our users with a clean and consistent level of hierarchy when viewing our websites and also conforms to today’s web standards by providing a clear content outline.

Let’s apply what you’ve learned about headings to improve the “Creamy Chocolate Cupcakes” site.


Accessible Design
Best Practices
6 min

New web design trends come and go, and many times they are aesthetically appealing, but they are not always the most usable or accessible.

You now know enough principles of accessibility and usability to be able to judge if these trends will create problems for your users. Let’s reason through a few examples.
Text Overlaid on Images

White text overlaid on an image is a popular design trend. However, it doesn’t adhere to standards as the contrast is often too low. Adding a dark transparent overlay on top of the image could increase the contrast and provide better legibility.
Removing Input Labels

Another trend often seen in web design is the removal of labels above input fields, sometimes relying on placeholder text instead to identify the input field.

While this enhances the aesthetic quality of a design in some instances, it can hinder a user’s ability to identify which input they are attempting to fill out. This is particularly true for low vision users because the placeholder text is often light gray and low contrast. This also creates problems for users employing screen readers, because the form’s placeholder text is not always narrated.
Buttons and Links

There has been a trend towards flat and minimal design in recent years. This trend has improved usability in some ways, as it has encouraged designers to remove visual effects that are not contributing to the usability of their site.

However, minimalism can go too far, especially if it obscures how users should navigate the site. Visual contrast is especially important for buttons and links because these are the tools our users employ to navigate. Color alone should not be used to indicate clickability, as this will cause challenges for low vision and color-blind users.

Taking into consideration color choices, contrast, and font legibility will help you evaluate new design trends, and reduce the chance of new designs introducing accessibility barriers.


## July 2, 2024

the alt "" can be left empty for decorative images and things, but shouldn't be left out entirely.



## July 12, 2024 ## 

clip-path can be used to make cool shapes.

perspective on parent div makes for cool effect. could possibly use for garden app. just enter a px value

styling input forms 

input {
  caret-color: red;
}

input:focus {
  outline = solid 1px red;
}


pseudo classes are powerful. can eliminate need for javascript

.class:is(h1, h2, h4) {}
.class:where(h1, h2, h4) {}

.class:has(button) .content {
} will only target .content of .class that has button

input::placeholder {
  color: red;
  }




## July 13th, 2024 ##

Line height Headers => 1.1- 1.3 times the font size. 
            Body => 1.2- 1.6 times the font size.

Letter spacing headers =>  -1% to -3%


line word length = 50 to 75 characters


try to use just 2 font sizes for entire design. Use font-weight and color to impact the style.


recommended way to use background-color is in the BODY tag.

order property on flex-box items real easy.

just assign
order: 1; 
order: 2;
order: etc; 
  on your flex box children.
