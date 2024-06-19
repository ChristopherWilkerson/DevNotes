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


## June 15th, 2024

The .insert() method will handle shifting over elements and can be used with negative indices.

To see it in action let’s imagine we have a list representing a line at a store:

store_line = ["Karla", "Maxium", "Martim", "Isabella"]

"Maxium" saved a spot for his friend "Vikor" and we need to adjust the list to add him into the line right behind "Maxium".

For this example, we can assume that "Karla" is the front of the line and the rest of the elements are behind her.

Here is how we would use the .insert() method to insert "Vikor" :

store_line.insert(2, "Vikor")
print(store_line) 

Would output:

 ['Karla', 'Maxium', 'Vikor', 'Martim', 'Isabella']


Just as we learned to insert elements at specific indices, Python gives us a method to remove elements at a specific index using a method called .pop().

The .pop() method takes an optional single input:

    The index for the element you want to remove.


Python gives us an easy way of creating these types of lists using a built-in function called range().

The function range() takes a single input, and generates numbers starting at 0 and ending at the number before the input.

So, if we want the numbers from 0 through 9, we use range(10) because 10 is 1 greater than 9:

my_range = range(10)
print(my_range)

Would output:

range(0, 10)


Notice something different? The range() function is unique in that it creates a range object. It is not a typical list like the ones we have been working with.

In order to use this object as a list, we have to first convert it using another built-in function called list().

The list() function takes in a single input for the object you want to convert.

We use the list() function on our range object like this: 

print(list(my_range))

Would output:

[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]

Let’s try out using range()!

** len of list

long_list = [1, 5, 6, 7, -23, 69.5, True, "very", "long", "list", "that", "keeps", "going.", "Let's", "practice", "getting", "the", "length"]

big_range = range(2, 3000, 10)

# Your code below: 
long_list_len = len(long_list)
print(len(long_list))

big_range_length = len(big_range)
print(big_range_length)


In Python, often we want to extract only a portion of a list. Dividing a list in such a manner is referred to as slicing.

Lets assume we have a list of letters:

letters = ["a", "b", "c", "d", "e", "f", "g"]

Suppose we want to select from "b" through "f".

We can do this using the following syntax: letters[start:end], where:

    start is the index of the first element that we want to include in our selection. In this case, we want to start at "b", which has index 1.
    end is the index of one more than the last index that we want to include. The last element we want is "f", which has index 5, so end needs to be 6.

sliced_list = letters[1:6]
print(sliced_list)

Would output:

["b", "c", "d", "e", "f"]

Notice that the element at index 6 (which is "g") is not included in our selection.


Slicing Lists II
8 min

Slicing syntax in Python is very flexible. Let’s look at a few more problems we can tackle with slicing.

Take the list fruits as our example:

fruits = ["apple", "cherry", "pineapple", "orange", "mango"]

If we want to select the first n elements of a list, we could use the following code:

fruits[:n]

For our fruits list, suppose we wanted to slice the first three elements.

The following code would start slicing from index 0 and up to index 3. Note that the fruit at index 3 (orange) is not included in the results.

print(fruits[:3])

Would output:

['apple', 'cherry', 'pineapple']

We can do something similar when we want to slice the last n elements in a list:

fruits[-n:]

For our fruits list, suppose we wanted to slice the last two elements.

This code slices from the element at index -2 up through the last index.

print(fruits[-2:])

Would output:

['orange', 'mango']

Negative indices can also accomplish taking all but n last elements of a list.

fruits[:-n]

For our fruits example, suppose we wanted to slice all but the last element from the list.

This example starts counting from the 0 index up to the element at index -1.

print(fruits[:-1])

Would output:

['apple', 'cherry', 'pineapple', 'orange']

Let’s practice some of these extra slicing techniques!


Counting in a List
4 min

In Python, it is common to want to count occurrences of an item in a list.

Suppose we have a list called letters that represents the letters in the word “Mississippi”:

letters = ["m", "i", "s", "s", "i", "s", "s", "i", "p", "p", "i"]

If we want to know how many times i appears in this word, we can use the list method called .count():

num_i = letters.count("i")
print(num_i)

Would output:

4

Notice that since .count() returns a value, we can assign it to a variable to use it.

We can even use .count() to count element appearances in a two-dimensional list.

Let’s use the list number_collection as an example:

number_collection = [[100, 200], [100, 200], [475, 29], [34, 34]]

If we wanted to know how often the sublist [100, 200] appears:

num_pairs = number_collection.count([100, 200])
print(num_pairs)

Would output:

2

Let’s count some list items using the .count() method!



Sorting Lists I
7 min

Often, we will want to sort a list in either numerical (1, 2, 3, …) or alphabetical (a, b, c, …) order.

We can sort a list using the method .sort().

Suppose that we have a list of names:

names = ["Xander", "Buffy", "Angel", "Willow", "Giles"]

Let’s see what happens when we apply .sort():

names.sort()
print(names)

Would output:

['Angel', 'Buffy', 'Giles', 'Willow', 'Xander']

As we can see, the .sort() method sorted our list of names in alphabetical order.

.sort() also provides us the option to go in reverse. Instead of sorting in ascending order like we just saw, we can do so in descending order.

names.sort(reverse=True)
print(names)

Would output:

['Xander', 'Willow', 'Giles', 'Buffy', 'Angel']

Note: The .sort() method does not return any value and thus does not need to be assigned to a variable since it modifies the list directly. If we do assign the result of the method, it would assign the value of None to the variable.

Let’s experiment sorting various lists!



Sorting Lists II
3 min

A second way of sorting a list in Python is to use the built-in function sorted().

The sorted() function is different from the .sort() method in two ways:

    It comes before a list, instead of after as all built-in functions do.
    It generates a new list rather than modifying the one that already exists.

Let’s return to our list of names:

names = ["Xander", "Buffy", "Angel", "Willow", "Giles"]

Using sorted(), we can create a new list, called sorted_names:

sorted_names = sorted(names)
print(sorted_names)

This yields the list sorted alphabetically:

['Angel', 'Buffy', 'Giles', 'Willow', 'Xander']

Note that using sorted did not change names:

print(names)

Tuples

like a list but immutable

unpacking a tuple: 


my_info = ("Chris", 32, "Software Engineer")
print(my_info)
print(my_info[-1])
name, age, occupation = my_info
print(age)




Suppose that we already had a list of names and a list of heights:

names = ["Jenny", "Alexus", "Sam", "Grace"]
heights = [61, 70, 67, 64]

If we wanted to create a nested list that paired each name with a height, we could use the built-in function zip().

The zip() function takes two (or more) lists as inputs and returns an object that contains a list of pairs. Each pair contains one element from each of the inputs. This is how we would do it for our names and heights lists:

names_and_heights = zip(names, heights)

If we were to then examine this new variable names_and_heights, we would find it looks a bit strange: 


This zip object contains the location of this variable in our computer’s memory. Don’t worry though, it is fairly simple to convert this object into a useable list by using the built-in function list():

converted_list = list(names_and_heights)
print(converted_list)

Outputs:

[('Jenny', 61), ('Alexus', 70), ('Sam', 67), ('Grace', 64)]

For Loops: Introduction
8 min

Now that we can appreciate what loops do for us, let’s start with your first type of loop, a for loop, a type of definite iteration.

In a for loop, we will know in advance how many times the loop will need to iterate because we will be working on a collection with a predefined length. In our examples, we will be using Python lists as our collection of elements.

With for loops, on each iteration, we will be able to perform an action on each element of the collection.

Before we work with any collection, let’s examine the general structure of a for loop:

for <temporary variable> in <collection>:
  <action>

Let’s break down each of these components:

    A for keyword indicates the start of a for loop.
    A <temporary variable> that is used to represent the value of the element in the collection the loop is currently on.
    An in keyword separates the temporary variable from the collection used for iteration.
    A <collection> to loop over. In our examples, we will be using a list.
    An <action> to do anything on each iteration of the loop.

Let’s link these concepts back to our ingredients example. This for loop prints each ingredient in ingredients:

ingredients = ["milk", "sugar", "vanilla extract", "dough", "chocolate"]

for ingredient in ingredients:
  print(ingredient)

In this example:

    ingredient is the <temporary variable>.
    ingredients is our <collection>.
    print(ingredient) was the <action> performed on every iteration using the temporary variable of ingredient.

This code outputs:

milk
sugar
vanilla extract
dough
chocolate

Some things to note about for loops:

    Temporary Variables:

A temporary variable’s name is arbitrary and does not need to be defined beforehand. Both of the following code snippets do the exact same thing as our above example:

for i in ingredients:
   print(i)

for item in ingredients:
  print(item)

Programming best practices suggest we make our temporary variables as descriptive as possible. Since each iteration (step) of our loop is accessing an ingredient it makes more sense to call our temporary variable ingredient rather than i or item.

    Indentation:

    Notice that in all of these examples the print statement is indented. Everything at the same level of indentation after the for loop declaration is included in the loop body and is run on every iteration of the loop.

    for ingredient in ingredients:
      # Any code at this level of indentation 
      # will run on each iteration of the loop
      print(ingredient)

If we ever forget to indent, we’ll get an IndentationError or unexpected behavior.

    Elegant loops:

Python loves to help us write elegant code so it allows us to write simple for loops in one-line. In order to see the below example as one line, you may need to expand your narrative window. Here is the previous example in a single line:

for ingredient in ingredients: print(ingredient)

Note: One-line for loops are useful for simple programs. It is not recommended you write one-line loops for any loop that has to perform multiple complex actions on each iteration. Doing so will hurt the readability of your code and may ultimately lead to buggier code.

Let’s practice writing our own for loop!


## June 17th, 2024

While loops

While Loops: Introduction
17 min

In Python, for loops are not the only type of loops we can use. Another type of loop is called a while loop and is a form of indefinite iteration.

A while loop performs a set of instructions as long as a given condition is true.

The structure follows this pattern:

while <conditional statement>:
  <action>

Let’s examine this example, where we print the integers 0 through 3:

count = 0
while count <= 3:
  # Loop Body
  print(count)
  count += 1

Let’s break the loop down:

    count is initially defined with the value of 0. The conditional statement in the while loop is count <= 3, which is true at the initial iteration of the loop, so the loop body executes.

Inside the loop body, count is printed and then incremented by 1.

    When the first iteration of the loop has finished, Python returns to the top of the loop and checks the conditional again. After the first iteration, count would be equal to 1 so the conditional still evaluates to True and so the loop continues.

    This continues until the count variable becomes 4. At that point, when the conditional is tested it will no longer be True and the loop will stop.

The output would be:

0
1
2
3

Note the following about while loops before we write our own:

Loops
Loop Control: Continue
7 min

While the break control statement will come in handy, there are other situations where we don’t want to end the loop entirely. What if we only want to skip the current iteration of the loop?

Let’s take this list of integers as our example:

big_number_list = [1, 2, -1, 4, -5, 5, 2, -9]

What if we want to print out all of the numbers in a list, but only if they are positive integers. We can use another common loop control statement called continue.

for i in big_number_list:
  if i <= 0:
    continue
  print(i)

This would produce the output:

1
2
4
5
2

Notice a few things:

    Similar to when we were using the break control statement, our continue control statement is usually paired with some form of a conditional (if/elif/else).
    When our loop first encountered an element (-1) that met the conditions of the if statement, it checked the code inside the block and saw the continue. When the loop then encounters a continue statement it immediately skips the current iteration and moves onto the next element in the list (4).
    The output of the list only printed positive integers in the list because every time our loop entered the if statement and saw the continue statement it simply moved to the next iteration of the list and thus never reached the print statement.



Loops
Nested Loops
12 min

Loops can be nested in Python, as they can with other programming languages. We will find certain situations that require nested loops.

Suppose we are in charge of a science class, that is split into three project teams:

project_teams = [["Ava", "Samantha", "James"], ["Lucille", "Zed"], ["Edgar", "Gabriel"]]

Using a for or while loop can be useful here to get each team:

for team in project_teams:
  print(team)

Would output:

["Ava", "Samantha", "James"]
["Lucille", "Zed"]
["Edgar", "Gabriel"]

But what if we wanted to print each individual student? In this case, we would actually need to nest our loops to be able to loop through each sub-list. Here is what it would look like:

# Loop through each sublist
for team in project_teams:
  # Loop elements in each sublist
  for student in team:
    print(student)

This would output:

Ava
Samantha
James
Lucille
Zed
Edgar
Gabriel

Let’s practice writing a nested loop!


My Home
Loops: List Comprehensions: Introduction
Narrative and Instructions
Learn
Loops
List Comprehensions: Introduction
8 min

So far we have seen many of the ideas about using loops in our code. Python prides itself on allowing programmers to write clean and elegant code. We have already seen this with Python giving us the ability to write while and for loops in a single line.

In this exercise, we are going to examine another way we can write elegant loops in our programs using list comprehensions.

To start, let’s say we had a list of integers and wanted to create a list where each element is doubled. We could accomplish this using a for loop and a new list called doubled:

numbers = [2, -1, 79, 33, -45]
doubled = []

for number in numbers:
  doubled.append(number * 2)

print(doubled)

Would output:

[4, -2, 158, 66, -90]

Let’s see how we can use the power of list comprehensions to solve these types of problems in one line. Here is our same problem but now written as a list comprehension:

numbers = [2, -1, 79, 33, -45]
doubled = [num * 2 for num in numbers]
print(doubled)

Let’s break down our example in a more general way:

new_list = [<expression> for <element> in <collection>]

In our doubled example, our list comprehension:

    Takes an element in the list numbers
    Assigns that element to a variable called num (our <element>)
    Applies the <expression> on the element stored in num and adds the result to a new list called doubled
    Repeats steps 1-3 for every other element in the numbers list (our <collection>)

Our result would be the same:

[4, -2, 158, 66, -90]


add 10 to grade list example

grades = [90, 88, 62, 76, 74, 89, 48, 57]
scaled_grades = [grade + 10 for grade in grades]
print(scaled_grades)

Here are a few list comprehensions in a single block. Take a moment to compare how the syntax must change depending on whether or not an else clause is included:

numbers = [2, -1, 79, 33, -45]

no_if   = [num * 2 for num in numbers]
if_only = [num * 2 for num in numbers if num < 0]
if_else = [num * 2 if num < 0 else num * 3 for num in numbers]

Now, let’s write our own list comprehensions with conditionals! 



## June 18th, 2024

Functions 

Introduction to Functions
Defining a Function
7 min

A function consists of many parts, so let’s first get familiar with its core - a function definition.

Here’s an example of a function definition:

def function_name():
  # functions tasks go here

There are some key components we want to note here:

    The def keyword indicates the beginning of a function (also known as a function header). The function header is followed by a name in snake_case format that describes the task the function performs. It’s best practice to give your functions a descriptive yet concise name.

    Following the function name is a pair of parenthesis ( ) that can hold input values known as parameters (more on parameters later in the lesson!). In this example function, we have no parameters.

    A colon : to mark the end of the function header.

    Lastly, we have one or more valid python statements that make up the function body (where we have our python comment).

Notice we’ve indented our # function tasks go here comment. Like loops and conditionals, code inside a function must be indented to show that they are part of the function.


My Home
Introduction to Functions: Calling a Function
Narrative and Instructions
Learn
Introduction to Functions
Calling a Function
2 min

Now that we’ve practiced defining a function, let’s learn about calling a function to execute the code within its body.

The process of executing the code inside the body of a function is known as calling it (This is also known as “executing a function”). To call a function in Python, type out its name followed by parentheses ( ).

Let’s revisit our directions_to_timesSq() function :

def directions_to_timesSq():
  print("Walk 4 mins to 34th St Herald Square train station.")
  print("Take the Northbound N, Q, R, or W train 1 stop.")
  print("Get off the Times Square 42nd Street stop.")

To call our function, we must type out the function’s name followed by a pair of parentheses and no indentation:

directions_to_timesSq()

Calling the function will execute the print statements within the body (from the top statement to the bottom statement) and result in the following output:

Walk 4 mins to 34th St Herald Square train station.
Take the Northbound N, Q, R, or W train 1 stop.
Get off the Times Square 42nd Street stop.

Note that you can only call a function after it has been defined in your code.

Now it’s your turn to call a function!
Instructions

    Checkpoint 1 Passed

    1.

    Call the directions_to_timesSq() function.

    Click Run to see it execute and print out.

Checkpoint 2 Passed

2.

Add an additional print statement to our directions_to_timesSq() function.

Have the statement print "Take lots of pictures!"

Run your code again and see how your output changes.

## simple function plane trip total python example 

def calculate_expenses(plane_ticket_price, car_rental_rate, hotel_rate, trip_time):
  car_rental_total = car_rental_rate * trip_time
  hotel_total = hotel_rate * trip_time - 10
  trip_total = car_rental_total + hotel_total + plane_ticket_price
  return trip_total
print(calculate_expenses(200, 100, 100, 5))

Introduction to Functions
Variable Access
7 min

As we expand our programs with more functions, we might start to ponder, where exactly do we have access to our variables? To examine this, let’s revisit a modified version of the first function we built out together:

def trip_welcome(destination):
  print(" Looks like you're going to the " + destination + " today. ")

What if we wanted to access the variable destination outside of the function? Could we use it? Take a second to think about what the following program will output, then check the result below!

def trip_welcome(destination):
  print(" Looks like you're going to the " + destination + " today. ")

print(destination)

Output Results

NameError: name 'destination' is not defined

If we try to run this code, we will get a NameError, telling us that destination is not defined. The variable destination has only been defined inside the space of a function, so it does not exist outside the function.

We call the part of a program where destination can be accessed its scope. The scope of destination is only inside the trip_welcome(). 


Narrative and Instructions
Learn
Introduction to Functions
Returns
13 min

At this point, our functions have been using print() to help us visualize the output in our interpreter. Functions can also return a value to the program so that this value can be modified or used later. We use the Python keyword return to do this.

Here’s an example of a program that will return a converted currency for a given location a user may want to visit in our trip planner application.

def calculate_exchange_usd(us_dollars, exchange_rate):
  return us_dollars * exchange_rate

new_zealand_exchange = calculate_exchange_usd(100, 1.4)

print("100 dollars in US currency would give you " + str(new_zealand_exchange) + " New Zealand dollars")

This would output:

100 dollars in US currency would give you 140 New Zealand dollars

Saving our values returned from a function like we did with new_zealand_exchange allows us to reuse the value (in the form of a variable) throughout the rest of the program. 






