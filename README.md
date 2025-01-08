# python-programming-questions

Question 1: Data Types
title: Type Based Output
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


Question 2: Data Processing
title: process_scores

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


Question 3: Data Processing I/O
title: filter_even_numbers

Write a function filter_even_numbers that:
Takes a list of integers as input from stdin.
Prints the sorted list of even integers to stdout.


Question 4: Problem Solving
title: calendar_planner

Implement functions for a mini event management system:
1) event_handler(cal_ops: dict) : to handle operation.
2) add_event(calendar: dict, date: str, event: str) -> dict: Adds an event to the specified date.If the date already exists, append the event.
3)remove_event(calendar: dict, date: str, event: str) -> dict: Removes the event from the date. If no events remain on that date, delete the date key.
4)view_calendar(calendar: dict) -> dict: Returns the calendar sorted by date.
Input :
{"calender":{"date1":["event1","event2"]} "ops": [("add", "date3", "event1"), ("add", "date1", "event3"),("remove","date1","event2") ("view", )]}
Output:
{"date1": ["event1", "event3"],"date3" : ["event1"]}



[Ques_1.md](https://github.com/user-attachments/files/18350809/Ques_1.md)
[Ques_2.md](https://github.com/user-attachments/files/18350810/Ques_2.md)
[Ques_3.md](https://github.com/user-attachments/files/18350811/Ques_3.md)
[Ques_4.md](https://github.com/user-attachments/files/18350812/Ques_4.md)
