# Lesson 4 - Customizing Recipes with Lists, Dictionaries, and AI

In the previous lesson, you explored how to use dictionaries to complete tasks by priority. In this lesson, you will learn how to use dictionaries to update LLM prompts and create food recipes that match your friends' preferences, restrictions, and cooking experience.

## Setup

```python
from helper_functions import print_llm_response, get_llm_response
```

---

## Food Preference Dictionaries

Dictionaries are a useful way to organize multiple variables associated with a single entity. Here, we store the food preferences and cooking experience for Tommy:

```python
food_preferences_tommy = {
    "dietary_restrictions": "vegetarian",
    "favorite_ingredients": ["tofu", "olives"],
    "experience_level": "intermediate",
    "maximum_spice_level": 6
}
```

You can access dictionary keys and values using:

```python
print(food_preferences_tommy.keys())
print(food_preferences_tommy.values())
```

This dictionary has values with different data types: lists, strings, and integers.

---

## Using Keys and Values Within an AI Prompt

You can create a prompt using the information from the dictionary:

```python
prompt = f"""Please suggest a recipe that tries to include
the following ingredients:
{food_preferences_tommy["favorite_ingredients"]}.
The recipe should adhere to the following dietary restrictions:
{food_preferences_tommy["dietary_restrictions"]}.
The difficulty of the recipe should be:
{food_preferences_tommy["experience_level"]}
The maximum spice level on a scale of 10 should be:
{food_preferences_tommy["maximum_spice_level"]}
Provide a two sentence description.
"""
```

Printing and using the prompt:

```python
print(prompt)
print_llm_response(prompt)
```

---

## Refining the Prompt with Available Ingredients

You can further refine the recipe based on available ingredients:

```python
available_spices = ["cumin", "turmeric", "oregano", "paprika"]
```

Incorporating available spices into the prompt:

```python
prompt = f"""Please suggest a recipe that tries to include
the following ingredients:
{food_preferences_tommy["favorite_ingredients"]}.
The recipe should adhere to the following dietary restrictions:
{food_preferences_tommy["dietary_restrictions"]}.
The difficulty of the recipe should be:
{food_preferences_tommy["experience_level"]}
The maximum spice level on a scale of 10 should be:
{food_preferences_tommy["maximum_spice_level"]}
Provide a two sentence description.

The recipe should not include spices outside of this list:
Spices: {available_spices}
"""
```

Get the recipe from the LLM:

```python
recipe = get_llm_response(prompt)
print(recipe)
```

You can modify the prompt to request step-by-step instructions or add additional keys to the dictionary, such as favorite cuisine type.

---

## Using Boolean Values for Preferences

Instead of strings for some restrictions, you can also use boolean values:

```python
food_preferences_tommy["is_vegetarian"] = True
print(food_preferences_tommy)
```

This prepares the structure for upcoming lessons where you will work with Boolean values (`True`/`False`) in Python.

---

## Extra Practice

### 1. Update the Dictionary with Your Own Preferences

```python
my_food_preferences = {
    "dietary_restrictions": [],  # List with dietary restrictions
    "favorite_ingredients": [],  # List with top three favorite ingredients
    "experience_level": "",      # Experience level (e.g., beginner, intermediate, expert)
    "maximum_spice_level": 0      # Spice level in a scale from 1 to 10
}
print(my_food_preferences)
```

### 2. Modify the Prompt for Detailed Instructions

Edit the final sentence of the prompt so that it requests detailed step-by-step instructions instead of a short description:

```python
prompt = f"""Please suggest a recipe that tries to include
the following ingredients:
{food_preferences_tommy["favorite_ingredients"]}.
The recipe should adhere to the following dietary restrictions:
{food_preferences_tommy["dietary_restrictions"]}.
The difficulty of the recipe should be:
{food_preferences_tommy["experience_level"]}
The maximum spice level on a scale of 10 should be:
{food_preferences_tommy["maximum_spice_level"]}
Provide detailed step-by-step cooking instructions.
"""
print_llm_response(prompt)
```

---

# Summary

In this lesson, you:

- Learned how to use dictionaries to organize preferences.
- Used dictionary data to dynamically create AI prompts.
- Refined recipe suggestions based on additional constraints.
- Prepared for future lessons by introducing Boolean values.

In the next lesson, you will explore Boolean values (`True` and `False`) and their role in Python programming.

