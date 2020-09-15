---
layout: default
name: Lists in Python
nav_order: 3
---

# Lists

Lists represent ordered sequences of values. We have already seen an example of a list.

```python
primes = [2, 3, 5, 7]
```

Lists doesn't have to always contain numbers. It can also contain strings or a mixture of numbers and strings.

```python
planets = ['Mercury', 'Venus', 'Earth', 'Mars', 'Jupiter', 'Saturn', 'Uranus', 'Neptune']
random = [1, 2, 3, 'how', 'are', 'you']
```

## Indexing

Now, how to access individual list elements. Identifying individual items in the list is called *indexing*. We use [] with the position number between the []. It will look like this.

```python
primes[0]
primes[3]
```
output will be '2' and '7', respectively. Note the position numbering within the list starts from zero and not one. So, in primes, the number in position 0 is 2, 1 is 3, 2 is 5 and 3 is 7. Makes sense?

What if we don't know how many items are in the list? How do we access the last item or last but one item? We can use this. Here, -1 will retrieve the last item 7, and -2 will retrieve the last but one item 5.

```python
primes[-1]
primes[-2]
```

## Slicing

Next, we will try to retrieve a group of items from the list. This is called *slicing*. We can slice the list from the beginning or from the end. For the first 2 items retrival, we can use one of the 2 options - both will provide the same answer 2, 3. primes[0:2] or [:2] is our way of asking for the elements of primes starting from index 0 and continuing up to but not including index 2.

```python
primes[0:2]
prime[:2]
```
We can also use negative values to do slicing. For eg. the below code will provide 3, 5 (elements of primes starting from index 1 and continuing up to but not including index -1.

```python
primes[1:-1]
```
Alternatively, the following code means starting from position -3, ends with -1. The output will be 3, 5, 7.

```python
primes[-3:]
```

## Changing lists

We can change individual elements in a list if we know the position. prime[1] is infact 3. Let's give a new number now. Now, the list will become [2, 10, 5, 7]

```python
prime[1] = 10
```

We can also use the colon function here. Let's try for the first 2 elements and change it. And the elements 2 and 3 of the original set will be changed to 20 and 30 respectively.

```python
prime[:2] = 20, 30]
```

## List functions

We have learnt about functions in our previous module. Lets use them in the context of lists. There are several pre-defined functions in Python that can be useful for simple data analysis. 

For finding the length of the list, use the code below. Answer will be 4.

```python
len(primes)
```

For displaying a sorted version of the list, use the code below. This code is most suitable for unsorted lists (both numbers and strings).

```python
sorted(primes)
```

For finding the sum of the list, use the code below. Answer will be 17.

```python
sum(primes)
```

We can also use `<max>` and `<min>` for finding the maximum and minimum element within the list. Here it is 2 and 7, respectively.

```python
max(primes)
min(primes)
```

## List methods


