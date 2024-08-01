## June 19th, 2024 
Java script :) 

      Introduction to JavaScript
      Console
      4 mins
      
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


Array :

myArray = ['a', 'b', 'c', 'd']
delete myArray[1];  => myArray = ['a', undefined, 'c', 'd']

leaves a hole

if want to remove hole in array, have to use splice.
myArray.splice(1, 1);  => myArray = ['a','c', 'd']



## When to use objects and when to use arrays

use objects when the names are arbitrary strings

use arrays when the names are sequential integers

don't get confused by associative arrays

constructor form new functionObject(arguments)


***Don't use eval or new function function

don't use new String () or new Number() or new Boolean()

Arrays 

Arrays
Update Elements
3 min

In the previous exercise, you learned how to access elements inside an array or a string by using an index. Once you have access to an element in an array, you can update its value.

let seasons = ['Winter', 'Spring', 'Summer', 'Fall'];

seasons[3] = 'Autumn';
console.log(seasons); 
//Output: ['Winter', 'Spring', 'Summer', 'Autumn']

In the example above, the seasons array contained the names of the four seasons.

However, we decided that we preferred to say 'Autumn' instead of 'Fall'.

The line, seasons[3] = 'Autumn'; tells our program to change the item at index 3 of the seasons array to be 'Autumn' instead of what is already there.


## June 23rd, 2024

Loops
The For Loop
6 min

Instead of writing out the same code over and over, loops allow us to tell computers to repeat a given block of code on its own. One way to give computers these instructions is with a for loop.

The typical for loop includes an iterator variable that usually appears in all three expressions. The iterator variable is initialized, checked against the stopping condition, and assigned a new value on each loop iteration. Iterator variables can have any name, but it’s best practice to use a descriptive variable name.

A for loop contains three expressions separated by ; inside the parentheses:

    an initialization starts the loop and can also be used to declare the iterator variable.
    a stopping condition is the condition that the iterator variable is evaluated against— if the condition evaluates to true the code block will run, and if it evaluates to false the code will stop.
    an iteration statement is used to update the iterator variable on each loop.

The for loop syntax looks like this:

for (let counter = 0; counter < 4; counter++) {
  console.log(counter);
}

In this example, the output would be the following:

0
1
2
3

Let’s break down the example:

    The initialization is let counter = 0, so the loop will start counting at 0.
    The stopping condition is counter < 4, meaning the loop will run as long as the iterator variable, counter, is less than 4.
    The iteration statement is counter++. This means after each loop, the value of counter will increase by 1. For the first iteration counter will equal 0, for the second iteration counter will equal 1, and so on.
    The code block is inside of the curly braces, console.log(counter), will execute until the condition evaluates to false. The condition will be false when counter is greater than or equal to 4 — the point that the condition becomes false is sometimes called the stop condition.

This for loop makes it possible to write 0, 1, 2, and 3 programmatically.

iterate through an array simple

                  const vacationSpots = ['Seoul', 'Scotland', 'Vancouver'];

                  // Write your code below
                  for (let i = 0; i < vacationSpots.length; i++){
                    console.log(`I would love to visit ${vacationSpots[i]}`);
                        }

Nested loop example to compare arrays with same values

                        const bobsFollowers = ["Mike", "Duncan", "Lewis", "Trae"];
                        const tinasFollowers = ["Mike", "Leslie", "Ellum", "MiYoung"];
                        mutualFollowers = [];
                        for (let i = 0; i < bobsFollowers.length; i++) {
                            for (let j = 0; j < tinasFollowers.length; j++) {
                                if (bobsFollowers[i] === tinasFollowers[j]) {
                                    mutualFollowers.push(tinasFollowers[j]);
                                }
                            }
                        }
                        console.log(mutualFollowers);

                        returns "Mike"

Loops
The While Loop
12 min

You’re doing great! We’re going to teach you about a different type of loop: the while loop. To start, let’s convert a for loop into a while loop:

// A for loop that prints 1, 2, and 3
for (let counterOne = 1; counterOne < 4; counterOne++){
  console.log(counterOne);
}

// A while loop that prints 1, 2, and 3
let counterTwo = 1;
while (counterTwo < 4) {
  console.log(counterTwo);
  counterTwo++;
}

Let’s break down what’s happening with our while loop syntax:

    The counterTwo variable is declared before the loop. We can access it inside our while loop since it’s in the global scope.
    We start our loop with the keyword while followed by our stopping condition, or test condition. This will be evaluated before each round of the loop. While the condition evaluates to true, the block will continue to run. Once it evaluates to false the loop will stop.
    Next, we have our loop’s code block which prints counterTwo to the console and increments counterTwo.

What would happen if we didn’t increment counterTwo inside our block? If we didn’t include this, counterTwo would always have its initial value, 1. That would mean the testing condition counterTwo < 4 would always evaluate to true and our loop would never stop running! Remember, this is called an infinite loop and it’s something we always want to avoid. Infinite loops can take up all of your computer’s processing power potentially freezing your computer.

So you may be wondering when to use a while loop! The syntax of a while loop is ideal when we don’t know in advance how many times the loop should run. Think of eating like a while loop: when you start taking bites, you don’t know the exact number you’ll need to become full. Rather you’ll eat while you’re hungry. In situations when we want a loop to execute an undetermined number of times, while loops are the best choice.



Loops
Do...While Statements
11 min

In some cases, you want a piece of code to run at least once and then loop based on a specific condition after its initial run. This is where the do...while statement comes in.

A do...while statement says to do a task once and then keep doing it until a specified condition is no longer met. The syntax for a do...while statement looks like this:

let countString = '';
let i = 0;

do {
  countString = countString + i;
  i++;
} while (i < 5);

console.log(countString);

In this example, the code block makes changes to the countString variable by appending the string form of the i variable to it. First, the code block after the do keyword is executed once. Then the condition is evaluated. If the condition evaluates to true, the block will execute again. The looping stops when the condition evaluates to false.

Note that the while and do...while loop are different! Unlike the while loop, do...while will run at least once whether or not the condition evaluates to true.

const firstMessage = 'I will print!';
const secondMessage = 'I will not print!'; 

// A do while with a stopping condition that evaluates to false
do {
 console.log(firstMessage)
} while (true === false);

// A while loop with a stopping condition that evaluates to false
while (true === false){
  console.log(secondMessage)
};


using break and array value 
                  const rapperArray = ["Lil' Kim", "Jay-Z", "Notorious B.I.G.", "Tupac"];
                  
                  // Write your code below
                  for (let i = 0; i < rapperArray.length; i++) {
                      console.log(rapperArray[i]);
                      if (rapperArray[i] === 'Notorious B.I.G.') {
                        break;
                      }
                  }
                  console.log("And if you don't know, now you know.");


for loop vs for…of loop

Here is an example of iterating over each element in an array using a traditional for loop with an index variable:

const hobbies = ['singing', 'eating', 'quidditch', 'writing'];
 
for (let i = 0; i < hobbies.length; i++) {
  console.log(`I enjoy ${hobbies[i]}.`);
}


And here is an example of iterating through the same array using a for...of loop:

const hobbies = ['singing', 'eating', 'quidditch', 'writing'];
 
for (const hobby of hobbies) {
  console.log(`I enjoy ${hobby}.`);
}

Iterating Through a String

The for...of can also be used to iterate over strings. Here is an example:

const username = 'joe';
 
for (const char of username) {
  console.log(char);
}

Objects
Accessing Properties
4 min

There are two ways we can access an object’s property. Let’s explore the first way— dot notation, ..

You’ve used dot notation to access the properties and methods of built-in objects and data instances:

'hello'.length; // Returns 5

With property dot notation, we write the object’s name, followed by the dot operator and then the property name (key):

let spaceship = {
  homePlanet: 'Earth',
  color: 'silver'
};
spaceship.homePlanet; // Returns 'Earth',
spaceship.color; // Returns 'silver',

If we try to access a property that does not exist on that object, undefined will be returned.

spaceship.favoriteIcecream; // Returns undefined

Let’s get some more practice using dot notation on an object!

Objects
Property Assignment
8 min

Once we’ve defined an object, we’re not stuck with all the properties we wrote. Objects are mutable meaning we can update them after we create them!

We can use either dot notation, ., or bracket notation, [], and the assignment operator, = to add new key-value pairs to an object or change an existing property.

diagram showing how an object followed by brackets ([]) with the property name as a string can be reassigned to a new value. This same idea applies for accessing a property using dot notation which has the object name, followed by a dot and the name of the property

One of two things can happen with property assignment:

    If the property already exists on the object, whatever value it held before will be replaced with the newly assigned value.
    If there was no property with that name, a new property will be added to the object.

It’s important to know that although we can’t reassign an object declared with const, we can still mutate it, meaning we can add new properties and change the properties that are there.

const spaceship = {type: 'shuttle'};
spaceship = {type: 'alien'}; // TypeError: Assignment to constant variable.
spaceship.type = 'alien'; // Changes the value of the type property
spaceship.speed = 'Mach 5'; // Creates a new key of 'speed' with a value of 'Mach 5'

You can delete a property from an object with the delete operator.

const spaceship = {
  'Fuel Type': 'Turbo Fuel',
  homePlanet: 'Earth',
  mission: 'Explore the universe' 
};
 
delete spaceship.mission;  // Removes the mission property

Objects
Methods
10 min

When the data stored on an object is a function we call that a method. A property is what an object has, while a method is what an object does.

Do object methods seem familiar? That’s because you’ve been using them all along! For example console is a global JavaScript object and .log() is a method on that object. Math is also a global JavaScript object and .floor() is a method on it. 



We can include methods in our object literals by creating ordinary, colon-separated key-value pairs. The key serves as our method’s name, while the value is an anonymous function expression.

const alienShip = {
  invade: function () { 
    console.log('Hello! We have come to dominate your planet. Instead of Earth, it shall be called New Xaculon.')
  }
};

With the new method syntax introduced in ES6 we can omit the colon and the function keyword.

const alienShip = {
  invade () { 
    console.log('Hello! We have come to dominate your planet. Instead of Earth, it shall be called New Xaculon.')
  }
};

Object methods are invoked by appending the object’s name with the dot operator followed by the method name and parentheses:

alienShip.invade(); // Prints 'Hello! We have come to dominate your planet. Instead of Earth, it shall be called New Xaculon.'



## June 24th, 2024

Looping Through Objects
15 min

Loops are programming tools that repeat a block of code until a condition is met. We learned how to iterate through arrays using their numerical indexing, but the key-value pairs in objects aren’t ordered! JavaScript has given us alternative solution for iterating through objects with the for...in syntax .

for...in will execute a given block of code for each property in an object.

let spaceship = {
  crew: {
    captain: { 
      name: 'Lily', 
      degree: 'Computer Engineering', 
      cheerTeam() { console.log('You got this!') } 
    },
    'chief officer': { 
      name: 'Dan', 
      degree: 'Aerospace Engineering', 
      agree() { console.log('I agree, captain!') } 
    },
    medic: { 
      name: 'Clementine', 
      degree: 'Physics', 
      announce() { console.log(`Jets on!`) } },
    translator: {
      name: 'Shauna', 
      degree: 'Conservation Science', 
      powerFuel() { console.log('The tank is full!') } 
    }
  }
}; 

// for...in
for (let crewMember in spaceship.crew) {
  console.log(`${crewMember}: ${spaceship.crew[crewMember].name}`);
}

Our for...in will iterate through each element of the spaceship.crew object. In each iteration, the variable crewMember is set to one of spaceship.crew‘s keys, enabling us to log a list of crew members’ role and name.



Objects
Review
<1 min

Way to go! You’re well on your way to understanding the mechanics of objects in JavaScript. By building your own objects, you will have a better understanding of how JavaScript built-in objects work as well. You can also start imagining organizing your code into objects and modeling real world things in code.

Let’s review what we learned in this lesson:

    Objects store collections of key-value pairs.
    Each key-value pair is a property—when a property is a function it is known as a method.
    An object literal is composed of comma-separated key-value pairs surrounded by curly braces.
    You can access, add or edit a property within an object by using dot notation or bracket notation.
    We can add methods to our object literals using key-value syntax with anonymous function expressions as values or by using the new ES6 method syntax.
    We can navigate complex, nested objects by chaining operators.
    Objects are mutable—we can change their properties even when they’re declared with const.
    Objects are passed by reference— when we make changes to an object passed into a function, those changes are permanent.
    We can iterate through objects using the For...in syntax.


Advanced Objects
The this Keyword
12 min

Objects are collections of related data and functionality. We store that functionality in methods on our objects:

const goat = {
  dietType: 'herbivore',
  makeSound() {
    console.log('baaa');
  }
};

In our goat object we have a .makeSound() method. We can invoke the .makeSound() method on goat.

goat.makeSound(); // Prints baaa

Nice, we have a goat object that can print baaa to the console. Everything seems to be working fine. What if we wanted to add a new method to our goat object called .diet() that prints the goat‘s dietType?

const goat = {
  dietType: 'herbivore',
  makeSound() {
    console.log('baaa');
  },
  diet() {
    console.log(dietType);
  }
};
goat.diet(); 
// Output will be "ReferenceError: dietType is not defined"

That’s strange, why is dietType not defined even though it’s a property of goat? That’s because inside the scope of the .diet() method, we don’t automatically have access to other properties of the goat object.

Here’s where the this keyword comes to the rescue. If we change the .diet() method to use the this, the .diet() works! :

const goat = {
  dietType: 'herbivore',
  makeSound() {
    console.log('baaa');
  },
  diet() {
    console.log(this.dietType);
  }
};

goat.diet(); 
// Output: herbivore

The this keyword references the calling object which provides access to the calling object’s properties. In the example above, the calling object is goat and by using this we’re accessing the goat object itself, and then the dietType property of goat by using property dot notation.

Let’s get comfortable using the this keyword in a method.


Test global collisions at
## JSLint.com

create own global object
all uppercase and put everything in there. <script>YOUROBJECT</script>


be strict and intentional about the style rules that are enforced in my code. 

      always use full correct form of code, and end with semi-colon (js will try to implement semi-colon to fix errors, without my knowledge)

      always break a line after a punctuator (, . ; : { } = (  [ ? ! + - * / % ~ ^ | & == <= >= += -= != < > << >> 
      *= /= %= ^= |= &= || && === !== <<= >>= >>> >>>=
      do not break line after name, string, number or ) ] ++ -- 


      be careful with comma usage.
            no extra commas
            Good = [1, 2, 3]
            Bad = [1, 2, 3,]

      use blocks around structured statements: 
            Good:
                  if (a) {
                  b ();
            }
            Bad:
            if (a) b(); 

      Blocks don't have scope in JS so only use them for structured statements:
            if
            while
            for 
            do 
            try 
            switch
            function

      Define all variables at beginning of function. 

      avoid fallthrough in switch statements
            every clause should explicitly end. with break, throw, or return.

## June 25th, 2024
      Don't put java code in html
      link it with src attribute


      put <script> tag as far down in the <body> html tag as possible.
      put the <css> as high in the <head> as possible.
      minimize number of scripts per html page.

      .getElementById is essentially walking the DOM and going through the entire document and pushing an object to fill it up with our found variables.  
      a


Advanced Objects
Privacy
6 min

Accessing and updating properties is fundamental in working with objects. However, there are cases in which we don’t want other code simply accessing and updating an object’s properties. When discussing privacy in objects, we define it as the idea that only certain properties should be mutable or able to change in value.

Certain languages have privacy built-in for objects, but JavaScript does not have this feature. Rather, JavaScript developers follow naming conventions that signal to other developers how to interact with a property. One common convention is to place an underscore _ before the name of a property to mean that the property should not be altered. Here’s an example of using _ to prepend a property.

const bankAccount = {
  _amount: 1000
}

In the example above, the _amount is not intended to be directly manipulated. 

Advanced Objects
Getters
15 min

Getters are methods that get and return the internal properties of an object. But they can do more than just retrieve the value of a property! Let’s take a look at a getter method:

const person = {
  _firstName: 'John',
  _lastName: 'Doe',
  get fullName() {
    if (this._firstName && this._lastName){
      return `${this._firstName} ${this._lastName}`;
    } else {
      return 'Missing a first name or a last name.';
    }
  }
}

// To call the getter method: 
person.fullName; // 'John Doe'

Notice that in the getter method above:

    We use the get keyword followed by a function.
    We use an if...else conditional to check if both _firstName and _lastName exist (by making sure they both return truthy values) and then return a different value depending on the result.
    We can access the calling object’s internal properties using this. In fullName, we’re accessing both this._firstName and this._lastName.
    In the last line we call fullName on person. In general, getter methods do not need to be called with a set of parentheses. Syntactically, it looks like we’re accessing a property.

Now that we’ve gone over syntax, let’s discuss some notable advantages of using getter methods:

    Getters can perform an action on the data when getting a property.
    Getters can return different values using conditionals.
    In a getter, we can access the properties of the calling object using this.
    The functionality of our code is easier for other developers to understand.

Another thing to keep in mind when using getter (and setter) methods is that properties cannot share the same name as the getter/setter function. If we do so, then calling the method will result in an infinite call stack error. One workaround is to add an underscore before the property name like we did in the example above.

Great, let’s go getter!


Advanced Objects
Setters
13 min

Along with getter methods, we can also create setter methods which reassign values of existing properties within an object. Let’s see an example of a setter method:

const person = {
  _age: 37,
  set age(newAge){
    if (typeof newAge === 'number'){
      this._age = newAge;
    } else {
      console.log('You must assign a number to age');
    }
  }
};

Notice that in the example above:

    We can perform a check for what value is being assigned to this._age.
    When we use the setter method, only values that are numbers will reassign this._age
    There are different outputs depending on what values are used to reassign this._age.

Then to use the setter method:

person.age = 40;
console.log(person._age); // Logs: 40
person.age = '40'; // Logs: You must assign a number to age

Setter methods like age do not need to be called with a set of parentheses. Syntactically, it looks like we’re reassigning the value of a property.

Like getter methods, there are similar advantages to using setter methods that include checking input, performing actions on properties, and displaying a clear intention for how the object is supposed to be used. Nonetheless, even with a setter method, it is still possible to directly reassign properties. For example, in the example above, we can still set ._age directly:

person._age = 'forty-five'
console.log(person._age); // Prints forty-five




Advanced Objects
Factory Functions
11 min

So far we’ve been creating objects individually, but there are times where we want to create many instances of an object quickly. Here’s where factory functions come in. A real world factory manufactures multiple copies of an item quickly and on a massive scale. A factory function is a function that returns an object and can be reused to make multiple object instances. Factory functions can also have parameters allowing us to customize the object that gets returned.

Let’s say we wanted to create an object to represent monsters in JavaScript. There are many different types of monsters and we could go about making each monster individually but we can also use a factory function to make our lives easier. To achieve this diabolical plan of creating multiple monsters objects, we can use a factory function that has parameters:

const monsterFactory = (name, age, energySource, catchPhrase) => {
  return { 
    name: name,
    age: age, 
    energySource: energySource,
    scare() {
      console.log(catchPhrase);
    } 
  }
};

In the monsterFactory function above, it has four parameters and returns an object that has the properties: name, age, energySource, and scare(). To make an object that represents a specific monster like a ghost, we can call monsterFactory with the necessary arguments and assign the return value to a variable:

const ghost = monsterFactory('Ghouly', 251, 'ectoplasm', 'BOO!');
ghost.scare(); // 'BOO!'

Now we have a ghost object as a result of calling monsterFactory() with the needed arguments. With monsterFactory in place, we don’t have to create an object literal every time we need a new monster. Instead, we can invoke the monsterFactory function with the necessary arguments to take over the world make a monster for us!



simple factory function to create multiple robots with two parameters and a talking method

            function robotFactory(model, mobile) {
                return {
                    model: model,
                    mobile: mobile,
                    beep() {
                        console.log('Beep Boop');
                    }
                }
            };
            const frank = robotFactory('shiny', 'hellish');
            console.log(frank.model);




Advanced Objects
Destructured Assignment
6 min

We often want to extract key-value pairs from objects and save them as variables. Take for example the following object:

const vampire = {
  name: 'Dracula',
  residence: 'Transylvania',
  preferences: {
    day: 'stay inside',
    night: 'satisfy appetite'
  }
};

If we wanted to extract the residence property as a variable, we could use the following code:

const residence = vampire.residence; 
console.log(residence); // Prints 'Transylvania' 

However, we can also take advantage of a destructuring technique called destructured assignment to save ourselves some keystrokes. In destructured assignment we create a variable with the name of an object’s key that is wrapped in curly braces { } and assign to it the object. Take a look at the example below:

const { residence } = vampire; 
console.log(residence); // Prints 'Transylvania'

Look back at the vampire object’s properties in the first code example. Then, in the example above, we declare a new variable residence that extracts the value of the residence property of vampire. When we log the value of residence to the console, 'Transylvania' is printed.

We can even use destructured assignment to grab nested properties of an object:

const { day } = vampire.preferences; 
console.log(day); // Prints 'stay inside'

Instructions

    Checkpoint 1 Passed

    1.

    Use destructured assignment to create a const variable named functionality that extracts the functionality property of robot.

    If you need a reminder on how to use destructured assignment, review the example in the narrative or check the hint.

Checkpoint 2 Passed

2.

Since functionality is referencing robot.functionality we can call the methods available to robot.functionality simply through functionality.

Take advantage of this shortcut and call the .beep() method on functionality.

You can think of functionality as the object that was pulled out of robot.functionality. To call .beep(), use dot notation with the name of the method and a set of parentheses:

functionality.beep();


Advanced Objects
Review
<1 min

Congratulations on finishing Advanced Objects!

Let’s review the concepts covered in this lesson:

    The object that a method belongs to is called the calling object.
    The this keyword refers to the calling object and can be used to access properties of the calling object.
    Methods do not automatically have access to other internal properties of the calling object.
    The value of this depends on where the this is being accessed from.
    We cannot use arrow functions as methods if we want to access other internal properties.
    JavaScript objects do not have built-in privacy, rather there are conventions to follow to notify other developers about the intent of the code.
    The usage of an underscore before a property name means that the original developer did not intend for that property to be directly changed.
    Setters and getter methods allow for more detailed ways of accessing and assigning properties.
    Factory functions allow us to create object instances quickly and repeatedly.
    There are different ways to use object destructuring: one way is the property value shorthand and another is destructured assignment.
    As with any concept, it is a good skill to learn how to use the documentation with objects!

You’re ready to start leveraging more elegant code for creating and accessing objects in your code!

## June 26th, 2024

Higher-Order Functions
Functions as Parameters
16 min

As you know, a parameter is a placeholder for the data that gets passed into a function. Since functions can behave like any other type of data in JavaScript, it might not surprise you to learn that functions can accept other functions as parameters. A higher-order function is a function that either accepts functions as parameters, returns a function, or both! We call functions that get passed in as parameters callback functions. Callback functions get invoked during the execution of the higher-order function.

When we invoke a higher-order function, and pass another function in as an argument, we don’t invoke the argument function. Invoking it would evaluate to passing in the return value of that function call. With callback functions, we pass in the function itself by typing the function name without the parentheses:

const higherOrderFunc = param => {
  param();
  return `I just invoked ${param.name} as a callback function!`
}
 
const anotherFunc = () => {
  return 'I\'m being invoked by the higher-order function!';
}

higherOrderFunc(anotherFunc);

We wrote a higher-order function higherOrderFunc that accepts a single parameter, param. Inside the body, param gets invoked using parentheses. And finally, a string is returned, telling us the name of the callback function that was passed in.

Below the higher-order function, we have another function aptly named anotherFunc. This function aspires to be called inside the higher-order function.

Lastly, we invoke higherOrderFunc(), passing in anotherFunc as its argument, thus fulfilling its dreams of being called by the higher-order function.

higherOrderFunc(() => {
  for (let i = 0; i <= 10; i++){
    console.log(i);
  }
});

In this example, we invoked higherOrderFunc() with an anonymous function (a function without a name) that counts to 10. Anonymous functions can be arguments too!

Let’s get some practice writing higher-order functions.



Feature detection for building scripts cross browser

Iterators
Introduction to Iterators
3 min

Imagine you had a grocery list and you wanted to know what each item on the list was. You’d have to scan through each row and check for the item. This common task is similar to what we have to do when we want to iterate over, or loop through, an array. One tool at our disposal is the for loop. However, we also have access to built-in array methods which make looping easier.

The built-in JavaScript array methods that help us iterate are called iteration methods, at times referred to as iterators. Iterators are methods called on arrays to manipulate elements and return values.

In this lesson, you will learn the syntax for these methods, their return values, how to use the documentation to understand them, and how to choose the right iterator method for a given task.



const artists = ['Picasso', 'Kahlo', 'Matisse', 'Utamaro'];

artists.forEach(artist => {
  console.log(artist + ' is one of my favorite artists.');
});

const numbers = [1, 2, 3, 4, 5];

const squareNumbers = numbers.map(number => {
  return number * number;
});

console.log(squareNumbers);

const things = ['desk', 'chair', 5, 'backpack', 3.14, 100];

const onlyNumbers = things.filter(thing => {
  return typeof thing === 'number';
});

console.log(onlyNumbers);

Iterators
The .map() Method
12 min

The second iterator we’re going to cover is .map(). When .map() is called on an array, it takes an argument of a callback function and returns a new array! Take a look at an example of calling .map():

const numbers = [1, 2, 3, 4, 5]; 

const bigNumbers = numbers.map(number => {
  return number * 10;
});

.map() works in a similar manner to .forEach()— the major difference is that .map() returns a new array.

In the example above:

    numbers is an array of numbers.
    bigNumbers will store the return value of calling .map() on numbers.
    numbers.map will iterate through each element in the numbers array and pass the element into the callback function.
    return number * 10 is the code we wish to execute upon each element in the array. This will save each value from the numbers array, multiplied by 10, to a new array.

If we take a look at numbers and bigNumbers:

console.log(numbers); // Output: [1, 2, 3, 4, 5]
console.log(bigNumbers); // Output: [10, 20, 30, 40, 50]

Notice that the elements in numbers were not altered and bigNumbers is a new array.


.map and .filter return an array but DO NOT alter it's parent function


Iterators
The .filter() Method
10 min

Another useful iterator method is .filter(). Like .map(), .filter() returns a new array. However, .filter() returns an array of elements after filtering out certain elements from the original array. The callback function for the .filter() method should return true or false depending on the element that is passed to it. The elements that cause the callback function to return true are added to the new array. Take a look at the following example:

const words = ['chair', 'music', 'pillow', 'brick', 'pen', 'door']; 

const shortWords = words.filter(word => {
  return word.length < 6;
});

    words is an array that contains string elements.
    const shortWords = declares a new variable that will store the returned array from invoking .filter().
    The callback function is an arrow function that has a single parameter, word. Each element in the words array will be passed to this function as an argument.
    word.length < 6; is the condition in the callback function. Any word from the words array that has fewer than 6 characters will be added to the shortWords array.

Let’s also check the values of words and shortWords:

console.log(words); // Output: ['chair', 'music', 'pillow', 'brick', 'pen', 'door']; 
console.log(shortWords); // Output: ['chair', 'music', 'brick', 'pen', 'door']

Observe how words was not mutated, i.e. changed, and shortWords is a new array.


simple small number filter 

const randomNumbers = [375, 200, 3.14, 7, 13, 852];

// Call .filter() on randomNumbers below
const smallNumbers = randomNumbers.filter(number => {
  if (number < 150) {
    return number;
  }
});

console.log(smallNumbers);



Iterators
The .findIndex() Method
10 min

We sometimes want to find the location of an element in an array. That’s where the .findIndex() method comes in! Calling .findIndex() on an array will return the index of the first element that evaluates to true in the callback function.

const jumbledNums = [123, 25, 78, 5, 9]; 

const lessThanTen = jumbledNums.findIndex(num => {
  return num < 10;
});

    jumbledNums is an array that contains elements that are numbers.
    const lessThanTen = declares a new variable that stores the returned index number from invoking .findIndex().
    The callback function is an arrow function that has a single parameter, num. Each element in the jumbledNums array will be passed to this function as an argument.
    num < 10; is the condition that elements are checked against. .findIndex() will return the index of the first element which evaluates to true for that condition.

Let’s take a look at what lessThanTen evaluates to:

console.log(lessThanTen); // Output: 3 

If we check what element has index of 3:

console.log(jumbledNums[3]); // Output: 5

Great, the element in index 3 is the number 5. This makes sense since 5 is the first element that is less than 10.

If there isn’t a single element in the array that satisfies the condition in the callback, then .findIndex() will return -1.

const greaterThan1000 = jumbledNums.findIndex(num => {
  return num > 1000;
});

console.log(greaterThan1000); // Output: -1


My Home
Iterators: Review
Narrative and Instructions
Learn
Iterators
Review
1 min

Awesome job on clearing the iterators lesson! You have learned a number of useful methods in this lesson as well as how to use the JavaScript documentation from the Mozilla Developer Network to discover and understand additional methods. Let’s review!

    .forEach() is used to execute the same code on every element in an array but does not change the array and returns undefined.
    .map() executes the same code on every element in an array and returns a new array with the updated elements.
    .filter() checks every element in an array to see if it meets certain criteria and returns a new array with the elements that return truthy for the criteria.
    .findIndex() returns the index of the first element of an array that satisfies a condition in the callback function. It returns -1 if none of the elements in the array satisfies the condition.
    .reduce() iterates through an array and takes the values of the elements and returns a single value.
    All iterator methods take a callback function, which can be a pre-defined function, a function expression, or an arrow function.
    You can visit the Mozilla Developer Network to learn more about iterator methods (and all other parts of JavaScript!).



## June 27th, 2024

Debugging JavaScript Code
JavaScript Error Types
4 min

Now that you can identify the type of error from an error stack trace, you might be wondering what the different types of errors mean.

Here are three common error types:

    SyntaxError: This error will be thrown when a typo creates invalid code — code that cannot be interpreted by the compiler. When this error is thrown, scan your code to make sure you properly opened and closed all brackets, braces, and parentheses and that you didn’t include any invalid semicolons.
    ReferenceError: This error will be thrown if you try to use a variable that does not exist. When this error is thrown, make sure all variables are properly declared.
    TypeError: This error will be thrown if you attempt to perform an operation on a value of the wrong type. For example, if we tried to use a string method on a number, it would throw a TypeError.





Use stack overflow website for debugging answers if can't find on google



CSS Functions
min() and max()
6 min

If we want to create responsive elements, the min() and max() functions are great solutions for setting case-specific design constraints. The min() function will select the smallest value from a range of values and set that as the associated property’s value. The max() function will select the largest value from a range of values, which will be used as the associated property’s value.

In the code snippet below, the width of the .content class is set to be 50vw. If the viewport width is greater than 1000 pixels (meaning that 50vw will be greater than 500px), the width of the content class will be set to a maximum width of 500px.

.content {
  width: 50vw;
  max-width: 500px;
}


CSS Functions
clamp()
6 min

Sometimes we will want to design elements to dynamically scale but also stay confined between an upper and lower bound. The clamp() function is ideal for achieving this!

As its name suggests, the clamp() function enables a specified value to be kept within an upper and lower bound.

.main-text{
  font-size: clamp(12px, 1.5vw, 48px);
}

The clamp() function takes three parameters in a specific order:

    The first argument specifies the minimum value. If the preferred value, given as the second argument, is less than this value, then the minimum value will be used. In the code snippet above, 12px is given as the minimum value of the font-size property.
    The second argument specifies the preferred value. This value is used as long as it is greater than the value of the first argument (lower bound) and less than the value of the third argument (upper bound). In the code snippet above, 1.5vw is given as the preferred value of the font-size property.
    The third argument specifies the maximum value. This value is the largest value that the property will be set to. In the code snippet above, 48px is given as the maximum value of the font-size property.



CSS Functions
Filter Functions
10 min

Like color functions, there are CSS functions specifically for the filter and backdrop-filter properties. These functions create a variety of visual effects for desired elements.

We can use the brightness() function for the filter and backdrop-filter property to affect an element’s overall brightness by applying a linear multiplier to it. The brightness() function takes a single argument for the amount, which can be either a number or percentage. Any value under 100% or 1.0 darkens the element, and any value over 100% or 1.0 will brighten the element. The default value of brightness is 100% or 1.0.

The blur() function applies a Gaussian blur to a specified element. The blur() function takes a single argument for the radius of the blur specified as a length. The argument of this function cannot be unitless unless a blur amount of 0 is being set.

The last filter function we are going to learn about is drop-shadow(). This function applies a drop shadow effect to the desired element. Take a look at the syntax below:

drop-shadow(offset-x offset-y blur-radius color)

Both offset-x and offset-y are required arguments that determine the horizontal and vertical offset respectively. While blur-radius is an optional argument that determines the shadow’s blur radius—the larger the value, the more blurred the shadow. Finally, the color argument is also optional and determines the shadow’s color. Notice that it is not necessary to separate each of the function’s arguments with commas.

Say we want to add a drop shadow to a <button> element. In the below code example, the horizontal offset is set to -10px and the vertical offset to 5px. It has a blur radius of 0.2rem and has a color of rgba(50, 200, 210, 0.6).

button {
  filter: drop-shadow(-10px 5px 0.2rem rgba(50, 200, 210, 0.6));
}

The drop shadow created on the button is offset vertically to the bottom and to the left. It also has a light blue color with 60% opacity.

There are more CSS functions that can be used with the filter and backdrop-filter properties—take a look at the full list to learn more!


CSS Functions
Transform Functions
7 min

We can transform any HTML element using the transform property combined with CSS functions that scale, rotate, and even distort. These functions apply both 2D and 3D transformations to elements.

The scale() function resizes an element, both horizontally and vertically, on a 2D plane. It can take either one or two parameters. If only one argument is given, scale(2) for instance, then the element will grow proportionally on both the x and y-axis. When two arguments are provided, the first argument scales along the x-axis, and the second scales along the y-axis. If you only want to scale an element on one of the two axes, either the scaleX() or the scaleY() function can be used.

The rotate() function can be used for the transform property to rotate an element around a fixed point on a given 2D plane. The function accepts a single argument for the angle, which must be in degrees specified with the deg unit. Any positive angle means clockwise rotation, and a negative angle means counter-clockwise rotation. It is important to note that the origin of rotation defaults to the center of the element being rotated. For example, using rotate(180deg) as the value of transform property would rotate an element at its center, 180 degrees clockwise.

Lastly, the translate() function moves an element from its initial position to another position on the page specified as the function’s arguments. The function can accept either one or two arguments—if one argument is provided, then the function will translate the element along the only x-axis by the specified amount. If two arguments are given, the element translates along the x-axis by the amount specified by the first argument and along the y-axis by the amount specified as the second argument.

.shifted {
  transform: translate(0px, 100px);
}

In the code example above, we wanted to shift the shifted element down the screen by 100px, so we used the transform property and set the translate() function as its value. The function’s x-axis argument was then set to be 0px and the y-axis to be 100px.


## Using a scale on a hover is cool :)

## June 29th, 2024

let and const have block-level scope.
var is global. don't use much. 

just use const unless know you're going to change it.

*markdown*


## July 1st, 2024


      **looping through array easy
const todos = [
    {
        id: 1,
        text: 'Take out trash',
        isCompleted: true
    },
    {
        id: 2,
        text: 'Brush teeth',
        isCompleted: true
    },
    {
        id: 3,
        text: 'Meet with boss',
        isCompleted: false
    }

];

for (let todo of todos) {
    console.log(todo);
}**

      console.log(todo.text) will return just the text: of each array so can loop through the array object and
            single out certain keys or values. 



            ## July 28th ## 

array.reduce 

      can add up all items in the array...i.e

      items = [{
      name: 'macbook pro',
      price: 1799
      },
      {name: 'macbook air',
      price: 1299
      
      }]

      data.reduce(currentTotal, item => {
      return item.price + currentTotal
      
      , 0})


## July 2nd, 2024

querySelector &

querySelectorAll = selects all elements with that tag or class 
      querySelectorAll(.class)
            gives us a collection we can run array methods on


.classList.add('') will add a class to the css of the element you select.

.innerHTML will add html elements 
      .innerHTML = '<h2>HEllo</h2>

.textContent will change text

.innerText will also change text. 

## July 3rd, 2024

classes

class Surgeon {
  constructor(name, department){
    this.name = name;
    this.department = department;
  }

}

Classes
Instance
6 min

Now, we’re ready to create class instances. An instance is an object that contains the property names and methods of a class, but with unique property values. Let’s look at our Dog class example.

class Dog {
  constructor(name) {
    this.name = name;
    this.behavior = 0;
  } 
}

const halley = new Dog('Halley'); // Create new Dog instance
console.log(halley.name); // Log the name value saved to halley
// Output: 'Halley'

Below our Dog class, we use the new keyword to create an instance of our Dog class. Let’s consider the line of code step-by-step.

    We create a new variable named halley that will store an instance of our Dog class.
    We use the new keyword to generate a new instance of the Dog class. The new keyword calls the constructor(), runs the code inside of it, and then returns the new instance.
    We pass the 'Halley' string to the Dog constructor, which sets the name property to 'Halley'.
    Finally, we log the value saved to the name key in our halley object, which logs 'Halley' to the console.

Now you know how to create instances. In the next exercise, you will learn how to add getters, setters, and methods.


class Surgeon {
  constructor(name, department) {
    this.name = name;
    this.department = department;
  }
}

const surgeonRomero = new Surgeon('Francisco Romero', 'Cardiovascular');

const surgeonJackson = new Surgeon('Ruth Jackson', 'Orthopedics');

console.log(surgeonJackson);


Classes
Methods
13 min

At this point, we have a Dog class that spins up objects with name and behavior properties. Below, we will add getters and a method to bring our class to life.

Class method and getter syntax is the same as it is for objects except you can not include commas between methods.

class Dog {
  constructor(name) {
    this._name = name;
    this._behavior = 0;
  }
    
  get name() {
    return this._name;
  }
  
  get behavior() {
    return this._behavior;
  }
  
  incrementBehavior() {
    this._behavior++;
  }
}

In the example above, we add getter methods for name and behavior. Notice, we also prepended our property names with underscores (_name and _behavior), which indicate these properties should not be accessed directly. Under the getters, we add a method named .incrementBehavior(). When you call .incrementBehavior() on a Dog instance, it adds 1 to the _behavior property. Between each of our methods, we did not include commas.


Classes
Inheritance III
14 min

We’ve abstracted the shared properties and methods of our Cat and Dog classes into a parent class called Animal (See below).

class Animal {
  constructor(name) {
    this._name = name;
    this._behavior = 0;
  }
    
  get name() {
    return this._name;
  }
  
  get behavior() {
    return this._behavior;
  }
    
  incrementBehavior() {
    this._behavior++;
  }
} 

Now that we have these shared properties and methods in the parent Animal class, we can extend them to the subclass, Cat.

class Cat extends Animal {
  constructor(name, usesLitter) {
    super(name);
    this._usesLitter = usesLitter;
  }
}

In the example above, we create a new class named Cat that extends the Animal class. Let’s pay special attention to our new keywords: extends and super.

    The extends keyword makes the methods of the animal class available inside the cat class.
    The constructor, called when you create a new Cat object, accepts two arguments, name and usesLitter.
    The super keyword calls the constructor of the parent class. In this case, super(name) passes the name argument of the Cat class to the constructor of the Animal class. When the Animal constructor runs, it sets this._name = name; for new Cat instances.
    _usesLitter is a new property that is unique to the Cat class, so we set it in the Cat constructor.

Notice, we call super on the first line of our constructor(), then set the usesLitter property on the second line. In a constructor(), you must always call the super method before you can use the this keyword — if you do not, JavaScript will throw a reference error. To avoid reference errors, it is best practice to call super on the first line of subclass constructors.

Below, we create a new Cat instance and call its name with the same syntax as we did with the Dog class:

const bryceCat = new Cat('Bryce', false); 
console.log(bryceCat._name); // output: Bryce

In the example above, we create a new instance the Cat class, named bryceCat. We pass it 'Bryce' and false for our name and usesLitter arguments. When we call console.log(bryceCat._name) our program prints, Bryce.

In the example above, we abandoned best practices by calling our _name property directly. In the next exercise, we’ll address this by calling an inherited getter method for our name property.




Classes
Inheritance V
10 min

In addition to the inherited features, child classes can contain their own properties, getters, setters, and methods.

Below, we will add a usesLitter getter. The syntax for creating getters, setters, and methods is the same as it is in any other class.

class Cat extends Animal {
  constructor(name, usesLitter) {
    super(name);
    this._usesLitter = usesLitter;
  }
    
  get usesLitter() {
    return this._usesLitter;
  }
}

In the example above, we create a usesLitter getter in the Cat class that returns the value saved to _usesLitter.

Compare the Cat class above to the one we created without inheritance:

class Cat {
  constructor(name, usesLitter) {
    this._name = name;
    this._usesLitter = usesLitter;
    this._behavior = 0;
  }
    
  get name() {
    return this._name;
  }
  
  get usesLitter() {
    return this._usesLitter;
  }
  
  get behavior() {
    return this._behavior;
  }   
  
  incrementBehavior() {
    this._behavior++;
  }
}

We decreased the number of lines required to create the Cat class by about half. Yes, it did require an extra class (Animal), making the reduction in the size of our Cat class seem moot. However, the benefits (time saved, readability, efficiency) of inheritance grow as the number and size of your subclasses increase.

One benefit is that when you need to change a method or property that multiple classes share, you can change the parent class, instead of each subclass.

Before we move past inheritance, take a moment to see how we would create an additional subclass, called Dog.

class Dog extends Animal {
  constructor(name) {
    super(name);
  }
}

This Dog class has access to the same properties, getters, setters, and methods as the Dog class we made without inheritance, and is a quarter the size.

Now that we’ve abstracted animal daycare features, it’s easy to see how you can extend Animal to support other classes, like Rabbit, Bird or even Snake.
Instructions

    Checkpoint 1 Passed

    1.

    Use the properties and methods below to help you complete the tasks that follow.
    Nurse
        Properties: _name, _remainingVacationDays (set to 20 inside the constructor()), _certifications
        Methods: .takeVacationDays(), .addCertification()

    Under the Nurse constructor(), add a getter that returns the value saved to the Nurse instance’s _certifications.

Checkpoint 2 Passed

2.

Add a method called addCertification under the certifications getter.

The method should accept one input (newCertification). Inside the method, use the push method to add the newCertification value to the nurse’s certifications array.
Checkpoint 3 Passed

3.

At the bottom of main.js call the .addCertification() method on nurseOlynyk with a parameter of 'Genetics'.
Checkpoint 4 Passed

4.

Log the value saved to the certifications property of nurseOlynyk.



Classes
Static Methods
8 min

Sometimes you will want a class to have methods that aren’t available in individual instances, but that you can call directly from the class.

Take the Date class, for example — you can both create Date instances to represent whatever date you want, and call static methods, like Date.now() which returns the current date, directly from the class. The .now() method is static, so you can call it directly from the class, but not from an instance of the class.

Let’s see how to use the static keyword to create a static method called generateName method in our Animal class:

class Animal {
  constructor(name) {
    this._name = name;
    this._behavior = 0;
  }
    
  static generateName() {
    const names = ['Angel', 'Spike', 'Buffy', 'Willow', 'Tara'];
    const randomNumber = Math.floor(Math.random()*5);
    return names[randomNumber];
  }
} 

In the example above, we create a static method called .generateName() that returns a random name when it’s called. Because of the static keyword, we can only access .generateName() by appending it to the Animal class.

We call the .generateName() method with the following syntax:

console.log(Animal.generateName()); // returns a name

You cannot access the .generateName() method from instances of the Animal class or instances of its subclasses (See below).

const tyson = new Animal('Tyson'); 
tyson.generateName(); // TypeError

The example above will result in an error, because you cannot call static methods (.generateName()) on an instance (tyson).


Classes
Review: Classes
2 min

Way to go! Let’s review what you learned.

    Classes are templates for objects.
    JavaScript calls a constructor method when we create a new instance of a class.
    Inheritance is when we create a parent class with properties and methods that we can extend to child classes.
    We use the extends keyword to create a subclass.
    The super keyword calls the constructor() of a parent class.
    Static methods are called on the class, but not on instances of the class.

In completing this lesson, you’ve taken one step closer to writing efficient, production-level JavaScript. Good luck as you continue to develop your skills and move into intermediate-level concepts.


## July 5th, 2024 ##


Learn JavaScript: Error Handling
Constructing an Error
4 min

JavaScript errors are objects that have a name and message property. Previously, we’ve seen how built-in errors alert us about common mistakes in our code. But, what if we need an error message that isn’t covered by the built-in errors? Let’s say we need to inform a user that a string passed in as an argument is too short with a custom message. Such a message isn’t covered by a built-in error, but we could use the Error function to make our own error object with a message that is unique to our program!

console.log(Error('Your password is too weak.'));
// Prints: Error: Your password is too weak.

The Error function takes an argument of a string which becomes the value of the error’s message property. In the code snippet above, we used the Error function to create an error object that has the message 'Your password is too weak.'.

You might also see errors created with the new keyword. Both methods will lead to the same functionality. Take a look:

console.log(new Error('Your password is too weak.'));
// Prints: Error: Your password is too weak.

Keep in mind that creating an error is not the same as throwing an error. A thrown error will cause the program to stop running. We’ll cover how to throw our created errors in the next exercise!



Learn JavaScript: Error Handling
The throw Keyword
2 min

Creating an error doesn’t cause our program to stop — remember, an error must be thrown for it to halt the program.

To throw an error in JavaScript, we use the throw keyword like so:

throw Error('Something wrong happened');
// Error: Something wrong happened

When we use the throw keyword, the error is thrown and code after the throw statement will not execute. Take for example:

throw Error('Something wrong happened');
// Error: Something wrong happened

console.log('This will never run');

After throw Error('Something wrong happened'); is executed and the error object is thrown, the console.log() statement will not run (just like when a built-in JavaScript error was thrown!).

In the next lesson we will cover how to handle an error so that the rest of our code can run!



Learn JavaScript: Error Handling
The try...catch Statement
5 min

Up to this point, thrown errors have caused our program to stop running. But, we have the ability to anticipate and handle these errors by writing code to address the error and allow our program to continue running.

In JavaScript, we use try...catch statement to anticipate and handle errors. Take a look at example below:

try {
  throw Error('This error will get caught');
} catch (e) {
  console.log(e);
}
// Prints: This error will get caught

console.log('The thrown error that was caught in the try...catch statement!');
// Prints: 'The thrown error that was caught in the try...catch statement!'

Now, let’s break down what happened in the try...catch statement above:

    We have code that follows try inside curly braces {} known as the try block.
    Inside the try block we insert code that we anticipate might throw an error.
    Since we want to see what happens if an error is thrown in the try block, we throw an error with the message 'This error will get caught'.
    Following the try block is the catch statement which accepts the thrown error from the try block . The e represents the thrown error.
    The curly braces that follow catch(e) is known as the catch block and contains code that executes to handle the error.
    Since the error is caught, our console.log() after the try...catch statement prints 'The thrown error that was caught in the try...catch statement!'.

Generally speaking, in a try...catch statement, we evaluate code in the try block and if the code throws an error, the code inside the catch block will handle the error for us. The provided example just showcases how a try...catch statement works because we know an error is being thrown. Let’s first practice writing our own try...catch statement and afterwards we will go over a more practical usage of try...catch.



Learn JavaScript: Error Handling
Handling with try...catch
6 min

In the previous exercise we caught an error that we threw, but we can also use a try...catch statement to handle built-in errors that are thrown by the JavaScript engine that is reading and evaluating our code.

const someVar = 'Cannot be reassigned';
try {
  someVar = 'Still going to try';
} catch(e) {
  console.log(e);
}
// Prints: TypeError: Assignment to constant variable.

In the example above, we didn’t use the throw keyword to throw a custom error, rather we tried to re-assign a const variable and a TypeError was thrown. Then, in our catch block, we logged the error to the console.

Using a try...catch statement for built-in JavaScript errors is really beneficial when we need to use data from an external source that’s not written directly in our program.

Let’s say we expect to grab an array from a database but the information we get back is a string. In our program, we could have a function that only works on arrays. If that function was called with a string instead of an array we would get an error and our program would stop running!

However, we can use a try...catch statement to handle the thrown error for us which allows our program to continue running and we receive a message knowing what went wrong! Let’s see how we can implement this in our code.



## July 6th, 2024


Automate and Organize Tests
describe and it blocks
8 min

In Mocha we group tests using the describe function and define tests using the it function. These two functions can be used to make your test suite complete, maintainable, and expressive in the following ways:

    Structure your test suite: you can organize tests into nested groups that reflect the structure of your implementation code.

    Provide informative messages: you can define your tests using human-readable strings.

If you are testing a Math object with the method .max, you could use the following test code.

describe('Math', () => {
  describe('.max', () => {
    it('returns the argument with the highest value', () => {
      // Your test goes here
    });
    it('returns -Infinity when no arguments are provided', () => {
      // Your test goes here
    });
  });
});

Both the describe and it functions accept two parameters: a descriptive string and a callback function. Though the functions are flexible, they are commonly used in the structure above: nest describe blocks to resemble the structure of your implementation code and write individual tests in it blocks. This makes your test suite isolated, maintainable, and expressive.


## July 7th, 2024 ##

You can do it :) Don't get too discouraged


Testing 
Write Expressive Tests
assert.ok
4 min

As a Node module, assert can be imported at the top of your files with

const assert = require('assert');

The functions in the assert library compare values and throw errors as needed using one function call. The small, human-readable format of the functions will help you make a more expressive test suite.

assert.ok(6 - 1 === 5);

In this case 6 - 1 === 5 evaluates to true, so no error is thrown.

If an argument passed to assert.ok() evaluates to false, an AssertionError is thrown. The error communicates to Mocha that a test has failed, and Mocha logs the error message to the console.



Write Expressive Tests
assert.strictEqual
4 min

Take a look at the code below. Will these assertions throw errors?

const a = 3;
const b = '3';
assert.ok(a == b);
assert.ok(a === b);

    The first assertion will not throw an error because it uses loose (==) equality. It performs a type conversion when comparing two things.
    The second will throw an error because it uses strict (===) equality. It returns false if the types differ.

If you need to be strict in evaluating equality, you can use assert.strictEqual().

    assert.equal() performs a == comparison
    assert.strictEqual() performs a === comparison

Compare the following code to the first example. This code performs the same verifications, but it is more expressive. Without parsing any logic, a reader would know the intention of your tests by reading the method names.

const a = 3;
const b = '3';
assert.equal(a, b);
assert.strictEqual(a, b);

    July 2021 Update: the assert documentation recommends always using assert.strictEqual() instead of assert.equal().



Write Expressive Tests
assert.deepEqual I
3 min

Do you think these assertions will throw errors?

const a = {relation: 'twin', age: '17'};
const b = {relation: 'twin', age: '17'};
assert.equal(a, b);
assert.strictEqual(a, b);

Both assertions will throw an error because distinct objects are not considered equal when using either loose or strict equality in JavaScript.

If you need to compare the values within two objects, you can use assert.deepEqual(). This method compares the values of each object using loose (==) equality.

The following code will not throw an error…

assert.deepEqual(a, b);

…and you can confirm by manually comparing the relation and age properties of each object.

a.relation == b.relation;
a.age == b.age;



Write Expressive Tests
assert.deepEqual II
2 min

In the last exercise you used deepEqual() to compare the values of two objects with loose equality. Arrays are also objects, so deepEqual() also compares their values with loose equality.

const arr1 = [1, 2, 3];
const arr2 = [1, 2, 3];
const arr3 = [1, 2, '3'];

assert.deepEqual(arr1, arr2); // No error
assert.deepEqual(arr1, arr3); // No error

If you’d like to learn more about deepEqual(), the documentation is available here.


Write Expressive Tests
Review
<1 min

You can now write tests with Node’s assert library! In this lesson you learned to:

    Check for loose (==) equality with assert.equal()
    Check for strict (===) equality with assert.strictEqual()
    Check the equality of two object’s values with assert.deepEqual()
    Make your tests expressive by using different assert methods found in the Node.js documentation.

As you continue to write tests, remember to always evaluate them against the characteristics of a good test: fast, complete, reliable, isolated, maintainable, and expressive. If you are meeting these six criteria, you are creating high quality test frameworks!


Learn TDD With Mocha
Review
1 min

We have just covered Test Driven Development with Mocha.

At a high-level the process is:

    Write The Test — Start with a test describing the functionality we’d like to see.
    Fail The Test — Write code in response to the test that fails.
    Pass The Test — The tests fail and communicate feedback to developers through error messages. It’s our responsibility to read those messages, then respond by writing the minimum amount of code to address those messages.
    Refactor Your Code — See below.

The development process is guided by the red-green-refactor cycle.
Red

Write a test that covers the functionality you would like to see implemented. You don’t have to know what your code looks like at this point, you just have to know what it will do.

Run the test. You should see it fail. Most test runners will output red for failure and green for success. While we say “failure” do not take this negatively. It’s a good sign! By seeing the test fail first, we know that once we make it pass, our code works.
Green

Read the error message from the failing test, and write as little code as possible to fix the current error message. By only writing enough code to see our test pass, we tend to write less code as a whole. Continue this process until the test passes.

This may involve writing intermediary features covering lower level functionality which require their own Red, Green, Refactor cycle. The edge-case was an example of this.

Do not focus on code quality at this point. Be shameless! We simply want to get our new test passing.
Refactor

Clean up your code, reducing any duplication you may have introduced. This includes your code as well as your tests.

Treat your test suite with as much respect as you would your live code, as it can quickly become difficult to maintain if not handled with care. You should feel confident enough in the tests you’ve written that you can make your changes without breaking anything.



## July 8th, 2024 ##

General Asynchronous Programming Concepts

Explore asynchronous programming and how it allows applications/apps to run operations in a non-sequential order.
What is Synchronous Code?

Before we define asynchronous code, let’s first start with synchronous code. We don’t even have to start with code, let’s use a real-life example.

Consider the building of a house. We would first need to first lay down the bricks that make our foundation. Then, we layer more bricks on top of each other, building the house from the ground up. We can’t skip a level and expect our house to be stable. Therefore, the laying of bricks happens synchronously, or in sequential order.

Likewise, synchronous code executes in sequential order — it starts with the code at the top of the file and executes line by line until it gets to the end of the file. This type of behavior is known as blocking (or blocking code) since each line of code cannot execute until the previous line finishes.
What is Asynchronous Code?

Let’s begin again with examining a real-life scenario, like baking a cake. We could start to preheat the oven and prepare our cake’s ingredients while we wait for our oven to heat up. The wait for the oven and the preparation of ingredients can happen at the same time, and thus these actions happen asynchronously.

Similarly, asynchronous code can be executed in parallel to other code that is already running. Without the need to wait for other code to finish before executing, our apps can save time and be more efficient. This type of behavior is considered non-blocking.
Asynchronous Code Under the Hood

For most programming languages, the ability to execute asynchronous code depends on the number of threads that an app has access to. We can think of a thread as a resource that a computer provides an app to do a task. Typically one thread allows for an app to complete one task. If we return to our house example, our computers thread tasks might look like this:

Thread 1: build house foundation -> build walls -> construct floor 

A single thread could work for a synchronous task like building a house. However, in our cake baking example, our threads would have to look like this:

Thread 1: preheat oven
Thread 2: prepare ingredients -> bake cake

We won’t discuss in-depth how many threads an app can access but we should note that the more threads we have, the more tasks we can run concurrently. Also, in most modern-day computers, multithreading is achieved by having a CPU that has multiple cores or by some other technology.
Asynchronous Code in Web Development

Similar to how asynchronous behavior is useful in baking a cake, it can also be helpful for web programming. If we use synchronous (blocking) code in the browser, we might be stopping a user from being able to interact with a web app until the code is done running. This isn’t a great user experience. If our app takes a long time to load, our users might think that something’s wrong and might even opt to browse a different site!

However, if we opt for an asynchronous approach, we can cut down on the wait time. We’d load only the code that’s necessary for user interactions and then load up other bits of code in the background. With asynchronous code, we can create better user experiences and make apps that work more efficiently! 




Introduction to Asynchronous JavaScript

Learn how JavaScript enables asynchronous actions.
Asynchronous Code in Web Development

JavaScript provides us with a seamless web browsing experience using asynchronous code. Sites often allow us to perform different interactions like scrolling through content, clicking to create a pop-up modal, typing out text, etc. When a site is set up to respond to different user actions at the same time, it’s likely that this site is using asynchronous JavaScript code. Such code takes into consideration how users might use the site without blocking them (forcing the user to wait for code from one interaction to finish before moving on to the next).

It is our job as developers to think about how much time it takes to complete a task and how to plan around that wait. Tasks like contacting the back-end to retrieve information, querying our database for user information, or making a request to an external server, like a 3rd party API, take varying amounts of time. Since we aren’t sure when we’ll get this information back, we can use asynchronous code to run these tasks in the background. Let’s see how JavaScript handles asynchronous code.
JavaScript and Asynchronous Code

JavaScript is a single-threaded language. This means it has a single thread that can carry out one task at a time. However, Javascript has what is known as the event loop, a specific design that allows it to perform asynchronous tasks even while only using a single thread (more on this later!). Let’s examine some examples of asynchronous code in Javascript!
Asynchronous Callbacks

One common example of asynchronicity in JavaScript is the use of asynchronous callbacks. This is a type of callback function that executes after a specific condition is met and runs concurrently to any other code currently running. Let’s look at an example:

easterEgg.addEventListener('click', () => {
  console.log('Up, Up, Down, Down, Left, Right, Left, Right, B, A');
});

In the code above, the function passed as the second argument of .addEventListener() is an asynchronous callback — this function doesn’t execute until the easterEgg is clicked.
setTimeout

In addition to asynchronous callbacks, JavaScript provides a handful of built-in functions that can perform tasks asynchronously. One function that is commonly used is the setTimeout() function.

With setTimeout() we can write code that tells our JavaScript program to wait a minimum amount of time before executing its callback function. Take a look at this example:

setTimeout(() => {
  console.log('Delay the printing of this string, please.');
}, 1000);

Notice that setTimeout() takes 2 arguments, a callback function and a number specifying how long to wait before executing the function. In the example above, the function will print 'Delay the printing of this string, please.' after 1000 milliseconds (or 1 second) have passed.

Since setTimeout() is non-blocking, we can be executing multiple lines of code at the same time! . Imagine if we had a program like this:

setTimeout(() => {
  console.log('Delay the printing of this string, please.');
}, 1000);
console.log('Doing important stuff.');
console.log('Still doing important stuff.'); 

Which outputs:

'Doing important stuff.'
'Still doing important stuff.' 
'Delay the printing of this string, please.'

If we take a closer look at the output, we’ll see that our setTimeout()‘s callback function didn’t execute until after our other very important console.log() statements were executed.

In web development, this means we can write code to wait for an event to trigger all while a user goes on interacting with our app. One such example could be if a user goes to a shopping site and gets notified that an item is up for sale and only for a limited time. Our asynchronous code could allow the user to interact with our site and when the sale timer expires, our code will remove the sale item.
setInterval()

Another common built-in function is setInterval() which also takes a callback function and a number specifying how often the callback function should execute. For example:

setInterval(() => {
  alert('Are you paying attention???')
}, 300000)

The setInterval() would call the alert() function and show a pop-up message of 'Are you paying attention???' every 300000 milliseconds (or 5 minutes). Note: Please don’t actually do this in your apps, thank you.

While we wait for our alert to chime in every 5 minutes, our users could still use our app! Note: Again, please don’t do this.

With setInterval(), we can programmatically create an alarm, a countdown timer, set the frequency of an animation, and so much more! 

Thanks to the event loop, JavaScript is a single-threaded, event-driven language that can run non-blocking code asynchronously. The Event Loop can be summarized as: when code is executed, it is handled by the heap and call stack, which interact with Node and Web APIs. Those APIs enable concurrency and pass asynchronous messages back to the stack via an event queue. The event queue’s interaction with the call stack is managed by an event loop. All together, those parts maintain the order of code execution when we run asynchronous functions. 


Concurrency in JavaScript

Usually when we think about concurrency in programming, it means that two or more procedures are executed at the same time on the same shared resources. Since JavaScript is single-threaded, as we saw in the for loop example, we’ll never have that flavor of “true” concurrency. However, we can emulate concurrency using the event loop.


Understand the Components of the Event Loop

The event loop is made up of these parts:

    Memory Heap
    Call Stack
    Event Queue
    Event Loop
    Node or Web APIs

Let’s take a closer look at each part before we put it all together.

JavaScript Promises
What is a Promise?
2 min

Promises are objects that represent the eventual outcome of an asynchronous operation. A Promise object can be in one of three states:

    Pending: The initial state— the operation has not completed yet.
    Fulfilled: The operation has completed successfully and the promise now has a resolved value. For example, a request’s promise might resolve with a JSON object as its value.
    Rejected: The operation has failed and the promise has a reason for the failure. This reason is usually an Error of some kind.

We refer to a promise as settled if it is no longer pending— it is either fulfilled or rejected. Let’s think of a dishwasher as having the states of a promise:

    Pending: The dishwasher is running but has not completed the washing cycle.
    Fulfilled: The dishwasher has completed the washing cycle and is full of clean dishes.
    Rejected: The dishwasher encountered a problem (it didn’t receive soap!) and returns unclean dishes.

If our dishwashing promise is fulfilled, we’ll be able to perform related tasks, such as unloading the clean dishes from the dishwasher. If it’s rejected, we can take alternate steps, such as running it again with soap or washing the dishes by hand.

All promises eventually settle, enabling us to write logic for what to do if the promise fulfills or if it rejects.



JavaScript Promises
The Node setTimeout() Function
12 min

Knowing how to construct a promise is useful, but most of the time, knowing how to consume, or use, promises will be key. Rather than constructing promises, you’ll be handling Promise objects returned to you as the result of an asynchronous operation. These promises will start off pending but settle eventually.

Moving forward, we’ll be simulating this by providing you with functions that return promises which settle after some time. To accomplish this, we’ll be using setTimeout(). setTimeout() is a Node API (a comparable API is provided by web browsers) that uses callback functions to schedule tasks to be performed after a delay. setTimeout() has two parameters: a callback function and a delay in milliseconds.

const delayedHello = () => {
  console.log('Hi! This is an asynchronous greeting!');
};

setTimeout(delayedHello, 2000);

Here, we invoke setTimeout() with the callback function delayedHello() and 2000. In at least two seconds delayedHello() will be invoked. But why is it “at least” two seconds and not exactly two seconds?

This delay is performed asynchronously—the rest of our program won’t stop executing during the delay. Asynchronous JavaScript uses something called the event-loop. After two seconds, delayedHello() is added to a line of code waiting to be run. Before it can run, any synchronous code from the program will run. Next, any code in front of it in the line will run. This means it might be more than two seconds before delayedHello() is actually executed.

Let’s look at how we’ll be using setTimeout() to construct asynchronous promises:

const returnPromiseFunction = () => {
  return new Promise((resolve, reject) => {
    setTimeout(( ) => {resolve('I resolved!')}, 1000);
  });
};

const prom = returnPromiseFunction();

In the example code, we invoked returnPromiseFunction() which returned a promise. We assigned that promise to the variable prom. Similar to the asynchronous promises you may encounter in production, prom will initially have a status of pending.

Let’s explore setTimeout() a bit more.



JavaScript Promises
Consuming Promises
4 min

The initial state of an asynchronous promise is pending, but we have a guarantee that it will settle. How do we tell the computer what should happen then? Promise objects come with an aptly named .then() method. It allows us to say, “I have a promise, when it settles, then here’s what I want to happen…”

In the case of our dishwasher promise, the dishwasher will run then:

    If our promise rejects, this means we have dirty dishes, and we’ll add soap and run the dishwasher again.
    If our promise fulfills, this means we have clean dishes, and we’ll put the dishes away.

.then() is a higher-order function— it takes two callback functions as arguments. We refer to these callbacks as handlers. When the promise settles, the appropriate handler will be invoked with that settled value.

    The first handler, sometimes called onFulfilled, is a success handler, and it should contain the logic for the promise resolving.
    The second handler, sometimes called onRejected, is a failure handler, and it should contain the logic for the promise rejecting.

We can invoke .then() with one, both, or neither handler! This allows for flexibility, but it can also make for tricky debugging. If the appropriate handler is not provided, instead of throwing an error, .then() will just return a promise with the same settled value as the promise it was called on. One important feature of .then() is that it always returns a promise. We’ll return to this in more detail in a later exercise and explore why it’s so important.


JavaScript Promises
Using catch() with Promises
10 min

One way to write cleaner code is to follow a principle called separation of concerns. Separation of concerns means organizing code into distinct sections each handling a specific task. It enables us to quickly navigate our code and know where to look if something isn’t working.

Remember, .then() will return a promise with the same settled value as the promise it was called on if no appropriate handler was provided. This implementation allows us to separate our resolved logic from our rejected logic. Instead of passing both handlers into one .then(), we can chain a second .then() with a failure handler to a first .then() with a success handler and both cases will be handled.

prom
 .then((resolvedValue) => {
   console.log(resolvedValue);
 })
 .then(null, (rejectionReason) => {
   console.log(rejectionReason);
 });

Since JavaScript doesn’t mind whitespace, we follow a common convention of putting each part of this chain on a new line to make it easier to read. To create even more readable code, we can use a different promise function: .catch().

The .catch() function takes only one argument, onRejected. In the case of a rejected promise, this failure handler will be invoked with the reason for rejection. Using .catch() accomplishes the same thing as using a .then() with only a failure handler.

Let’s look at an example using .catch():

prom
 .then((resolvedValue) => {
   console.log(resolvedValue);
 })
 .catch((rejectionReason) => {
   console.log(rejectionReason);
 });

Let’s break down what’s happening in the example code:

    prom is a promise which randomly either resolves with 'Yay!' or rejects with 'Ohhh noooo!'.
    We pass a success handler to .then() and a failure handler to .catch().
    If the promise resolves, .then()‘s success handler will be invoked with 'Yay!'.
    If the promise rejects, .then() will return a promise with the same rejection reason as the original promise and .catch()‘s failure handler will be invoked with that rejection reason.

JavaScript Promises
Avoiding Common Mistakes
9 min

Promise composition allows for much more readable code than the nested callback syntax that preceded it. However, it can still be easy to make mistakes. In this exercise, we’ll go over two common mistakes with promise composition.

Mistake 1: Nesting promises instead of chaining them.

returnsFirstPromise()
.then((firstResolveVal) => {
  return returnsSecondValue(firstResolveVal)
    .then((secondResolveVal) => {
      console.log(secondResolveVal);
    })
})

Let’s break down what’s happening in the above code:

    We invoke returnsFirstPromise() which returns a promise.
    We invoke .then() with a success handler.
    Inside the success handler, we invoke returnsSecondValue() with firstResolveVal which will return a new promise.
    We invoke a second .then() to handle the logic for the second promise settling all inside the first then()!
    Inside that second .then(), we have a success handler which will log the second promise’s resolved value to the console.

Instead of having a clean chain of promises, we’ve nested the logic for one inside the logic of the other. Imagine if we were handling five or ten promises!

Mistake 2: Forgetting to return a promise.

returnsFirstPromise()
.then((firstResolveVal) => {
  returnsSecondValue(firstResolveVal)
})
.then((someVal) => {
  console.log(someVal);
})

Let’s break down what’s happening in the example:

    We invoke returnsFirstPromise() which returns a promise.
    We invoke .then() with a success handler.
    Inside the success handler, we create our second promise, but we forget to return it!
    We invoke a second .then(). It’s supposed to handle the logic for the second promise, but since we didn’t return, this .then() is invoked on a promise with the same settled value as the original promise!

Since forgetting to return our promise won’t throw an error, this can be a really tricky thing to debug!


JavaScript Promises
Using Promise.all()
18 min

When done correctly, promise composition is a great way to handle situations where asynchronous operations depend on each other or execution order matters. What if we’re dealing with multiple promises, but we don’t care about the order? Let’s think in terms of cleaning again.

For us to consider our house clean, we need our clothes to dry, our trash bins emptied, and the dishwasher to run. We need all of these tasks to complete but not in any particular order. Furthermore, since they’re all getting done asynchronously, they should really all be happening at the same time!

To maximize efficiency we should use concurrency, multiple asynchronous operations happening together. With promises, we can do this with the function Promise.all().

Promise.all() accepts an array of promises as its argument and returns a single promise. That single promise will settle in one of two ways:

    If every promise in the argument array resolves, the single promise returned from Promise.all() will resolve with an array containing the resolve value from each promise in the argument array.
    If any promise from the argument array rejects, the single promise returned from Promise.all() will immediately reject with the reason that promise rejected. This behavior is sometimes referred to as failing fast.

Let’s look at a code example:

let myPromises = Promise.all([returnsPromOne(), returnsPromTwo(), returnsPromThree()]);

myPromises
  .then((arrayOfValues) => {
    console.log(arrayOfValues);
  })
  .catch((rejectionReason) => {
    console.log(rejectionReason);
  });

Let’s break down what’s happening:

    We declare myPromises assigned to invoking Promise.all().
    We invoke Promise.all() with an array of three promises— the returned values from functions.
    We invoke .then() with a success handler which will print the array of resolved values if each promise resolves successfully.
    We invoke .catch() with a failure handler which will print the first rejection message if any promise rejects.


## July 9th, 2024 ##

Async Await
The await Operator
13 min

In the last exercise, we covered the async keyword. By itself, it doesn’t do much; async functions are almost always used with the additional keyword await inside the function body.

The await keyword can only be used inside an async function. await is an operator: it returns the resolved value of a promise. Since promises resolve in an indeterminate amount of time, await halts, or pauses, the execution of our async function until a given promise is resolved.

In most situations, we’re dealing with promises that were returned from functions. Generally, these functions are through a library, and, in this lesson, we’ll be providing them. We can await the resolution of the promise it returns inside an async function. In the example below, myPromise() is a function that returns a promise which will resolve to the string "I am resolved now!".

async function asyncFuncExample(){
  let resolvedValue = await myPromise();
  console.log(resolvedValue);
}

asyncFuncExample(); // Prints: I am resolved now!

Within our async function, asyncFuncExample(), we use await to halt our execution until myPromise() is resolved and assign its resolved value to the variable resolvedValue. Then we log resolvedValue to the console. We’re able to handle the logic for a promise in a way that reads like synchronous code.


promise.finally runs after your .then and your .catch and will run after all other promises are fulfilled (whether successful or not) and is good for cleaning up code or removing event listeners or something of the like. 


using await in an async function is powerful because you can set the resolve of the promise to a variable and 
use it for anything else.

async await have to be used together

just parsed my first api for weather data on my own comp :)

async/await only affects the promise receiver. The promise creator stays the same.

you can await any function that returns a promise

most any function can be converted into an async function

all async functions return a promise by default


Cool weather app with actual api data! :) 

                              const weatherLocation = document.querySelector('.weather-container');
                        const temperature = document.querySelector('.temperature');
                        const emojiSelector = document.querySelector('.emoji');
                        
                        async function start() {
                            const data = await fetch("https://api.weather.gov/gridpoints/DMX/91,87/forecast")
                            const result = await data.json();
                            weatherLocation.innerHTML = result.properties.periods[1].detailedForecast;
                            temperature.innerHTML = result.properties.periods[1].temperature;
                            
                        };
                        
                        
                        start();



## July 10th, 2024 ##

can set the url in a variable
      const name = url

.json() also returns a promise if calling from an api
      so will have to await variable.json() as well to get it to return a desirable result. 


## July 12th 2024 ##


Async Await
Handling Errors
13 min

When .catch() is used with a long promise chain, there is no indication of where in the chain the error was thrown. This can make debugging challenging.

With async...await, we use try...catch statements for error handling. By using this syntax, not only are we able to handle errors in the same way we do with synchronous code, but we can also catch both synchronous and asynchronous errors. This makes for easier debugging!

async function usingTryCatch() {
 try {
   let resolveValue = await asyncFunction('thing that will fail');
   let secondValue = await secondAsyncFunction(resolveValue);
 } catch (err) {
   // Catches any errors in the try block
   console.log(err);
 }
}

usingTryCatch();

Remember, since async functions return promises we can still use native promise’s .catch() with an async function

async function usingPromiseCatch() {
   let resolveValue = await asyncFunction('thing that will fail');
}

let rejectedPromise = usingPromiseCatch();
rejectedPromise.catch((rejectValue) => {
console.log(rejectValue);
})

This is sometimes used in the global scope to catch final errors in complex code.


Narrative and Instructions
Learn
Async Await
Handling Independent Promises
14 min

Remember that await halts the execution of our async function. This allows us to conveniently write synchronous-style code to handle dependent promises. But what if our async function contains multiple promises which are not dependent on the results of one another to execute?

async function waiting() {
 const firstValue = await firstAsyncThing();
 const secondValue = await secondAsyncThing();
 console.log(firstValue, secondValue);
}

async function concurrent() {
 const firstPromise = firstAsyncThing();
 const secondPromise = secondAsyncThing();
console.log(await firstPromise, await secondPromise);
}

In the waiting() function, we pause our function until the first promise resolves, then we construct the second promise. Once that resolves, we print both resolved values to the console.

In our concurrent() function, both promises are constructed without using await. We then await each of their resolutions to print them to the console.

With our concurrent() function both promises’ asynchronous operations can be run simultaneously. If possible, we want to get started on each asynchronous operation as soon as possible! Within our async functions we should still take advantage of concurrency, the ability to perform asynchronous actions at the same time.

Note: if we have multiple truly independent promises that we would like to execute fully in parallel, we must use individual .then() functions and avoid halting our execution with await.



Async Await
Await Promise.all()
13 min

Another way to take advantage of concurrency when we have multiple promises which can be executed simultaneously is to await a Promise.all().

We can pass an array of promises as the argument to Promise.all(), and it will return a single promise. This promise will resolve when all of the promises in the argument array have resolved. This promise’s resolve value will be an array containing the resolved values of each promise from the argument array.

async function asyncPromAll() {
  const resultArray = await Promise.all([asyncTask1(), asyncTask2(), asyncTask3(), asyncTask4()]);
  for (let i = 0; i<resultArray.length; i++){
    console.log(resultArray[i]); 
  }
}

In our above example, we await the resolution of a Promise.all(). This Promise.all() was invoked with an argument array containing four promises (returned from required-in functions). Next, we loop through our resultArray, and log each item to the console. The first element in resultArray is the resolved value of the asyncTask1() promise, the second is the value of the asyncTask2() promise, and so on.

Promise.all() allows us to take advantage of asynchronicity— each of the four asynchronous tasks can process concurrently. Promise.all() also has the benefit of failing fast, meaning it won’t wait for the rest of the asynchronous actions to complete once any one has rejected. As soon as the first promise in the array rejects, the promise returned from Promise.all() will reject with that reason. As it was when working with native promises, Promise.all() is a good choice if multiple asynchronous tasks are all required, but none must wait for any other before executing.



## july 14th, 2024 ## 

JSON Object vs. JavaScript Object

Here is an example JSON object of a person named Kate, who is 30 years old, and whose hobbies include reading, writing, cooking, and playing tennis:

{
  "person": {  
    "name": "Kate",  
    "age": 30,  
    "hobbies": [ "reading", "writing", "cooking", "tennis" ] 
  }
}

Represented as a JavaScript object literal, the same information would appear as:

{  
  person: {
    name: 'Kate',  
    age: 30,  
    hobbies: [ 'reading', 'writing', 'cooking', 'tennis' ] 
  }
}


Requests with Fetch API
Introduction to Requests with ES6
3 min

Have you ever wondered what happens after you click a “Submit” button on a web page? For instance, if you are submitting information, where does the information go? How is the information processed? The answer to the previous questions revolves around HTTP requests.

There are many types of HTTP requests. The four most commonly used types of HTTP requests are GET, POST, PUT, and DELETE. In this lesson, we’ll cover GET and POST requests.

With a GET request, we’re retrieving, or getting, information from some source (usually a website). For a POST request, we’re posting information to a source that will process the information and send it back.

JavaScript uses an event loop to handle asynchronous function calls. When a program is run, function calls are made and added to a stack. The functions that make requests that need to wait for servers to respond then get sent to a separate queue. Once the stack has cleared, then the functions in the queue are executed.

Web developers use the event loop to create a smoother browsing experience by deciding when to call functions and how to handle asynchronous events. We will go into event loops in more detail in the Concurrency Model and Event Loop in JavaScript article.

To make asynchronous event handling easier, promises were introduced in ES6 JavaScript.

In this lesson, we will explain how to use fetch() and promises to handle requests. Then, we will simplify requests using async and await.


## July 15th, 2024 ##

Requests with Fetch API
Review
1 min

In this lesson, we learned how to make GET and POST requests using the Fetch API and async/await keywords. Let’s recap on the concepts covered in the previous exercises:

    GET and POST requests can be created in a variety of ways.
    We can use fetch() and async/await to asynchronous request data from APIs.
    Promises are a type of JavaScript object that represents data that will eventually be returned from a request.
    The fetch() function can be used to create requests and will return promises.
    We can chain .then() methods to handle promises returned by the fetch() function.
    The async keyword is used to create asynchronous functions that will return promises.
    The await keyword can only be used with functions declared with the async keyword.
    The await keyword suspends the program while waiting for a promise to resolve.

Congratulations on learning all about asynchronous requests using fetch(), async, and await! These concepts are fundamental to helping you develop more robust web apps!

## July 19th, 2024 ##


getting input from search value 

                  const searchInput = document.querySelector('.search__bar');
                  const searchValue = searchInput.value;
                  const buttonDiv = document.querySelector('button');
                  
               #searchInput.addEventListener('keyup', (e) => {
                      buttonDiv.innerHTML = e.target.value;
                  })#


## July 20th, 2024 ##

prototypal inheiritance

j.s will keep looking through __proto__s until it finds an instance of whatever you're calling.  


cool timing function script
      /*function createSpan(){
    let index = 0;
    let timer = setInterval(function(){
        document.querySelector('span').innerHTML= jobs[index];
        index++;
        if (index === jobs.length) {
            document.querySelector('span').style.color = 'rgb(240, 201, 180)';
            document.querySelector('span').style.fontSize = '4rem';
            clearInterval(timer);
        }
            }, 1000);
            
            }
            
            createSpan();*/


#date function#

const date = new Date()
yearEl = date.getYear()


## July 22nd, 2024 ## 



.classList.toggle  = will add or remove a class from our element depending on if it exists there already


## July 31st, 2024 ##

pomodoro app javascript code:


const timerNumbers = document.querySelector('.numbers');
const startButton = document.querySelector('.start');
const stopButton = document.querySelector('.stop');
const resetButton = document.querySelector('.reset');

let interval;
let timeLeft = 1500;

function updateTimer() {
    timerNumbers.textContent = `${Math.floor((timeLeft / 60)).toFixed(0).toString().padStart(2, '0')}:${(timeLeft % 60).toString().padStart(2, "0")}`;
}


// start time

function startTime() {
    interval = setInterval(() => {
    timeLeft--;
    updateTimer();
    if (timeLeft === 0) {
        clearInterval(interval)
        alert('Time is Up!');
        timeLeft = 1500;
    }
    }, 1000)
   
}

startButton.addEventListener('click', () => {
    startTime()
    clearInterval(interval);
})

// stop time 

function stopTime() {
    clearInterval(interval)
}

stopButton.addEventListener('click', stopTime)

// reset time 

function resetTime() {
    timeLeft = 1500;
    clearInterval(interval);
    updateTimer()
}

resetButton.addEventListener('click', resetTime)
