# Lesson 9: Building LLM Prompts with Variables

In this lesson, you will learn how to **use variables** to **build dynamic prompts** for an **LLM (Large Language Model)** and make your code more flexible and powerful.

---

## Table of Contents
- [Importing the LLM Helper Function](#importing-the-llm-helper-function)
- [Sending a Simple LLM Query](#sending-a-simple-llm-query)
- [Using Variables Inside Prompts](#using-variables-inside-prompts)
- [Fixing Variable Naming Issues](#fixing-variable-naming-issues)
- [Extra Practice](#extra-practice)
- [Summary](#summary)

---

## Importing the LLM Helper Function

First, import the provided helper function:

```python
from helper_functions import print_llm_response
```
The `print_llm_response()` function sends a string instruction to an LLM and displays the generated response.

## Sending a Simple LLM Query
You can start with a simple prompt:

```python
print_llm_response("What is the capital of France?")
```
## Using Variables Inside Prompts
Define some variables:

```python
name = "Otto Matic"
dog_age = 21 / 7
```
Then, use f-strings to create a custom instruction dynamically:

```python
print_llm_response(f"""If {name} were a dog, he would be {dog_age} years old.
Describe what life stage that would be for a dog and what that might 
entail in terms of energy level, interests, and behavior.""")
```
✅ You just used AI with your own variables! 🎉

## Fixing Variable Naming Issues
Some variable names were incorrect. Here’s how to fix them:

Incorrect code:

```python
driver = "unicorn"
driver's vehicle = "colorful, asymmetric dinosaur car"  # ❌ Invalid
favorite planet = "Pluto"                               # ❌ Invalid
```
✅ Corrected code:

```python
driver = "unicorn"
drivers_vehicle = "colorful, asymmetric dinosaur car"
favorite_planet = "Pluto"
```
Now, use them in a prompt:

```python
print_llm_response(f"""Write me a 300-word children's story about a {driver} racing
a {drivers_vehicle} for the {favorite_planet} champion cup.""")
```
## Extra Practice
Practice exercises:

✅ Fix this broken code:

Incorrect:

```python
1favorite-book = "1001 Ways to Wear a Hat"
"2002 Ways to Wear a Scarf" = second_fav_book
print(f"My most favorite book is {1favorite-book}, but I also like {second_fav_book})
```
✅ Corrected:

```python
first_fav_book = "1001 Ways to Wear a Hat"
second_fav_book = "2002 Ways to Wear a Scarf"
print(f"My most favorite book is {first_fav_book}, but I also like {second_fav_book}.")
```
✅ Creative Practice:

Define your favorites:

```python
favorite_game = "Chess"
favorite_movie = "Inception"
favorite_food = "Sushi"
```
Send a creative LLM prompt:

```python
print_llm_response(f"""
Based on my favorites — game: {favorite_game}, movie: {favorite_movie}, and food: {favorite_food} —
recommend a new song I should listen to that matches my taste.
""")
```

## 🎯 Summary
You can build dynamic LLM prompts by inserting variables into f-strings.

Correct variable naming is crucial for smooth execution.

Using variables makes your code more organized, efficient, and creative when working with AI.
