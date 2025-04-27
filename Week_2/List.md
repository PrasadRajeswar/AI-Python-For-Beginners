# Lesson 1: Completing a Task List with AI

Welcome! In this lesson, you’ll learn how to automate tasks using **Python**, and how to **store multiple pieces of data** together using **lists** — a powerful and essential data type.

---

## Table of Contents
- [Getting Started](#getting-started)
- [Creating a List](#creating-a-list)
- [Using Lists in AI Prompts](#using-lists-in-ai-prompts)
- [Accessing List Elements](#accessing-list-elements)
- [Adding and Removing Elements](#adding-and-removing-elements)
- [Lists with Other Data Types](#lists-with-other-data-types)
- [Using Lists to Complete Tasks](#using-lists-to-complete-tasks)
- [Extra Practice](#extra-practice)
- [Summary](#summary)

---

## Getting Started

First, import the necessary helper functions:

```python
from helper_functions import print_llm_response, get_llm_response
```
You’ll use:

- `print_llm_response()` — sends a prompt to an LLM and prints the output.

- `get_llm_response()` — sends a prompt to an LLM and returns the output as a string.

## Creating a List
Create a list of friends:

```python
friends_list = ["Tommy", "Isabel", "Daniel"]
print(friends_list)
print(type(friends_list))  # Output: <class 'list'>
print(len(friends_list))   # Output: 3
```
## Using Lists in AI Prompts
You can include entire lists inside LLM prompts:

```python
prompt = f"""
Write a set of four-line birthday poems for my friends {friends_list}. 
The poems should be inspired by the first letter of each friend's name.
"""
print_llm_response(prompt)
```
## Accessing List Elements
Access individual elements using indexing:

```python
first_friend = friends_list[0]
print(first_friend)   # Output: Tommy

print(friends_list[1])  # Output: Isabel
print(friends_list[2])  # Output: Daniel
```
⚠️ Remember: Indexing starts at 0, not 1!

Trying to access an out-of-range index like `friends_list[3]` will cause an error.

## Adding and Removing Elements
Adding a New Friend
```python
friends_list.append("Otto")
print(friends_list)
```
Try adding yourself too!

```python
friends_list.append("YourName")
```
Removing a Friend
```python
friends_list.remove("Tommy")
print(friends_list)
```
## Lists with Other Data Types
Lists can hold any type of data.

Example of a list of numbers:

```python
list_ages = [42, 28, 30]
print(list_ages)
```
Example of a list of tasks:

```python
list_of_tasks = [
    "Compose an email to my boss explaining I'll be late.",
    "Write a birthday poem for Otto.",
    "Write a 300-word review of the movie 'The Arrival'."
]
```
## Using Lists to Complete Tasks
You can automate tasks by looping through your list:

```python
task = list_of_tasks[0]
print_llm_response(task)

task = list_of_tasks[1]
print_llm_response(task)

task = list_of_tasks[2]
print_llm_response(task)
(Later, you'll learn how to automate this better with loops.)
```
## Extra Practice
1. Create a List of Your Favorite Movies
```python
movie_list = ["Inception", "Interstellar", "The Matrix", "Arrival", "Blade Runner 2049"]
```
2. Display the Fourth Element
```python
prime_numbers = [2, 3, 5, 7, 11]
print(prime_numbers[3])  # Output: 7
```
3. Fix the Bug
Incorrect:

```python
print(prime_numbers(3))
```
Correct:

```python
print(prime_numbers[3])
```
4. Add a Friend
```python
friends_list = ["Tommy", "Isabel", "Daniel", "Otto"]
friends_list.append("YourFriendName")
print(friends_list)
```
5. Remove a Non-South American Country
```python
countries_in_south_america = ["Colombia", "Peru", "Brasil", "Japan", "Argentina"]
countries_in_south_america.remove("Japan")
print(countries_in_south_america)
```
## Summary
- Lists store multiple pieces of data in one variable.

- Access list elements using indexing.

- Modify lists using append() and remove().

- Combine lists with LLM prompts to automate creative tasks.

- Lists are a powerful foundation for future automation with loops!

