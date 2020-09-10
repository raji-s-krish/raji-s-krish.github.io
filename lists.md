---
name: Lists
layout: default
nav_order: 4
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

Now, how to access individual list elements. We use [] with the position number between the []. It will look like this.

```python
primes[0]
primes[3]
```
output will be '2' and '7', respectively. Note the position numbering within the list starts from zero and not one. So, in primes, the number in position 0 is 2, 1 is 3, 2 is 5 and 3 is 7. Makes sense?


