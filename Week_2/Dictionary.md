# Lesson 3: Prioritizing Tasks with Dictionaries and AI

In this lesson, you'll learn about **dictionaries** in Python — a powerful data structure that lets you store **key-value pairs**. You'll also see how dictionaries can help prioritize and organize tasks for AI processing.

---

## Table of Contents
- [Getting Started](#getting-started)
- [Storing Data with Lists vs Dictionaries](#storing-data-with-lists-vs-dictionaries)
- [Understanding Dictionaries](#understanding-dictionaries)
- [Accessing Dictionary Elements](#accessing-dictionary-elements)
- [Adding and Updating Dictionary Elements](#adding-and-updating-dictionary-elements)
- [Storing Complex Data](#storing-complex-data)
- [Prioritizing Tasks with Dictionaries](#prioritizing-tasks-with-dictionaries)
- [Extra Practice](#extra-practice)
- [Summary](#summary)

---

## Getting Started

First, import the necessary helper functions:

```python
from helper_functions import print_llm_response, get_llm_response
```

---

## Storing Data with Lists vs Dictionaries

Using a **list** to store flavor descriptions:

```python
ice_cream_flavors = [
    "Vanilla: Classic and creamy...",
    "Chocolate: Deep and indulgent...",
    "Strawberry: Sweet and fruity...",
    # and so on...
]
```

❗ **Problem**: You need to remember the index to retrieve a flavor's description.

Using a **dictionary**:

```python
ice_cream_flavors = {
    "Mint Chocolate Chip": "Refreshing mint ice cream studded with decadent chocolate chips.",
    "Cookie Dough": "Vanilla ice cream loaded with chunks of cookie dough.",
    "Salted Caramel": "Sweet and salty with a smooth caramel swirl."
}
```

✅ **Benefit**: Access flavors directly by name!

---

## Understanding Dictionaries

Dictionaries are like real-world dictionaries:
- **Key**: the word
- **Value**: its definition

You can inspect the dictionary:

```python
print(ice_cream_flavors.keys())   # Lists all keys
print(ice_cream_flavors.values()) # Lists all values
```

---

## Accessing Dictionary Elements

Wrong way (causes error):

```python
print(ice_cream_flavors[0])
```

Correct way (using a **key**):

```python
cookie_dough_description = ice_cream_flavors["Cookie Dough"]
print(cookie_dough_description)
```

---

## Adding and Updating Dictionary Elements

**Adding a new entry**:

```python
ice_cream_flavors["Rocky Road"] = "Chocolate ice cream mixd witother ngredients."
```

**Fixing typos (updating existing entry)**:

```python
ice_cream_flavors["Rocky Road"] = "Chocolate ice cream mixed with other ingredients."
```

---

## Storing Complex Data

Dictionaries can also hold lists and other complex data:

```python
isabel_facts = {
    "age": 28,
    "Favorite color": "red",
    "Cat names": ["Charlie", "Smokey", "Tabitha"],
    "Favorite Snacks": ["pineapple cake", "candy"]
}
```

---

## Prioritizing Tasks with Dictionaries

In real life, tasks have different priorities.

Instead of using a single list:

```python
list_of_tasks = [
    "Compose an email...",
    "Write a birthday poem...",
    "Write a review...",
    "Draft a thank-you note...",
    "Create a presentation outline..."
]
```

Organize by priority:

```python
high_priority_tasks = [
    "Compose a brief email to my boss...",
    "Create an outline for a presentation..."
]

medium_priority_tasks = [
    "Write a birthday poem for Otto...",
    "Draft a thank-you note for Dapinder..."
]

low_priority_tasks = [
    "Write a 300-word review of 'The Arrival'."
]
```

Combine them into a **dictionary**:

```python
prioritized_tasks = {
    "high_priority": high_priority_tasks,
    "medium_priority": medium_priority_tasks,
    "low_priority": low_priority_tasks
}
```

Now you can easily focus on urgent work:

```python
for task in prioritized_tasks["high_priority"]:
    print_llm_response(task)
```

---

## Extra Practice

### 1. Update Ice Cream Flavor Description

Use the LLM to update "Rocky Road":

```python
flavor = "Rocky Road"
prompt = f"Provide a brief description for the {flavor} ice cream flavor"

ice_cream_flavors["Rocky Road"] = get_llm_response(prompt)
```

---

### 2. Complete Medium Priority Tasks

Modify the code to complete medium priority tasks:

```python
for task in prioritized_tasks["medium_priority"]:
    print_llm_response(task)
```

---

## Summary

- **Dictionaries** store data as key-value pairs.
- You can access values by their **keys**, not by index.
- **Add/update** dictionary entries easily.
- Dictionaries can hold **complex data** like lists.
- Use dictionaries to **prioritize and automate** AI tasks effectively.

---
