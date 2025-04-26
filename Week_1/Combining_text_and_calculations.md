# Lesson 7: Displaying Text and Calculations Together

In this lesson, you will learn how to combine text (strings) and numbers (integers and floats) to display results in a readable way using **f-strings** in Python.

---

## Table of Contents
- [Review: Strings, Integers, and Floats](#review-strings-integers-and-floats)
- [Printing Data](#printing-data)
- [Mixing Strings with Computations: f-Strings](#mixing-strings-with-computations-f-strings)
- [Controlling Display in f-Strings](#controlling-display-in-f-strings)
- [Multi-line f-Strings](#multi-line-f-strings)
- [Extra Practice](#extra-practice)

---

## Review: Strings, Integers, and Floats

- **Strings** (text):  
  `"Hello, world"`, `"My favorite drink is Earl Grey tea"`

- **Integers and Floats** (numbers):  
  `42`, `3.14`

---

## Printing Data

Printing a string:

```python
print("Hello, World!")
```

## Mixing Strings with Computations: f-Strings
If you want to combine a calculation with text in the output, use an f-string:

Incorrect way (just prints the formula):

```python
print("The temperature 75F in degrees Celsius is ((75 - 32) * 5 / 9)C")
```
Correct way using f-string:

```python
print(f"The temperature 75F in degrees Celsius is {(75 - 32) * 5 / 9}C")
```
In an f-string:

- Prefix the string with `f`

- Insert expressions inside `{}`

## Controlling Display in f-Strings
Example:

```python
print(f"Isabel is {28/7} dog years old.")
```
If you want to remove decimal places:

```python
print(f"Isabel is {28/7:.0f} dog years old.")
```
Explanation:

`:.0f` formats the floating-point number to zero decimal places (rounds to nearest whole number).

## Multi-line f-Strings
For longer text, use triple quotes `""" """` with f-strings:
```python
print(f"""
    Most countries use the metric system for recipe measurement, 
    but American bakers use a different system. For example, they use 
    fluid ounces to measure liquids instead of milliliters (ml).
    
    So you need to convert recipe units to your local measuring system!
    
    For example, 8 fluid ounces of milk is {8 * 29.5735} ml.
    And 100ml of water is {100 / 29.5735} fluid ounces.
""")
```
Key Points:

- Triple quotes allow multi-line strings.

- Computations inside `{}` are still evaluated.

- Helps make long messages more readable.

## Extra Practice
Try these exercises:

### ✅ Modify the code to print your age:

```python
print(f"I am {} years old.")
```
### ✅ Fix this broken f-string:

```python
print(f"There are {365/7 weeks in a year")
```
### ✅ Complete this code to show area:

```python
print(f"The area of a square with side 5 cm is {} cm squared.")
```
### ✅ Modify the code to display one decimal place:

```python
print(f"The house was a good size: 1200 square feet, or {1200 * 0.092903} meters squared!")
```
## 🎉 Congratulations!
You now know how to use f-strings to mix text and calculations in Python!
Next, you'll learn how to make your code even more readable and reusable.
