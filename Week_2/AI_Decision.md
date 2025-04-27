# Lesson 6 - Helping AI Make Decisions

```python
from helper_functions import print_llm_response
```

## Performing Tasks Depending on Their Time to Completion

Let's say you have a task list with tasks that LLMs could assist you with. Each element is a dictionary with two keys: `description` and `time_to_complete`.

```python
task_list = [
    {
        "description": "Compose a brief email to my boss explaining that I will be late for next week's meeting.",
        "time_to_complete": 3
    },
    {
        "description": "Create an outline for a presentation on the benefits of remote work.",
        "time_to_complete": 60
    },
    {
        "description": "Write a 300-word review of the movie 'The Arrival'.",
        "time_to_complete": 30
    },
    {
        "description": "Create a shopping list for tofu and olive stir fry.",
        "time_to_complete": 5
    }
]
```

Access the first element:

```python
task = task_list[0]
print(task)
```

Check whether the first task takes at most 5 minutes:

```python
task["time_to_complete"] <= 5
```

Perform the task if it takes 5 minutes or less:

```python
if task["time_to_complete"] <= 5:
    task_to_do = task["description"]
    print_llm_response(task_to_do)
```

Test with other tasks:

```python
task = task_list[1]
if task["time_to_complete"] <= 5:
    task_to_do = task["description"]
    print_llm_response(task_to_do)

task = task_list[2]
if task["time_to_complete"] <= 5:
    task_to_do = task["description"]
    print_llm_response(task_to_do)

task = task_list[3]
if task["time_to_complete"] <= 5:
    task_to_do = task["description"]
    print_llm_response(task_to_do)
```

---

## Looping Through the Task List

Instead of repeating code, use a `for` loop:

```python
for task in task_list:
    if task["time_to_complete"] <= 5:
        task_to_do = task["description"]
        print_llm_response(task_to_do)
```

---

## If-Else Blocks

Perform another action when the condition is **not met** using `else`:

```python
for task in task_list:
    if task["time_to_complete"] <= 5:
        task_to_do = task["description"]
        print_llm_response(task_to_do)
    else:
        print(f"To complete later: {task['time_to_complete']} time to complete.")
```

---

## Saving Tasks for Later Using Lists

Store incomplete tasks in a new list:

```python
tasks_for_later = []

for task in task_list:
    if task["time_to_complete"] <= 5:
        task_to_do = task["description"]
        print_llm_response(task_to_do)
    else:
        tasks_for_later.append(task)

print(tasks_for_later)
```

---

## Extra Practice

### Exercise 1: Complete Task if It Takes More Than 15 Minutes

```python
task = task_list[2]

### EDIT THE FOLLOWING CODE ###
if task["time_to_complete"] > 15:
    task_to_do = task["description"]
    print_llm_response(task_to_do)
### ---------------
```

---

### Exercise 2: Fix the Indentation

Print a message if the "Chocolate" flavor is found:

```python
ice_cream_flavors = [
    "Vanilla", "Strawberry", "Mint Chocolate Chip",
    "Cookies and Cream", "Rocky Road", "Butter Pecan",
    "Pistachio", "Salted Caramel", "Chocolate", "Mango"
]

### EDIT THE FOLLOWING CODE ###
for flavor in ice_cream_flavors:
    if flavor == "Chocolate":
        print(f"The list of flavors contains {flavor}, Andrew's favorite.")
### ---------------
```

---

### Exercise 3: Add Variables to the F-String

Add task description and time to complete:

```python
for task in task_list:
    if task["time_to_complete"] <= 5:
        task_to_do = task["description"]
        print_llm_response(task_to_do)
    else:
        ### EDIT THE FOLLOWING CODE ###
        print(f"To complete later: {task['description']} (Time to complete: {task['time_to_complete']} minutes)")
        ### ---------------
```

---
