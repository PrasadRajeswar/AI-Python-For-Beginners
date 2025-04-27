# Lesson 5 - Comparing Data in Python

```python
from helper_functions import print_llm_response, get_llm_response
```

## Introduction to Booleans

Take a closer look at the `True`/`False` variable you saw at the end of the last lesson:

```python
food_preferences_tommy = {
    "favorite_ingredients": ["mushrooms", "olives"],
    "experience_level": "intermediate",
    "maximum_spice_level": 6
}

food_preferences_tommy["is_vegetarian"] = True
print(food_preferences_tommy)
```

This type of data is known as **boolean**. It can only take two values: `True` or `False`.

```python
print(True)
print(False)
```

You can check the type for each:

```python
type(True)
type(False)
```

Booleans are named after George Boole, a mathematician who pioneered this kind of logic.

You can also assign booleans to variables:

```python
is_tommy_my_friend = True
is_isabel_older_than_me = False

print(is_tommy_my_friend)
print(is_isabel_older_than_me)

type(is_isabel_older_than_me)
```

---

## Comparison Operators

Booleans are often the result of comparing variables. For example:

```python
isabel_age = 28
daniel_age = 30
tommy_age = 30
```

Determine if Isabel is older than Daniel:

```python
print(isabel_age > daniel_age)
```

Determine if she is younger:

```python
print(isabel_age < daniel_age)
```

Assign the result to a variable:

```python
is_isabel_older_than_daniel = isabel_age > daniel_age
print(is_isabel_older_than_daniel)
```

Use `<=` and `>=` to check "less than or equal" or "greater than or equal":

```python
print(isabel_age <= daniel_age)
print(tommy_age < daniel_age)
print(tommy_age <= daniel_age)
```

---

## Equality Operator

The `==` operator checks if two things are equal:

- `=` is an **assignment** operator.
- `==` is a **comparison** operator.

Example comparisons:

```python
print(tommy_age == daniel_age)
print(isabel_age == daniel_age)
```

Comparison works for strings too:

```python
print("vegetarian" == "vegan")
```

---

## Logical Operators

Logical operations with booleans involve operators like `and` and `or`.

```python
is_tommy_my_friend = True
is_isabel_my_friend = True
```

Check if **both** are your friends:

```python
print(is_tommy_my_friend and is_isabel_my_friend)
```

Check if **at least one** is your friend:

```python
print(is_tommy_my_friend or is_isabel_my_friend)
```

Another example with a game involving ages:

```python
isabel_age = 28
daniel_age = 30
otto_age = 29

is_isabel_younger_than_tommy = isabel_age < tommy_age
is_isabel_younger_than_daniel = isabel_age < daniel_age

print(is_isabel_younger_than_tommy and is_isabel_younger_than_daniel)
```

---

## Extra Practice

### Exercise 1: Comparison Operators

Check whether Isabel is older than at least one of your friends (Tommy and Daniel):

```python
# Hint: Replace the "?" with the correct comparison operator
is_isabel_older_than_tommy = isabel_age > tommy_age
is_isabel_older_than_daniel = isabel_age > daniel_age
```

---

### Exercise 2: Logical Operators

Check if Isabel is older than at least one of your friends:

```python
# Hint: Recall the logical operators "and" and "or"
print("Check if Isabel is older than at least one of my friends")
print(is_isabel_older_than_tommy or is_isabel_older_than_daniel)
```

---

## Summary

- **Booleans** represent `True` or `False`.
- **Comparison operators** like `>`, `<`, `==`, `<=`, `>=` return booleans.
- **Logical operators** like `and` and `or` combine boolean values.
- You can use booleans to make decisions in your code.

In the next lesson, you'll learn how to **execute different blocks of code depending on boolean conditions**.

---

✅ Now you can copy and paste this directly into a `README.md` file.  

Would you also like me to format it a bit more stylishly (for example, with collapsible sections like `<details>` tags) if you want it for a GitHub page? 📚
