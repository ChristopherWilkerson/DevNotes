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




                              
                              