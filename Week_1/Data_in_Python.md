# Lesson 6: Data in Python

In this lesson, we explore different types of data in Python, focusing on text and numbers.

---

## Strings

Strings are used to store and manipulate text. Strings are written inside quotation marks and can contain letters, numbers, punctuation, and special characters.

```python
print("Hello, World")
print("My favorite drink is Earl Grey tea.")
print("¯\_(ツ)_/¯")
print("2.99")
```
## Multiline Strings

You can use triple quotation marks to create a multiline string that spans more than one line.

```python
print("""Hello, World!
      It's great to be here!""")
```
Attempting to define a multiline string using only single quotation marks will lead to an error:

```python
# This will cause an error
print("Hello, World!
      It's great to be here!")
```
## The **type()** Function
The `type()` function allows you to check the type of any data in Python.

Example checking the type of a string:

```python
type("Andrew")
```
Example checking the type of a multiline string:

```python
type("""
Numbers, text, and truth,
Strings, ints, and floats in our code,
Data shapes our path
""")
```
Checking the type of a string that looks like a number:

```python
type("2.99")
```
Checking the type of a whole number without quotes:

```python
type(100)
```
Checking the type of a floating-point number:

```python
type(2.99)
```
## Summary of Data Types
- str: Strings (text data)

- int: Integers (whole numbers)

- float: Floating point numbers (numbers with decimals)

## Python as a Calculator
Python can be used for quick arithmetic calculations. For example:

```python
# Summing up sales over 12 months
print(28+35+43+50+65+70+68+66+75+80+95)
```
To compute more complex calculations, such as compound interest, you can use exponents:

```python
# Example of using exponents
print("Complete with chatbot code")
```
## Order of Operations
Python follows standard arithmetic rules:

1. Parentheses `()`

2. Exponents `**`

3. Multiplication `*` and Division `/` (from left to right)

4. Addition `+` and Subtraction `-` (from left to right)

Incorrect Fahrenheit to Celsius conversion (due to missing parentheses):

```python
# Incorrect
print(75 - 32 * 5 / 9)
```
Correct Fahrenheit to Celsius conversion:

```python
# Correct
print((75 - 32) * 5 / 9)
```
## Debugging Practice
Fix the following errors:

```python
# Fix the error in the following code
# Incorrect
# print(There are 366 days in a leap year")
# Correct
print("There are 366 days in a leap year")
```
Fix the error in the following code
```python
# Incorrect
print("There are 366 days in a leap year")
# Correct
print("""There are 366 days in a leap year""")
```
Application Exercise
```python
Convert 6 feet to meters (1 foot = 0.3048 meters).
```
```python
# Conversion from feet to meters
print(6 * 0.3048)
```
