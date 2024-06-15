## Python Notes
#### June 10th, 2024


python interpreter starts from top of code and works line by line toward the bottom.
" " equals a string (series of characters
print("*" * 10) = multiplying the string by 10. So will output 10 *s in code.
    also known as an 'expression'

= to identify a variable
    i.e price = 10 
      then print(price) will output "10"
      but not print("price") which will output "price"

Boolean values = true or false 
  i.e. is_published = True
       is_published = False

Python IS case sensitive

define variables with lowercase

Separate words with underscore _
Not - as in html and css

name = input("What is your name? ")
print("Hi " + name)

simple name input exercise: 

color = input("What is your favorite color? ")
print(name + " likes " + color)

int () = converts a string into an integer
float () = converts a string into a number with a decimal point
bool () = converts string into boolean value


simple weight lbs to kg program

user_weight = input("user_weight: ")
weight = 0.45359237 * int(user_weight)
print(weight)


Triple quotes for defining on multiple lines
    ''' asdifaodfhadfoa
adfiadsofijaf
adoifasdfjdso'''

[] = returns character in string. 1,2,3,4,5 [0] is first character. [1] is second character. [-1] is last character

formatted strings

f"  " with curly brackets used to define variables
   i.e first_name = "John"
  last_name = "Smith"
  message = first_name + " [" + last_name + "] is a coder "
**  msg = f"{first_name} [{last_name}] is a coder"     **
  print(msg)

len() = calculate number of characters

. after a variable allows for a method (a function specific to a variable)
course.uppercase = uppercase letters for our variable
      course = "Python for Beginners"
      print(course.upper())

find an instance
    .find()

replace in output

.replace
        variable.replace('x', 'y')

check to see if something exists in your string

in

  ie course = "Python for Beginners"

        "Python" in course

CASE SENSITIVE

## June 11th, 2024
Arithmatic 

number1 ** number2  = number 1 to the power of number 2

Augmented

x = 10
x = x + 3 
    will return 13
x += 3 
    will also return 13

order of operations are just standard math order

parenthesis
exponents
mult and div
add and sub


round() = rounding float up to nearest integer
abs() = absolute value, or positive value of result.


********

import math

math. 

if functions - 
boolean rules;


is_hot = True
is_cold = False

if is_hot:
    print("It's a hot day")
    print("Drink plenty of water")
elif is_cold:
    print("It's a cold day")
    print("Wear warm clothes")
else:
    print("Enjoy your day")

simple down payment calc

price = 1000000
is_good = False
is_bad = True

if is_good:
    down_payment = 0.1 * price
elif is_bad:
    down_payment = 0.2 * price
print(f"Down payment: ${down_payment}")

simple credit loan approval with AND operator

has_high_income = True
has_good_credit = True

if has_high_income and has_good_credit:
    print("Eligible for loan")
else:
    print("Not eligible for loan")


Operators = and, or, not


<  less than
<= less than or equal to
> greater than
>= greater than or equal to
== equal to
!= not equal

simple temp program

temperature = input("What is the current temperature?: ")
if int(temperature) < 50:
    print("Bundle up, it's freezing")
elif int(temperature) < 70:
    print("absolutely perfect")
elif int(temperature) > 70:
    print("it's hot as shit, good luck")

simple character limit program

name = input("what is your name? ")
if len(name) < 3:
    print("name is too short")
elif len(name) > 50:
    print("name is too long")
else:
    print("name looks good!")

simple weight conversion 2.0

weight = int(input("what is your weight? "))
unit = input('(L)bs or (K)g: ')
if unit.upper() == "L":
    converted = weight * 0.45
    print(f"you are {converted} kilos ")
if unit.upper() == "K":
    converted = weight / 0.45
    print(f"you are {converted} pounds ")


Today I learned css colors, a little about git, git functions, and git hub. I also learned about typography
and importing fonts to html projects. I started a table project to refresh my memory on how to create tables in html
as well as to serve as my notes on the subject. Finally I learned some arithmetic and if and conditional functions in python and how to program them.


## June 13th, 2024

while loop

while condition:

example

    i = 1
    while i <= 5:
    print(i)
    i = i + 1


    (don't forget the colon)

Renaming a variable

rightclick refactor then rename

or hotkey shift+F6

break
    will break the loop

simple car game that doesn't exit program until given command to "quit"

             Old CODE               command = ""
                        while command.lower() != "quit":
                            user_input = input("> ")
                            if user_input == "quit":
                                print("sorry to see you go ")
                                break
                            elif user_input.lower() == "help":
                                print("start - to start the car ")
                                print("stop -- to stop the car ")
                                print("cruise -- to cruise around ")
                                print("quit -- to exit ")
                            elif user_input.lower() == "stop":
                                print("the car has been stopped ")
                            elif user_input.lower() == "start":
                                print("the car has been started ")
                            elif user_input.lower() == "cruise":
                                print("you're cruising around town listening to LANY ")
                            else:
                                print("sorry, I do not understand ")



        Revised Code (slimmer)
        
                
                user_input = ""
        while user_input != "quit":
            user_input = input("> ").lower()
            if user_input == "quit":
                print("sorry to see you go ")
                break
            elif user_input == "help":
                print("""
                start -- to start the car 
                stop -- to stop the car
                cruise -- to cruise around 
                quit -- to exit """)
            elif user_input == "stop":
                print("the car has been stopped ")
            elif user_input == "start":
                print("the car has been started ")
            elif user_input == "cruise":
                print("you're cruising around town listening to LANY ")
            else:
                print("sorry, I do not understand ")


        code with already stopped and started

        user_input = ""
started = False
while user_input != "quit":
    user_input = input("> ").lower()
    if user_input == "quit":
        print("sorry to see you go ")
        break
    elif user_input == "help":
        print("""
start -- to start the car 
stop -- to stop the car
cruise -- to cruise around 
quit -- to exit """)
    elif user_input == "stop":
        if not started:
            print("the car is already stopped ")
        else:
            started = False
            print("the car has been stopped ")
    elif user_input == "stop":
        print("the car is already stopped ")
    elif user_input == "start":
        if started:
            print("the car is already started ")
        else:
            started = True
            print("the car has been started ")
    elif user_input == "cruise":
        print("you're cruising around town listening to LANY ")
    else:
        print("sorry, I do not understand ")


For loops

print [] = print lists

for item in ["Chris", "Nash", "Emma", "Son Ye-Jin"]:
    print(item)

range = object over numbers
range(10) = 0-9

range(5, 10, 2) = start, end, step


*** Let’s look at another example to get a better idea of how modulo is useful in programming:

print(3 % 3) # Prints 0
print(4 % 3) # Prints 1
print(5 % 3) # Prints 2
print(6 % 3) # Prints 0
print(7 % 3) # Prints 1

In each of these modulo operations, 3 is the divisor. Since 3 / 3 equals 1 with no remainder, the result of the first modulo operation is 0. Note that as the dividend increases by 1, the remainder also increases by 1, until we reach the next number that is evenly divisible by 3 — this creates a pattern that repeats contiuously as the dividend increases by 1!

Because of this, the modulo operator is useful in programming when we want to perform an action every nth time something occurs. Imagine you own a small café and would like for every 7th customer to receive a survey. If every customer transaction is numbered in the order they occur, you can determine which customers should receive the survey by calculating <transaction number> % 7 — if the result is 0, hand out the survey!


If you want to concatenate a string with a number you will need to make the number a string first, using the str() function. If you’re trying to print() a numeric variable you can use commas to pass it as a different argument rather than converting it to a string.

birthday_string = "I am "
age = 10
birthday_string_2 = " years old today!"

# Concatenating an integer with strings is possible if we turn the integer into a string first
full_birthday_string = birthday_string + str(age) + birthday_string_2

# Prints "I am 10 years old today!"
print(full_birthday_string)

# If we just want to print an integer 
# we can pass a variable as an argument to 
# print() regardless of whether 
# it is a string.

# This also prints "I am 10 years old today!"
print(birthday_string, age, birthday_string_2)

Using str() we can convert variables that are not strings to strings and then concatenate them. But we don’t need to convert a number to a string for it to be an argument to a print statement.


# for notes in python

True and False are their own special type: bool.

True and False are the only bool types, and any variable that is assigned one of these values is called a boolean variable.

Boolean variables can be created in several ways. The easiest way is to simply assign True or False to a variable:


## June 14th, 2024

what makes a programmer successful isn’t avoiding errors, it’s knowing how to solve them.


# Fortune Cookie Program 🥠

import random

fortune = random.randint(0, 4)

if fortune == 0:
  print("May you one day be carbon neutral")
elif fortune == 1:  
  print("You have rice in your teeth")
elif fortune == 2:
  print("No snowflake feels responsible for an avalanche")
elif fortune == 3:
  print("You can only connect the dots looking backwards")
elif fortune == 4:
  print("The fortune you seek is in another cookie")



We can even combine multiple data types in one list. For example, this list contains both a string and an integer:

mixed_list_string_number = ["Noelle", 61]

Lists can contain any data type in Python! For example, this list contains a string, integer, boolean, and float.

mixed_list_common = ["Mia", 27, False, 0.5]


create an empty list like this:

empty_list = []

Why would we create an empty list?

Usually, it’s because we’re planning on filling it up later based on some other input. We’ll talk about two ways of filling up a list in the next exercise


When we want to add multiple items to a list, we can use + to combine two lists (this is also known as concatenation).

Below, we have a list of items sold at a bakery called items_sold:

items_sold = ["cake", "cookie", "bread"]

Suppose the bakery wants to start selling "biscuit" and "tart":

items_sold_new = items_sold + ["biscuit", "tart"]
print(items_sold_new)
# Prints ['cake', 'cookie', 'bread', 'biscuit', 'tart']

In this example, we created a new variable, items_sold_new, which contained both the original items sold, and the new items. We can inspect the original items_sold and see that it did not change:

We can select a single element from a list by using square brackets ([]) and the index of the list item. If we wanted to select the third element from the list, we’d use calls[2]:

print(calls[2])



** We will need to modify the list to accommodate the change to our garden list. To change a value in a list, reassign the value using the specific index.

garden[2] = "Strawberries"

print(garden)

Will output:

["Tomatoes", "Green Beans", "Strawberries", "Grapes"]

Negative indices will work as well.

garden[-1] = "Raspberries"

print(garden)

Will output:

["Tomatoes", "Green Beans", "Strawberries", "Raspberries"]



\\We can remove elements in a list using the .remove() Python method.


recalling 2d lists 

#Your code below:
class_name_test = [["Jenny", 90], ["Alexus", 85.5], ["Sam", 83], ["Ellie", 101.5]]
print(class_name_test)
sams_score = class_name_test[2][1]

modifying 2d lists

We will need to modify the list to accommodate the change to our class_name_hobbies list. To change a value in a two-dimensional list, reassign the value using the specific index.

# The list of Jenny is at index 0. The hobby is at index 1. 
class_name_hobbies[0][1] = "Meditation"
print(class_name_hobbies)

print(sams_score)

To use the .remove() method on a two-dimensional list, call it on the sublist you are modifying and pass the value you want to remove in between the parenthesis ( ).

practice_list = [["a"], ["b"], ["c"]]
practice_list[1].remove("b")

print(practice_list)

  
