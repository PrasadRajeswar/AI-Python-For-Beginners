# Lesson 10: Functions - Actions on Data

Learn how to use built-in Python **functions** to perform actions on data, create smarter AI prompts, and store results dynamically.

---

## Table of Contents
- [Importing Helper Functions](#importing-helper-functions)
- [Review: Functions You Have Used](#review-functions-you-have-used)
- [New Functions: `len()`, `round()` and More](#new-functions-len-round-and-more)
- [Saving Function Results to Variables](#saving-function-results-to-variables)
- [Using Functions in AI Programs](#using-functions-in-ai-programs)
- [Extra Practice](#extra-practice)
- [Summary](#summary)

---

## Importing Helper Functions

Start by importing the necessary helper functions:

```python
from helper_functions import *
```
This includes functions like:

`print_llm_response()` — Sends a prompt to an LLM and prints the response.

`get_llm_response()` — Sends a prompt to an LLM and returns the response as a string.

## Review: Functions You Have Used
Some functions you've already encountered:

```python
print("¯\_(ツ)_/¯")
print_llm_response("What is the capital of France?")
type(17)  # Displays the data type (int)
```
## New Functions: len(), round() and More
You can use many built-in functions to act on your data:

```python
# Find the length of a string
print(len("Hello World!"))

# Round a floating point number
print(round(42.17))
```
## Saving Function Results to Variables
You can save the output of a function to a variable:

```python
string_length = len("Hello World!")
print(string_length)  # Outputs: 12
```
Tip: You don't need to memorize every function — ask the chatbot if you need help! Example prompt: "How can I find the length of a string?"

## Using Functions in AI Programs
Mix variables, functions, and AI prompts together!

Example:

```python
name = "Tommy"
potatoes = 4.75
prompt = f"""Write a couplet about my friend {name} who has about {round(potatoes)} potatoes"""
response = get_llm_response(prompt)
print(response)
```
- `round(potatoes)` rounds 4.75 to 5.

- `get_llm_response()` gets the LLM output as a string.

- `print()` displays the final output.

## Extra Practice
1. Lucky Number Generator
```python
# Multiply your favorite number by 10 and save it
lucky_number = 
print(f"Your lucky number is {lucky_number}!")
```
2. Create a Poem with print_llm_response()
```python
number_of_lines = 
prompt = f"Write me a poem with {number_of_lines} lines."
print_llm_response(prompt)
```
3. Create a Poem with get_llm_response()

```python
number_of_lines = 
prompt = f"Write me a poem with {number_of_lines} lines."
response = get_llm_response(prompt)
print(response)

```
## 🎯 Summary
Functions process data and return results.

You can store function results inside variables.

Functions like len(), round(), print_llm_response(), and get_llm_response() make your programs dynamic and flexible.

Functions are powerful tools, especially when building prompts for AI models.
