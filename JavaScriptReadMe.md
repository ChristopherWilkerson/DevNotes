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
