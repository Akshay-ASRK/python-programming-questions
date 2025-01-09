---
title: calendar_planner
tags: ['sample tag1', 'sample tag2']
---

# Problem Statement

Question 4: Problem Solving

Implement functions for a mini event management system:

event_handler(cal_ops: dict) : to handle operation.

add_event(calendar: dict, date: str, event: str) -> dict: Adds an event to the specified date.
 If the date already exists, append the event.

remove_event(calendar: dict, date: str, event: str) -> dict: Removes the event from the date. 
If no events remain on that date, delete the date key.

view_calendar(calendar: dict) -> dict: Returns the calendar sorted by date.

Input :

{"calender":{"date1":["event1","event2"]} "ops": [("add", "date3", "event1"), ("add", "date1", "event3"),("remove","date1","event2") ("view", )]}

Output:

{"date1": ["event1", "event3"],"date3" : ["event1"]}

# Solution
```python test.py  -r 'python test.py'
<prefix>

</prefix>
<template>
<sol> 
def add_event(calendar: dict, date: str, event: str) -> dict:
    if date not in calendar:
        calendar[date] = []
    calendar[date].append(event)
    return calendar

def remove_event(calendar: dict, date: str, event: str) -> dict:
    if date in calendar:
        calendar[date].remove(event)
        if not calendar[date]:
            del calendar[date]
    return calendar

def view_calendar(calendar: dict) -> dict:
    return dict(sorted(calendar.items()))

def event_handler(cal_ops: dict):
    Cal= cal_ops["calendar"]
    operations = cal_ops["ops"]
    for operation in operations:
        if operation[0] == "remove" :
            Cal = remove_event(Cal,operation[1],operation[2])
        elif operation[0] == "add" :
            Cal = add_event(Cal,operation[1],operation[2])
        elif operation[0] == "view" :
            return view_calendar(Cal)
        else :
            print("Wrong Input")
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
cal_ops = {"calendar" : {}, "ops": [("add", "2025-01-01", "New Year"), ("add", "2025-01-01", "Party"), ("view", )]}
```
## Output 1
```
(event_handler(cal_ops) == {"2025-01-01": ["New Year", "Party"]})
```
# Private Test Cases

## Input 1
```
cal_ops = {"calendar": {"2025-01-01": ["Meeting"]}, "ops": [("remove", "2025-01-01", "Meeting"), ("view", )]} 
```
## Output 1
```
(event_handler(cal_ops) == {})
```