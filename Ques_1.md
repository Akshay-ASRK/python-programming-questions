---
title: Type Based Output
tags: ['sample tag1', 'sample tag2']
---

# Problem Statement

Question 1: Data Types

Implement a function data_operations(variable) that takes input:
    1 : An integer .
    2 : A floating-point number.
    3 : A string .
    4 : A list .
    5 : A dictionary e where keys are strings and values are integers.
    6 : A set.
The function should perform the following do operation on varible:
    1 : Multiply the integer a by 2 and return the result.
    2 : Add 5.5 to the float b and return the result.
    3 : Return the uppercase version of the string c.
    4 : Append the integer 10 to the list d and return it.
    5 : Add a new key-value pair {"extra": 100} to the dictionary e and return it.
    6 : Add the value 99 to the set f and return it.

Return the result as mentioned above.


# Solution
```python test.py  -r 'python test.py'
<prefix>

</prefix>
<template>
<sol> 
def data_operations(variable):
    typo = type(variable).__name__
    match typo:
        case int :
            return variable * 2
        case float:
            return variable + 5.5
        case str:
            return variable.upper()
        case list:
            return variable + [10]
        case dict :
            return {**variable, "extra": 100}
        case set :
            return variable | {99}
        case default:
            return "Wrong Input"

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
4 
```
## Output 1
```
(data_operations(variable) == 8)
```
## Input 2
```
2.5
```
## Output 2
```
(data_operations(variable) == 8.0)
```
## Input 3
```
"hello"
```
## Output 3
```
(data_operations(variable) == "HELLO")
```
## Input 4
```
[1, 2]
```
## Output 4
```
(data_operations(variable) == [1, 2, 10])
```
## Input 5
```
{"key1": 1}
```
## Output 5
```
(data_operations(variable) == {"key1": 1, "extra": 100})
```
## Input 6
```
{1, 2, 3}
```
## Output 6
```
(data_operations(variable) == {1, 2, 3, 99})
```
# Private Test Cases

## Input 1
```
0 
```
## Output 1
```
(data_operations(variable) == 0)
```
## Input 2
```
-1.5
```
## Output 2
```
(data_operations(variable) == 4.0)
```
## Input 3
```
"world"
```
## Output 3

```
(data_operations(variable) == "WORLD")
```
## Input 4
```
[]
```
## Output 4

```
(data_operations(variable) == [10])
```
## Input 5
```
{}
```
## Output 5
```
(data_operations(variable) == {"extra": 100})
```
## Input 6

```
set()
```
## Output 6
```
(data_operations(variable) == {99})
```