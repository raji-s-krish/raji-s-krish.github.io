---
layout: default
title: Learning Python
nav_order: 2
---


# Learning Python

## Introduction

Let’s start from the basics.

Python is a programming language. What is a programming language? Programming language is a vocabulary and set of grammatical rules for instructing a computing device to perform specific tasks. There are so many programming languages - Python, Java, Ruby/Ruby on Rails, HTML, JavaScript, C Language, C++ - Python is obviously one among them.


Why we use Python at Qure? Python is a more popular language for AI because Python is easy to learn and implement. With its many libraries, they can also be used for data analysis (most relevant for clinical research and statistical analysis at Qure).


If you are starting to learn programming for the first time (absolute beginners), and using this [link](https://folk.idi.ntnu.no/mlh/hetland_org/writing/instant-hacking.html) to learn it, start typing all the codes. The first day and probably for the first week (I might edit this later as it’s my second day at coding), you will have all sorts of syntax error due to mistakes in spacing, indentation, etc., But keep at it, will get better.


First, if you are using a Mac, Python is inbuilt - access it via TERMINAL (you might have never used this in Mac before). If you are using a Windows, Python has to be downloaded. For Mac, open TERMINAL, type ‘python’, press enter.


Second, you will also need a text editor (a software that helps you type the code more easily); here, I will be using Visual Studio Code. Once Visual Studio Code is set up, create a New file as learning.py or anyother.py in your home 🏠 folder. Although, for simple code, you can use the TERMINAL, I am going to use Visual Studio Code from the start.

## Basics

Given that, let’s get to the actual programming,

Let’s start with a very simple command, “print”. 


Type exactly the following in your new ‘learning.py’ file in Visual Studio Code, pay attention to space & quotations. 


print “Hello, world!” 

```python
print "Hello, world!" 
```

The typing will look like 👆.


Copy this and paste it in TERMINAL, press enter. Now you have your command executed like below. Awesome!

```python
print "Hello, world!" 
Hello, world!
```


Let’s try one more.

```python
print "Goodbye, world!"
Goodbye, world!
```

Great!

Now let’s learn about the 3 building blocks of programming

Sequential execution (one command after the other)

Conditionals (if this → do this, else → do this)

Loop (still figuring this out 😒)

Why do we have to start with these building blocks? These are fundamentals for programming and more importantly, (through examples) we can get started on some fundamental coding principles/methods/commands, etc.,

## Sequential execution (one command after the other)

First, let’s start with a simple area calculation. We all know this (Area of circle = π*r^2; Area of a rectangle = length*width; Area of square = side^2). Before going into the sequential execution, let’s calculate an area first - how do we tell the computer that? Here is how. (Type in VS Code, copy paste in Terminal and you will get the following). ⚠️ pay attention to spacing.

```python
>>> length = 20
>>> width = 30
>>> area = length*width
>>> print area
600
```

What do we learn here?

when ‘=’ is used, a value is assigned to the variable. These are called assignments. Here, length takes up a value of 20, width takes up a value of 30, area takes up the value of length*width.

Python runs commands one line after the other. So we cannot do this 👇, try it.

```python
area = length*width
length = 20
width = 30
print area
```

So, that is our sequential execution.

## Conditionals (if this → do this, else → do this)

For this let’s use a simple example first, then we will go back to our Area problem. Below is the code.

```python
temperature = input("What is the temperature?")
if temperature > 50:
    print "Too hot"
else:
    print "Not too hot"
```

What do we learn here?

1. the term input - it is something called a function. You can add a number, text, string, etc., inside a parentheses () next to input . What goes inside the () is the parameter. The input function tells the user ‘what to do’. In this case, input tells/asks the user “what is the temperature?”.

2. in sequential execution example, we gave the values. Here we are learning how to ask the user to give us the values.

3. if and else is the conditional term, I guess. With an if, you can enter the first condition, insert a colon: Everything after this colon is called scope. Scope is the instructions for the computer. It can be a single line like above print "too hot". OR it can be two lines like below. Both commands will be executed.

```python
temperature = input("What is the temperature?")
if temperature > 50:
    print "Too hot"
    print "oh no!"
```

With an else, the alternate condition will be met.

Important: Did you notice the indentation before print? In VSCode, when a colon is typed, automatically an indentation is created in the next line. An indentation is required for this command to run.

another small tip, I tried >=50 to try more than and equal to 50, it works.

```python
temperature = input("What is the temperature?")
if temperature >= 50:
    print "Too hot"
else:
    print "Not too hot"
```

another experiment and tip. For the condition that temperature equals (not greater than) to 50, what do you do? do you say, temperature = 50? ❌❌❌. Remember what I said about ‘=’ in previous point? Go back and read again. ‘=’ assigns a value to a variable. Since it is a condition, so we use ‘==’ in this case. Only for a temperature of 50, the answer will be ‘Too hot’.

```python
temperature = input("What is the temperature?")
if temperature == 50:
    print "Too hot"
else:
    print "Not too hot"
```

Second example for conditionals: Let’s do an area problem and insert 3 conditions (not just 2 conditions like the previous one). We only have ‘if’ and ‘else’. How can we include 3 conditions then? We use ‘elif’.

```python
print "Welcome to the Area calculation program"
print "---------------------------------------"
print

# Print out the menu:
print "Please select a shape:"
print "1  Rectangle"
print "2  Circle"
print "3  Square"

# Get the user's choice:
shape = input("> ")

# Calculate the area:
if shape == 1:
    height = input("Please enter the height: ")
    width = input("Please enter the width: ")
    area = height*width
    print "The area is", area
elif shape == 2:
    radius = input("Please enter the radius: ")
    area = 3.14*(radius**2)
    print "The area is", area
else:
    side = input("Please enter the side: ")
    area = side**2
    print "The area is", area
```

What do we learn here?

We can ‘print’ many text, lines, blank space using ‘print’ to make it user friendly. In this case, the output of first 3 lines is

```python
Welcome to the Area calculation program
--------------------------------------
```

We can use # to insert a comment, so a person who is reading the code understands what exactly you are doing, what is the code for, etc.,

‘elif’ is between if and else, so it can be just one ‘elif’ or many ‘elif’s depending on the number of conditions we have.

There are 3 commands/scope after the conditions if or elif or else. 1) instructions for user 2) formula for calculation 3) output.

## Loops ( loop back and check if all conditions are met)

Loop is a programming structure that repeats a sequence of instructions until a specific condition is met. Loops are used to cycle through values, add sums of numbers, repeat functions, and many other things.

There are two major loops - for and while

Let’s start with for

for loops can iterate over a given sequence. The output will print out 2,3,5,7. The for command loops back each time to print the sequence of number within [].

```python
primes = [2, 3, 5, 7]
for prime in primes:
    print(prime)
```

Another example for for. It can iterate over a sequence of numbers using the "range"

```python
# Prints out the numbers 0,1,2,3,4
for x in range(5):
    print(x)

# Prints out 3,4,5
for x in range(3, 6):
    print(x)

# Prints out 3,5,7
for x in range(3, 8, 2):
    print(x)

Yet another example for for. The output also is included.

for number in range(1,5):
    print "Hello, world!"
    print "Just", 5 - number, "more to go..."

print "Hello, world"
print "That was the last one... Phew!"

# Output
Hello, world!
Just 4 more to go...
Hello, world!
Just 3 more to go...
Hello, world!
Just 2 more to go...
Hello, world!
Just 1 more to go...
Hello, world
That was the last one... Phew!
```

What do we learn here?

for  is a function which is always followed by  in  and the variable is present in between for and in . The variables in the above examples are prime, x and number. Don’t forge the colon at the end.

For the loops (i.e. what values are looped) can be given by us, as in first eg. [2, 3, 5, 7] or we can use the function range. The function range returns a list of numbers in the range given (including the first, excluding the second, using the third as the difference).

In the last example, the sequence of events are like this: first,  print  ‘Hello world’, next, subtract all numbers in range i.e. 1,2,3,4 from 5, one by one until it reaches 5 - 4 = 1 is reached (Last output is ‘Just 1 more to go’ and then, go to the last 2 print command i.e. “Hello world” and “That was the last one… Phew!”

Let’s move on to while

While loops repeat as long as a certain boolean condition is met.

```python
count = 0
while count < 5:
    print(count)
    count += 1 
```

count +=1 is same as count = count + 1. Try it. What happens here is count is assigned a value of zero. Then, until count is less than 5, print count. Next count is printed (which is zero). For every next step, 1 will be added to the zero. So, the output will be this below.

```python
0
1
2
3
4
```

Another, a little more complex example. Here, we will use an example of a salad. We plan to instruct the computer to cook the pizza, check in between if it’s ready, then give instructions to continue or not to continue cooking a pizza. To account for the time factor here, we use function sleep that can be imported from a module time.So anything that goes inside the () after sleep  will be the number of seconds that the computer will continue cooking the pizza. Here the output will be pizza cooks for 3 minutes then checks with the user what is the temperature; if it is < 50, then the pizza cooks 30 more seconds. Until a temperature of 50 is reached, this command keeps looping.

```python
# Pizza-cooking program

# Fetch the function *sleep*
from time import sleep

print "Please start cooking the pizza. (I'll be back in 3 minutes.)"

# Wait for 3 minutes (that is, 3*60 seconds)...
sleep(180)

print "I'm baaack :)"

# How hot is hot enough?
hot_enough = 50

temperature = input("How hot is the spam? ")
while temperature < hot_enough:
    print "Not hot enough... Cook it a bit more..."
    sleep(30)
    temperature = input("OK. How hot is it now? ")

print "It's hot enough - You're done!"
```

## Abstraction (will update this later)

What is abstraction? Abstraction in Python is the process of hiding the real implementation of an application from the user and emphasising only on usage of it. Example, when you use TV remote, you do not know how pressing a key in the remote changes the channel internally on the TV. You just know that pressing + volume key will increase the volume. You don’t have to know how remote works internally, yet you can still use remote perfectly fine.

## Functions

Let’s do functions now. Here are the different definitions of functions that I found.

A function is a block of organized, reusable code that is used to perform a single, related action.

A function is a collection of instructions or a collection of codes.

So, instead or writing a code one by one each time, we can group a bunch of codes together and give a name to it (on our own). A classic example will be a formula, such as BMI (we will talk about this in an exercise below).

To create a function, command def is used. Let’s start with a simple function. Couple of things here:

here ‘qure’ is the name of the function that I have assigned.

I don’t give an argument to this function hence the paranthesis is empty

a colon should follow the paranthesis

indentation for the instructional codes

if no indentation, then that code will not be part of the function.

```python
def qure():
    print("AI")
    print("HeadCT")
print("this does not apply to qure")
```

If you run this code above, the output will be this does not apply to qure. So what happened to the function codes (i.e. print (“AI”) and print(“HeadCT”))? These code were not processed because there is one essential step that needs to be done before we get an output for a function. And that is ‘calling the function’. How do we call the function? Like this below. Now run this and you will see the results.

```python
def qure():
    print("AI")
    print("HeadCT")
print("this does not apply to qure")
qure()
```

The next step is now to include an argument to a function. And this is called ‘mapping’. Let’s start with x that goes inside the parentheses. Here, when we have an argument, we can include a return command to give an output for this function with an argument.

```python
def function(x):
    return 2*x
```

Now, to call this function (with an argument), we assign this function to a variable say a or b. Then, we print that variable to see the results.

```python
a = function(3)
print(a)
b = function(4)
print(b) 
```

Now, can we have an argument, but not use return to have an output? Yes. Now, the output will be not a processed output like in the previous example but just the print of the argument, i.e. 9 and then “Hello, world”.

```python
def function(argument):
    print(argument)
    print("Hello,world!")
function(9)
```

Let’s move on. Can we add two arguments in a function? Yes, absolutely. If a function cannot take more than one argument, how can we use a function for processing a formula which almost always has more than a variable (e.g addition needs two numbers). Couple of things here:

Multiple arguments are separated by , and space within the parentheses.

When we assign the function (with multiple arguments) to a variable, we use the same pattern of , to provide values of the argument.

```python
def addition(x, y):
    return x + y
c = addition(3, 5)  
print(c)
```
### Exercise 1

Let’s try a simple exercise. Creating a function to convert miles to km. (1 mile = 1.6 km).

```python
#Exercise 1

def km(miles):
    return miles*1.6

#call the function
e = km(33)
print(e)
```

### Exercise 2

Let’s try a more complicated problem. Here we set up a formula first with 2 different cases and then include if else condition within the function.

create a function to calculate BMI

create 2 cases

determine if each of the 2 cases is overweight or not

```python
#Exercise 2
name1 = "RS"
height1 = 1.6
weight1 = 60

name2 = "CS"
height2 = 1.8
weight2 = 90

def bmi_calculator(name, height, weight):
    bmi = weight / (height ** 2)
    print("bmi: ")
    print(bmi)
    if bmi < 25:
        return name + " is not overweight"
    else:
        return name + " is overweight"

#call the function
result1 = bmi_calculator(name1, height1, weight1)
result2 = bmi_calculator(name2, height2, weight2)

#print output
print(result1)
print(result2)
```

The output will look something like this.

```python
bmi:
23.4375
bmi:
27.7777777778
RS is not overweight
CS is overweight
```

A point to note here under return we have name + “ is not overweight”. The two can be combined because both are string variable. In Python, when + is used, it simply puts the two strings on either side together. In the example (see the above output), ‘RS is not overweight” is simply place side by side. The space between RS and is created by the space between “ and is in “ is not overweight”. This + sign will not work if one is a number and one is a string. For eg. return 5 + “ is not overweight”
