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

