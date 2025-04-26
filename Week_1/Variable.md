# Lesson 8: Variables

In computer programming, **variables** are used to **store**, **process**, and **manipulate** data.

---

## Table of Contents
- [Introduction to Variables](#introduction-to-variables)
- [Printing Variables](#printing-variables)
- [Variables for Different Data Types](#variables-for-different-data-types)
- [Variables are Case-Sensitive](#variables-are-case-sensitive)
- [Variables for Changing Values](#variables-for-changing-values)
- [Variable Naming Rules](#variable-naming-rules)
- [Efficiency with Variables](#efficiency-with-variables)
- [Extra Practice](#extra-practice)

---

## Introduction to Variables

To store a value in a variable:

```python
age = 28
```
You can then display it:

```python
print(age)
```
You can reassign a variable at any time:

```python
age = 5
print(age)
```
## Printing Variables
Use f-strings for more descriptive output:

```python
print(f"Age: {age}")
```
Example with name and height:

```python
name = "Otto"
gnome_height = 12.7

print(f"Name: {name}")
print(f"Gnome height: {gnome_height}")
```

## Variables for Different Data Types
Variables can store different types of data:

- Strings: `"Otto"`

- Integers: `28`

- Floats: `12.7`

## Variables are Case-Sensitive
Python treats variable names with different cases as different variables:

```python
# This will raise an error if Gnome_height is not defined
print(f"Gnome height: {Gnome_height}")
```
✅ Correct usage:

```python
print(f"Gnome height: {gnome_height}")
```
## Variables for Changing Values
Example with a game score:

```python
score = 0
print(score)

score = score + 50
print(score)

score = score + 100
print(score)

score = score + 300
print(score)

print(f"Your final score was: {score}")
The variable score keeps updating as the game progresses.
```
## Variable Naming Rules
Invalid variable name:

```python
my score = 450  # ❌ This will cause an error!
```
✅ Variables cannot contain spaces. Use underscores instead:

```python
my_score = 450
```
## Efficiency with Variables
Instead of repeating calculations:

```python
print(49 / 7)
print(f"""Otto's dog age is {49/7}. 
A dog that's about {49/7} years old is the same age as Otto.""")
```
You can define a variable:

```python
dog_age = 49 / 7

print(f"""Otto's dog age is {dog_age}. 
A dog that's about {dog_age} years old is the same age as Otto.""")
```
If Otto's age changes:

```python
dog_age = 50 / 7
```
You only need to update the variable once!

Using both `name` and `dog_age` in an f-string:

```python
name = "Otto Matic"
print(f"""{name}'s dog age is {dog_age}.
A dog that's about {dog_age} years old is the same age as {name}.""")
```
## Extra Practice
Practice exercises:

✅ Create a variable for your name and print a greeting:

```python
my_name = 
print()
```
✅ Store your favorite number and print a message adding 10:

```python
fav_num = 
print(f"Your favorite number plus 10 is {}")
```
✅ Create two variables for countries visited and planned to visit:

```python
countries_visited = 
countries_to_visit = 

print(f"""I have visited {} countries. 
I plan to visit {} more countries, 
and when I'm done I will have visited {} countries.""")
```
## 🎯 Summary
Variables store data.

Variables can be updated.

Variables make your code more efficient and easier to manage.
