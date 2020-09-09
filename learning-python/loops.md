# Loops ( loop back and check if all conditions are met)

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

