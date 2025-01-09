---
title: process_scores
tags: ['sample tag1', 'sample tag2']
---

# Problem Statement

Question 2: Data Processing

Implement a function process_scores(scores: list of dictionary) -> dict that takes a list of dictionaries containing scores in different subjects. 

Each dictionary is structured like:
```
{"name": str, "math": int, "science": int, "english": int}
```
Output :
sorted average marks, student dictionary 
{'name': 44,'name2':76}

Your function should:
Map each students name to their average score across all subjects.
Return a dictionary with sorted names (keys) and their average scores (values).

# Solution
```python test.py  -r 'python test.py'
<prefix>

</prefix>
<template>
<sol> 
def process_scores(scores: list) -> dict:
    averages = {student["name"]: sum([student["math"], student["science"], student["english"]]) / 3 for student in scores}
    return dict(sorted(averages.items()))
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
scores = [  {"name": "Alice", "math": 90, "science": 80, "english": 70},
            {"name": "Bob", "math": 85, "science": 90, "english": 95}] 
```
## Output 1
```
(process_scores(scores) ==  {"Alice": 80.0, "Bob": 90.0})
```
# Private Test Cases

## Input 1
```
scores = [{"name": "Charlie", "math": 60, "science": 70, "english": 80}, 
            {"name": "Diana", "math": 100, "science": 90, "english": 85}]
```
## Output 1
```
(process_scores(scores) == {"Charlie": 70.0, "Diana": 91.66666666666667})
```