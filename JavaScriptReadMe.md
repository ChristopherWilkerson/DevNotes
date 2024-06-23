## June 19th, 2024 
Java script :) 

      Introduction to JavaScript
      Console
      4 min
      
      The console is a panel that displays important messages, like errors, for developers. Much of the work the computer does with our code is invisible to us by default. If we want to see things appear on our screen, we can print, or log, to our console directly.
      
      In JavaScript, the console keyword refers to an object, a collection of data and actions, that we can use in our code. Keywords are words that are built into the JavaScript language, so the computer recognizes them and treats them specially.
      
      One action, or method, that is built into the console object is the .log() method. When we write console.log() what we put inside the parentheses will get printed, or logged, to the console.
      
      It’s going to be very useful for us to print values to the console, so we can see the work that we’re doing.
      
      console.log(5); 


Comments: 

// for single line

/*  
*/

for multi line. 

Introduction to JavaScript
Properties
3 min

When you introduce a new piece of data into a JavaScript program, the browser saves it as an instance of the data type. All data types have access to specific properties that are passed down to each instance. For example, every string instance has a property called length that stores the number of characters in that string. You can retrieve property information by appending the string with a period and the property name:

console.log('Hello'.length); // Prints 5

The . is another operator! We call it the dot operator.

In the example above, the value saved to the length property is retrieved from the instance of the string, 'Hello'. The program prints 5 to the console, because Hello has five characters in it.
Instructions

    Checkpoint 1 Passed

    1.

    Use the .length property to log the number of characters in the following string to the console:

    'Teaching the world how to code'


Introduction to JavaScript
Review
1 min

Let’s take one more glance at the concepts we just learned:

    Data is printed, or logged, to the console, a panel that displays messages, with console.log().
    We can write single-line comments with // and multi-line comments between /* and */.
    There are 7 fundamental data types in JavaScript: strings, numbers, booleans, null, undefined, symbol, and object.
    Numbers are any number without quotes: 23.8879
    Strings are characters wrapped in single or double quotes: 'Sample String'
    The built-in arithmetic operators include +, -, *, /, and %.
    Objects, including instances of data types, can have properties, stored information. The properties are denoted with a . after the name of the object, for example: 'Hello'.length.
    Objects, including instances of data types, can have methods which perform actions. Methods are called by appending the object or instance with a period, the method name, and parentheses. For example: 'hello'.toUpperCase().
    We can access properties and methods by using the ., dot operator.
    Built-in objects, including Math, are collections of methods and properties that JavaScript provides.

Here are a few more resources to add to your toolkit:

    Codecademy Docs: JavaScript
    Codecademy Workspaces: JavaScript

Make sure to bookmark these links so you have them at your disposal.

Variables
The Increment and Decrement Operator
2 min

Other mathematical assignment operators include the increment operator (++) and decrement operator (--).

The increment operator will increase the value of the variable by 1. The decrement operator will decrease the value of the variable by 1. For example:

let a = 10;
a++;
console.log(a); // Output: 11

let b = 20;
b--;
console.log(b); // Output: 19

Variables
String Interpolation
8 min

In the ES6 version of JavaScript, we can insert, or interpolate, variables into strings using template literals. Check out the following example where a template literal is used to log strings together:

const myPet = 'armadillo';
console.log(`I own a pet ${myPet}.`);
// Output: I own a pet armadillo.

Notice that:

    a template literal is wrapped by backticks ` (this key is usually located on the top of your keyboard, left of the 1 key).
    Inside the template literal, you’ll see a placeholder, ${myPet}. The value of myPet is inserted into the template literal.
    When we interpolate `I own a pet ${myPet}.`, the output we print is the string: 'I own a pet armadillo.'

One of the biggest benefits to using template literals is the readability of the code. Using template literals, you can more easily tell what the new string will be. You also don’t have to worry about escaping double quotes or single quotes.


## let myName = "Chris";
let myCity = "Seoul";
console.log(`My name is ${myName}. My favorite city is ${myCity}`)


Variables
Review Variables
2 min

Nice work! This lesson introduced you to variables, a powerful concept you will use in all your future programming endeavors.

Let’s review what we learned:

    Variables hold reusable data in a program and associate it with a name.
    Variables are stored in memory.
    The var keyword is used in pre-ES6 versions of JS.
    let is the preferred way to declare a variable when it can be reassigned, and const is the preferred way to declare a variable with a constant value.
    Variables that have not been initialized store the primitive data type undefined.
    Mathematical assignment operators make it easy to calculate a new value and assign it to the same variable.
    The + operator is used to concatenate strings including string values held in variables.
    In ES6, template literals use backticks ` and ${} to interpolate values into a string.
    The typeof keyword returns the data type (as a string) of a valu


example temperature celsius to fahrenheit

                              let celsius = 32;
                              // temp in celsius
                              let fahrenheit = Math.floor(celsius * (9/5) + 32);
                              // temp in fahrenheit 
                              console.log(`The temperature is ${fahrenheit} degrees Fahrenheit`)

      My Home
Conditional Statements: If Statement
Narrative and Instructions
Learn
Conditional Statements
If Statement
7 min

We often perform a task based on a condition. For example, if the weather is nice today, then we will go outside. If the alarm clock rings, then we’ll shut it off. If we’re tired, then we’ll go to sleep.

In programming, we can also perform a task based on a condition using an if statement:

if (true) {
  console.log('This message will print!'); 
}
// Prints: This message will print!

Notice in the example above, we have an if statement. The if statement is composed of:

    The if keyword followed by a set of parentheses () which is followed by a code block, or block statement, indicated by a set of curly braces {}.
    Inside the parentheses (), a condition is provided that evaluates to true or false.
    If the condition evaluates to true, the code inside the curly braces {} runs, or executes.
    If the condition evaluates to false, the block won’t execute.

Let’s make an if statement.


Conditional Statements
If...Else Statements
4 min

In the previous exercise, we used an if statement that checked a condition to decide whether or not to run a block of code. In many cases, we’ll have code we want to run if our condition evaluates to false.

If we wanted to add some default behavior to the if statement, we can add an else statement to run a block of code when the condition evaluates to false. Take a look at the inclusion of an else statement:

if (false) {
  console.log('The code in this block will not run.');
} else {
  console.log('But the code in this block will!');
}

// Prints: But the code in this block will!

An else statement must be paired with an if statement, and together they are referred to as an if...else statement.

In the example above, the else statement:

    Uses the else keyword following the code block of an if statement.
    Has a code block that is wrapped by a set of curly braces {}.
    The code inside the else statement code block will execute when the if statement’s condition evaluates to false.

if...else statements allow us to automate solutions to yes-or-no questions, also known as binary decisions.


Is equal to: ===
Is not equal to: !==

            let hungerLevel = 7;
            if (hungerLevel > 3) {
              console.log('Time to eat!')
            } else {
              console.log("We can eat later!");
            }

Logical Operators
10 min

Working with conditionals means that we will be using booleans, true or false values. In JavaScript, there are operators that work with boolean values known as logical operators. We can use logical operators to add more sophisticated logic to our conditionals. There are three logical operators:

    the and operator (&&)
    the or operator (||)
    the not operator, otherwise known as the bang operator (!)


Conditional Statements
Truthy and Falsy Assignment
8 min

Truthy and falsy evaluations open a world of short-hand possibilities!

Say you have a website and want to take a user’s username to make a personalized greeting. Sometimes, the user does not have an account, making the username variable falsy. The code below checks if username is defined and assigns a default string if it is not:

let username = '';
let defaultName;

if (username) {
  defaultName = username;
} else {
  defaultName = 'Stranger';
}

console.log(defaultName); // Prints: Stranger

If you combine your knowledge of logical operators you can use a short-hand for the code above. In a boolean condition, JavaScript assigns the truthy value to a variable if you use the || operator in your assignment:

let username = '';
let defaultName = username || 'Stranger';

console.log(defaultName); // Prints: Stranger

Because || or statements check the left-hand condition first, the variable defaultName will be assigned the actual value of username if it is truthy, and it will be assigned the value of 'Stranger' if username is falsy. This concept is also referred to as short-circuit evaluation.


Ternary Operator
10 min

In the spirit of using short-hand syntax, we can use a ternary operator to simplify an if...else statement.

Take a look at the if...else statement example:

let isNightTime = true;

if (isNightTime) {
  console.log('Turn on the lights!');
} else {
  console.log('Turn off the lights!');
}

We can use a ternary operator to perform the same functionality:

isNightTime ? console.log('Turn on the lights!') : console.log('Turn off the lights!');


let isLocked = false;

isLocked ? console.log('You will need a key to open the door.') : console.log('You will not need a key to open the door.');

let isCorrect = true;

isCorrect ? console.log('Correct!') : console.log('Incorrect!');

let favoritePhrase = 'Love That!';

favoritePhrase === 'Love That!' ? console.log('I love that!') : console.log("I don't love that!");



Conditional Statements
The switch keyword
11 min

else if statements are a great tool if we need to check multiple conditions. In programming, we often find ourselves needing to check multiple values and handling each of them differently. For example:

let groceryItem = 'papaya';

if (groceryItem === 'tomato') {
  console.log('Tomatoes are $0.49');
} else if (groceryItem === 'papaya'){
  console.log('Papayas are $1.29');
} else {
  console.log('Invalid item');
}

In the code above, we have a series of conditions checking for a value that matches a groceryItem variable. Our code works fine, but imagine if we needed to check 100 different values! Having to write that many else if statements sounds like a pain!

A switch statement provides an alternative syntax that is easier to read and write. A switch statement looks like this:

let groceryItem = 'papaya';

switch (groceryItem) {
  case 'tomato':
    console.log('Tomatoes are $0.49');
    break;
  case 'lime':
    console.log('Limes are $1.49');
    break;
  case 'papaya':
    console.log('Papayas are $1.29');
    break;
  default:
    console.log('Invalid item');
    break;
}

// Prints 'Papayas are $1.29'

    The switch keyword initiates the statement and is followed by ( ... ), which contains the value that each case will compare. In the example, the value or expression of the switch statement is groceryItem.
    Inside the block, { ... }, there are multiple cases. The case keyword checks if the expression matches the specified value that comes after it. The value following the first case is 'tomato'. If the value of groceryItem equalled 'tomato', that case‘s console.log() would run.
    The value of groceryItem is 'papaya', so the third case runs— Papayas are $1.29 is logged to the console.
    The break keyword tells the computer to exit the block and not execute any more code or check any other cases inside the code block. Note: Without break keywords, the first matching case will run, but so will every subsequent case regardless of whether or not it matches—including the default. This behavior is different from if/else conditional statements that execute only one block of code.
    At the end of each switch statement, there is a default statement. If none of the cases are true, then the code in the default statement will run.



Simple marathon program
            let raceNumber = Math.floor(Math.random() * 1000);
            let runnerEarly = false
            let runnerAge = 33
            if (runnerAge > 18 && runnerEarly) {
              raceNumber += 1000
            }
            if (runnerAge > 18 && runnerEarly) {
              console.log(`You will race at 9:30a. Your race number is ${raceNumber}`)
            } else if (runnerAge > 18 && !runnerEarly) {
              console.log(`You will race at 11:00a. Your race number is ${raceNumber}`)
            } else if (runnerAge < 18) {
              console.log(`You will race at 12:30pm. Your race number is ${raceNumber}`)
            } else {
              console.log("See official before start.")
            }
                              


      Functions
Calling a Function
5 min

As we saw in previous exercises, a function declaration binds a function to an identifier.

However, a function declaration does not ask the code inside the function body to run, it just declares the existence of the function. The code inside a function body runs, or executes, only when the function is called.

To call a function in your code, you type the function name followed by parentheses.
Diagram showing the syntax of invoking a function

This function call executes the function body, or all of the statements between the curly braces in the function declaration. Function execution diagram

We can call the same function as many times as needed.

Let’s practice calling functions in our code.


Functions
Parameters and Arguments
8 min

So far, the functions we’ve created execute a task without an input. However, some functions can take inputs and use the inputs to perform a task. When declaring a function, we can specify its parameters. Parameters allow functions to accept input(s) and perform a task using the input(s). We use parameters as placeholders for information that will be passed to the function when it is called.

Let’s observe how to specify parameters in our function declaration:
JavaScript syntax for declaring a function with parameters

In the diagram above, calculateArea(), computes the area of a rectangle, based on two inputs, width and height. The parameters are specified between the parenthesis as width and height, and inside the function body, they act just like regular variables. width and height act as placeholders for values that will be multiplied together. 



simple rectangular area functin
function area_rect(width, height) {
  console.log(width * height)
}
area_rect(2119, 5123)



**** Functions
Default Parameters
5 min

One of the features added in ES6 is the ability to use default parameters. Default parameters allow parameters to have a predetermined value in case there is no argument passed into the function or if the argument is undefined when called.

Take a look at the code snippet below that uses a default parameter:

function greeting (name = 'stranger') {
  console.log(`Hello, ${name}!`)
}

greeting('Nick') // Output: Hello, Nick!
greeting() // Output: Hello, stranger!

    In the example above, we used the = operator to assign the parameter name a default value of 'stranger'. This is useful to have in case we ever want to include a non-personalized default greeting!

    When the code calls greeting('Nick') the value of the argument is passed in and, 'Nick', will override the default parameter of 'stranger' to log 'Hello, Nick!' to the console.

    When there isn’t an argument passed into greeting(), the default value of 'stranger' is used, and 'Hello, stranger!' is logged to the console.

By using a default parameter, we account for situations when an argument isn’t passed into a function that is expecting an argument. 


## June 20th, 2024

Functions
Function Expressions
13 min

Another way to define a function is to use a function expression. To define a function inside an expression, we can use the function keyword. In a function expression, the function name is usually omitted. A function with no name is called an anonymous function. A function expression is often stored in a variable in order to refer to it.

Consider the following function expression:
defining a function expression

To declare a function expression:

    Declare a variable to make the variable’s name be the name, or identifier, of your function. Since the release of ES6, it is common practice to use const as the keyword to declare the variable.

    Assign as that variable’s value an anonymous function created by using the function keyword followed by a set of parentheses with possible parameters. Then a set of curly braces that contain the function body.

To invoke a function expression, write the name of the variable in which the function is stored followed by parentheses enclosing any arguments being passed into the function.

variableName(argument1, argument2)

Unlike function declarations, function expressions are not hoisted so they cannot be called before they are defined.

Let’s define a new function using a function expression.


Functions
Arrow Functions
3 min

ES6 introduced arrow function syntax, a shorter way to write functions by using the special “fat arrow” () => notation.

Arrow functions remove the need to type out the keyword function every time you need to create a function. Instead, you first include the parameters inside the ( ) and then add an arrow => that points to the function body surrounded in { } like this:

const rectangleArea = (width, height) => {
  let area = width * height;
  return area;
};

It’s important to be familiar with the multiple ways of writing functions because you will come across each of these when reading other JavaScript code.


Functions
Concise Body Arrow Functions
5 min

JavaScript also provides several ways to refactor arrow function syntax. The most condensed form of the function is known as concise body. We’ll explore a few of these techniques below:

    Functions that take only a single parameter do not need that parameter to be enclosed in parentheses. However, if a function takes zero or multiple parameters, parentheses are required.
    showcasing how arrow functions parameters differ for different amounts of parameters

    A function body composed of a single-line block does not need curly braces. Without the curly braces, whatever that line evaluates will be automatically returned. The contents of the block should immediately follow the arrow => and the return keyword can be removed. This is referred to as implicit return.

comparing single line and multiline arrow functions

So if we have a function:

const squareNum = (num) => {
  return num * num;
};

We can refactor the function to:

const squareNum = num => num * num;

Notice the following changes:

    The parentheses around num have been removed, since it has a single parameter.
    The curly braces { } have been removed since the function consists of a single-line block.
    The return keyword has been removed since the function consists of a single-line block.



My Home
Scope: Review: Scope
Narrative and Instructions
Learn
Scope
Review: Scope
1 min

In this lesson, you learned about scope and how it impacts the accessibility of different variables.

Let’s review the following terms:

    Scope refers to where variables can be accessed throughout the program, and is determined by where and how they are declared.
    Blocks are statements that exist within curly braces {}.
    Global scope refers to the context within which variables are accessible to every part of the program.
    Global variables are variables that exist within global scope.
    Block scope refers to the context within which variables are accessible only within the block they are defined.
    Local variables are variables that exist within block scope.
    Global namespace is the space in our code that contains globally scoped information.
    Scope pollution is when too many variables exist in a namespace or variable names are reused.

As you continue your coding journey, remember to use best practices when declaring your variables! Scoping your variables tightly will ensure that your code has clean, organized, and modular logic.



grid-template-column: repeat(auto-fit, minmax(300px, 1fr)); 

on flex-children
flex: 1;



## June 21, 2024

Command + Opt + K to run javascript console in browser


## Node.js

Note the following syntax rules for JSON:

    The curly braces, {..}, hold objects.
    The square brackets, [..], hold arrays.
    Data is stored in name-value pairs separated by a colon, :.
    Every name-value pair is separated from another pair by a comma, ,. Similarly, every item in an array is delimited by a comma as well. Trailing commas are forbidden.
    JSON property names must be in double-quoted (" ") text even though JavaScript names do not hold by this stringency.


What Is JSON?

A brief guide to understanding JSON and its use cases.
Introduction

In a world inundated with data, it is becoming more important to know how to work with a variety of data. As programmers, we need to be able to transfer our populated data structures from any language we choose to a format that is recognizable and readable by other languages and platforms. Fortunately for us, there exists such a data-exchange format.
What is JSON?

JSON, or JavaScript Object Notation, is a popular, language-independent, standard format for storing and exchanging data. Adopted by ECMA International, an industry association founded in 1961 to standardize information and communication systems, JSON has become the de facto standard that facilitates storing and sending data between all programming languages.
Common Uses of JSON

JSON is heavily used to facilitate data transfer in web applications between a client, such as a web browser, and a server. A typical example where such data transfer occurs is when you fill out a web form. The form data is converted from HTML to JavaScript objects to JSON objects and sent to a remote web server for processing. These transactions could be as simple as entering a search engine query to a multi-page job application.

When companies make their data public for other applications, like Spotify sharing its music library or Google sharing its map data, the information is formatted in JSON. This way, any application, regardless of language, can collect and parse the data.

Some of the popular web APIs that utilize JSON in data exchanges are:

    Google Maps
    Google Auth 2.0 Authentication
    Facebook Social Graph API
    Spotify Music Web API
    LinkedIn Profile API

JSON Syntax

Since JSON is derived from the JavaScript programming language, its appearance is similar to that of JavaScript objects.

A sample JSON object is represented as follows:

{
  "student": {
    "name": "Rumaisa Mahoney",
    "age": 30,
    "fullTime": true,
    "languages": [ "JavaScript", "HTML", "CSS" ],
    "GPA": 3.9,
    "favoriteSubject": null
  }
}

Note the following syntax rules for JSON:

    The curly braces, {..}, hold objects.
    The square brackets, [..], hold arrays.
    Data is stored in name-value pairs separated by a colon, :.
    Every name-value pair is separated from another pair by a comma, ,. Similarly, every item in an array is delimited by a comma as well. Trailing commas are forbidden.
    JSON property names must be in double-quoted (" ") text even though JavaScript names do not hold by this stringency.

JSON Data Types

A JSON data type must be one of the following:

    string (double-quoted)
    number (integer or floating point)
    object (name-value pair)
    array (comma-delimited)
    boolean (true or false)
    null


By default, you indicate the input is ready for eval when you hit enter. If you’d like to type multiple lines and then have them evaluated at once, you can type .editor while in the REPL. Once in “editor” mode, you can type control + d when you’re ready for the input to be evaluated. Each session of the REPL has a single shared memory; you can access any variables or functions you define until you exit the REPL.


Introduction to Node.js
Core Modules
6 min

Modularity is a software design technique where one program has distinct parts, each providing a single piece of the overall functionality. These separate modules come together to build a cohesive whole. Modularity is essential for creating scalable programs which incorporate libraries and frameworks and separate the program’s concerns into manageable chunks. Essentially, a module is a collection of code located in a file. Instead of having an entire program located in a single file, code is organized into separate files based on the concerns they address. These files can then be included in other files by using the require() function.

To save developers from reinventing the wheel each time, Node.js has several built-in modules to perform common tasks efficiently. These are known as the core modules. The core modules are defined within Node.js’s source code and are located in the lib/ folder. Core modules can be required by passing a string with the name of the module into the require() function:

// Require in the 'events' core module:
const events = require('events');

The example above shows how the events module is required into a file and stored in an events variable. Understanding the specifics of this module isn’t necessary at this point, but the events module is a Node.js core module that provides key functions for working with, well… events. You’ll learn more about it in a later lesson. 

Once in the REPL, a complete list of core modules can be accessed by typing the command:

require('module').builtinModules

As you can see, there are many modules already built into Node.js and ready to be utilized! In the next few exercises, we’ll explore some of the more useful ones in further detail.

## June 22nd, 2024

Introduction to Node.js
The OS Module
11 min

When developing or debugging an app, it can be helpful to have information about the computer, operating system, and network on which the program is running. Before Node, this information could not be retrieved using JavaScript due to the language being confined to the browser. However, Node.js is a JavaScript runtime, which means it can execute code outside of the browser, and we’re able to get access to much of this information through the os core module.

Unlike process and console, the os module is not global and needs to be included into the file in order to gain access to its methods. You can include the os module into your file by typing:

const os = require('os');

With the os module saved to the os variable, you can call methods like:

    os.type() — to return the computer’s operating system.
    os.arch() — to return the operating system CPU architecture.
    os.networkInterfaces() — to return information about the network interfaces of the computer, such as IP and MAC address.
    os.homedir() — to return the current user’s home directory.
    os.hostname() — to return the hostname of the operating system.
    os.uptime() — to return the system uptime, in seconds.

Let’s take a look at an example:

const os = require('os');

const local = {  
  'Home Directory': os.homedir(),    
  'Operating System': os.type(),
  'Last Reboot': os.uptime()
}

In the above example code, we first require the os module and store it in a variable, os. Below that, we have an object, local, that will hold some information about the user’s computer: the name of the home directory, the type of operating system, and the time since the computer was last rebooted.

  {
    'Home Directory': '/Users/luca',
    'Operating System': 'Darwin',
    'Time since reboot': 86997
  }

When we run the program, the local object stores all the requested information:

    the user’s home directory — '/Users/luca',
    the operating system — 'Darwin' (Darwin is the underlying operating system of macOS.),
    and the time since the computer was last rebooted — 86997 seconds.
Introduction to Node.js
The Util Module
22 min

Developers sometimes classify outlier functions used to maintain code and debug certain aspects of a program’s functionality as utility functions. Utility functions don’t necessarily create new functionality in a program, but you can think of them as internal tools used to maintain and debug your code. The Node.js util core module contains methods specifically designed for these purposes. The util module can be required into the file using:

const util = require('util');

Once required, you have access to many useful objects and methods within the util module. One important object is types, which provides methods for runtime type checking in Node.

const util = require('util');

const today = new Date();
const earthDay = 'April 22, 2022';

console.log(util.types.isDate(today));
console.log(util.types.isDate(earthDay));

In the above example, we first require in the util module. Next, we declare two variables: today stores today’s date as an instance of the Date object, and earthDay stores the date of Earth Day as a string. We then log the results of type checking each variable using util.types.isDate(). The types.isDate() method checks for Date objects and returns a boolean value, giving us:

true
false

Since today is a Date object, it returns true, and since earthDay is a string, it returns false!

Another important util method is .promisify(), which turns callback functions into promises. As you know, asynchronous programming is essential to Node.js. In the beginning, this asynchrony was achieved using error-first callback functions, which are still very prevalent in the Node ecosystem today. But since promises are often preferred over callbacks and especially nested callbacks, Node offers a way to turn these into promises. Let’s take a look:

function getUser (id, callback) {
  return setTimeout(() => {
    if (id === 5) {
      callback(null, { nickname: 'Teddy' })
    } else {
      callback(new Error('User not found'))
    }
  }, 1000)
}

function callback (error, user) {
  if (error) {
    console.error(error.message)
    process.exit(1)
  }

  console.log(`User found! Their nickname is: ${user.nickname}`)
}

getUser(1, callback) // -> `User not found`
getUser(5, callback) // -> `User found! Their nickname is: Teddy`

Here we have a function that queries a database for a specified user ID. getUser methods are very common in back-end applications, and most will also support error-first callbacks. Since a database query typically takes longer to run than other operations, we simulate the query with a setTimeout() method that executes a callback function after 1000 milliseconds (or 1 second). If the user with the specified ID is found, the callback function is executed with null passed in as the argument for the error parameter, and an object containing the returned user information is passed in as an argument for the user parameter. If the user is not found, the callback function is executed, passing in a new Error as the argument for the error parameter. A second argument for user is not necessary since the function will end in the case of an error.

This way of handling this function may seem a bit convoluted these days, but with .promisify(), we can easily change it into a modern, cleaner, and more maintainable version of itself:

const getUserPromise = util.promisify(getUser);

getUserPromise(id)
  .then((user) => {
      console.log(`User found! Their nickname is: ${user.nickname}`);
  })
  .catch((error) => {
      console.log('User not found', error);
  });

getUser(1) // -> `User not found`
getUser(5) // -> `User found! Their nickname is: Teddy`

We declare a getUserPromise variable that stores the getUser method turned into a promise using the .promisify() method. With that in place, we’re able to use getUserPromise with .then() and .catch() methods (or we could also use the async...await syntax here) to resolve the promise returned or catch any errors.

Now, this is an extremely simplified example, but it’s helpful to recognize how to use this important tool when you start working with more complex callback functions


## Douglas Crockford JavaScript video notes
## if dealing with money : javascript bad with some arithmetic functions. .1 + .2 = .30000004
need to multiple by 100 (or 1000 or whatever) to deal with integers, then scale it back

sitting in a beach house on the east coast, learning code on a saturday.

in for statements, make conditional if statement to avoid for looping thru object container heirachy. 
when using parse.int always use a radix.




only functions have scope 
variables do not have scope. 

if creating something with more than a few variables, step back and consider refactoring them as a single object. 



