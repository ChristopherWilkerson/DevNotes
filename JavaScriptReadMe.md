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

