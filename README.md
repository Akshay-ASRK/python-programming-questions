# python-programming-questions
---
title: filter_even_numbers
---

# Problem Statement

Question 3: Data Processing I/O
 
Write a function filter_even_numbers that:
Takes a list of integers as input from stdin.
Prints the sorted list of even integers to stdout.

# Solution
```python test.py  -r 'python test.py'
<prefix>

</prefix>
<template>
<sol> 
def filter_even_numbers():
    import sys
    nums = list(map(int, sys.stdin.readline().strip().split()))
    evens = sorted([num for num in nums if num % 2 == 0])
    print(" ".join(map(str, evens)))
</sol>
</template>
<suffix>

</suffix>
<suffix_invisible>

</suffix_invisible>
```

# Public Test Cases
## Input 1
```
10 15 8 7 12
```
## Output 1
```
(filter_even_numbers() == 8 10 12)
```
# Private Test Cases
## Input 1
```
3 5 2 8 1 0
```
## Output 1
```
(filter_even_numbers() == 0 2 8)
```
