
# Python Conditional Statements
Often, we only want code to be executed if a certain condition is met. Just like in JavaScript, we can use conditional statements to help control the flow of our program.

## Objectives:
+ Write conditional statement syntax
+ Use each statement type in the appropriate context
+ Evaluate boolean expressions

##Multi-line Code in Python
The easiest way to follow along with these multi-line Python examples is by creating a new .py file and running your script through the command line.
```
touch conditionals.py
open conditionals.py -a "Atom"
# write your code in conditionals.py and then run it with the python command below.
python conditionals.py
```

Alternatively, you can still use the Python console, but for multiline commands, you will need to use tab to indent where appropriate and press enter twice! In the example below you'd type the if statement and press `Enter`. Next, press `tab` to type the code block (in this case the `print` statement). After typing the code block, hit enter. Finally, you'll need to hit enter again after the second set of ellipses. All of this is to say that writing your *python code in a text editor is a lot simpler!*

```
>>> number_of_lines = 2
>>>if number_of_lines > 1: 
... print "you have to use tab and press enter twice"
... 
```
## If Statements
Conditional statements are a type of control flow. They can control which parts of code get executed, and which do not. The basic conditional statement is the if statement:
```
if condition_1:
    run this block of code
```

Note the syntax here. The condition ends with a colon and the block of code is indented.
Let's use an example where we ask the user for their favorite animal. In Python, this can be achieved using the `raw_input()` function (Python 2) or the `input()` function (Python 3).

```
yourAnimal = input('What is your favorite animal?')
myAnimal = "dog"

if yourAnimal == myAnimal:
  print "That's my favorite animal, too!"
```
###The Comparison Operator

Just like in JavaScript, a single equals sign and double equals sign mean two different things.
  + "==" checks for equality: "are these two things equal?".
  + "=" is used for variable assignment: "set variable x equal to 10."

When we check for equality in conditionals, make sure to **use the double equal sign.**

### Boolean Values
Python has Boolean values as well: False and True. Booleans can be assigned to variables.
For example:
```
x = (3 == 5)
print x
>>> False
```
First, we calculate (3 == 5). This is a question: "Is 3 equal to 5?". The answer to that question is False: 3 is not equal to 5.

So, when we say x = (3==5), this is equivalent to x = False. We're setting X to the boolean value False. Now when we print x, we see that "False" is printed on the screen.

Here are some important boolean operators:
<img src= "images/boolean_table.png">

## If/Else Conditional Statement
There are a few other conditional statements that work together with `if`. For example, you often want to do something if the condition is not met:
```
yourAnimal = input('What is your favorite animal? ')
myAnimal = "dog"
if yourAnimal == myAnimal:
  print "That's my favorite animal, too!"
else:
  print "I don't think you understand how cool dogs are."
```
An "else" clause will always follow an "if" clause, because "else" means "otherwise."

## Statements Using the Elif Clause
Where JavaScript has "else if" (and Ruby has "elsif"), Python has `elif`. This allows multiple conditions to be checked. When a condition is met, the code block underneath it is executed and we exit the conditional statement (we call this lazy evaluation).
```
x = 25

if x > 500:
  print "x is really big"
elif x > 50:
  print "x is sort of big"
elif x > 0:
  print "x is not very big!"
else:
  print "x is negative"

=> "x is sort of big"
```

## Conclusion
Flow Control is an important part of any programming language and Python is no exception. As you practice writing conditional statements in Python, be careful with your syntax use - it's easy to get confused once you've seen a bunch of languages. However, the general concepts are the same and you can use your insights from JavaScript conditional statements to help work though the next lab.

Some criteria to help decide which condition to use:
+ If - one condition, specifies what to do if condition is True
+ If/Else - one condition, specifies what to do if condition is True OR False
+ Elif - more than one condition
