# Data Types

## Integers

1. *How would you convert a float or a string to an integer?*

+ The only way to **convert a string to an integer** is if the string contains a whole number. If the string contains a decimal or anything other than a whole number, the conversion will fail.

```python
data = "24"
print("The value of 'data' before conversion"
	  f" is {data} and has the data type"
	  f" of {type(data)}.")
# The value of 'data' before conversion \
#  is 24 and has the data type of <class 'str'>.

data = int(data)
print("The value of 'data' after conversion"
	  f" is {data} and has the data type"
	  f" of {type(data)}.")
# The value of 'data' after conversion \
#  is 24 and has the data type of <class 'int'>.
```

+ When you **convert a float to an integer** you always **round it down** to a whole number.

```python
data = 9.99
print("The value of 'data' before conversion"
	  f" is {data} and has the data type"
	  f" of {type(data)}.")
# The value of 'data' before conversion \
#  is 9.99 and has the data type of <class 'float'>.

data = int(data)
print("The value of 'data' after conversion"
	  f" is {data} and has the data type"
	  f" of {type(data)}.")
# The value of 'data' after conversion \
#  is 9 and has the data type of <class 'int'>
```

---

2. *What does it mean that integers in Python 3 are of arbitrary size?*

In Python 3, integers are of arbitrary size, meaning they can grow to hold any extremely large value without predefined limits. This dynamic allocation of memory allows Python to handle calculations involving very large numbers without overflow errors.

---

3. *What is the difference between `//` and `/` when performing division operations in Python?*

+ The `//` operator is used to perform [[floor_division]].

```python
floor_division = 4 // 2
print(floor_division, type(floor_division))
```

+ The `/` operator is used to perform [[decimal_division]].

```python
decimal_division = 4 / 2
print(decimal_division, type(decimal_division))
```

---


## Floats (Floating-Point numbers)

1. *How do you round a floating-point number to a specific number of decimal places in Python?*

Python has a built-in function called [[round]]. To round to a specific number of decimal places, you would need to provide the number you would like to round and optionally, the amount of decimal places you would like to round it to. Here is an example.

```python
number = 5.2678

print(f"The number {number} rounded to the nearest"
	  " whole number, expressed like 'round(number)'"
	  f" equals {round(number)}.")
# The number 5.2678 rounded to the nearest whole number,
#  expressed like 'round(number)' equals 5.

print(f"The number {number} rounded to the nearest"
	  " three decimal places, expressed like"
	  f" 'round(number, 3)' equals {round(number, 3)}.")
# The number 5.2678 rounded to the nearest
#  three decimal places, expressed like
#  'round(number, 3)' equals 5.268.
```

---

2. *Can you explain the limitations of floating point arithmetic and why it might lead to seemingly odd results (for example, `0.1 + 0.2 != 0.3`)?*

Floating-point arithmetic has limitations due to finite precision and binary representation. Numbers are stored with a fixed number of bits, leading to rounding errors during calculations. Binary representation may cause some decimal numbers to be imprecise. As a result, seemingly simple calculations like `0.1 + 0.2` might not equal `0.3` exactly due to accumulated rounding errors and the inability to represent these numbers precisely in binary. The result is a value that is very close to `0.3` but not exactly equal to it, leading to the odd result `0.1 + 0.2 != 0.3` in some programming languages.

---

3. *How would you convert a string or an integer to a float?*


+ The only way to **convert a string to a float** is if the string contains a decimal. If the string contains anything other than a decimal or an integer, it will not work.

```python
data = "24"
print("The value of 'data' before conversion"
	  f" is {data} and has the data type"
	  f" of {type(data)}.")
# The value of 'data' before conversion \
#  is 24 and has the data type of <class 'str'>.

data = float(data)
print("The value of 'data' after conversion"
	  f" is {data} and has the data type"
	  f" of {type(data)}.")
# The value of 'data' after conversion \
#  is 24.0 and has the data type of <class 'float'>.
```

+ When you **convert an integer to a float** you will add a decimal to the whole number of zero.

```python
data = 9
print("The value of 'data' before conversion"
	  f" is {data} and has the data type"
	  f" of {type(data)}.")
# The value of 'data' before conversion \
#  is 9 and has the data type of <class 'int'>.

data = float(data)
print("The value of 'data' after conversion"
	  f" is {data} and has the data type"
	  f" of {type(data)}.")
# The value of 'data' after conversion \
#  is 9.0 and has the data type of <class 'float'>
```

---

## Complex Numbers

1. *How would you define a complex number in Python?*

In Python, you can define a complex number using the `complex` function or by specifying the real and imaginary parts with a `j` suffix. For example, `z = complex(real_part, imaginary_part)` or `z = real_part + imaginary_part * 1j`. The `real_part` represents the real component, and the `imaginary_part` represents the imaginary component of the complex number.

---

2. *How can you access the real and imaginary parts of a complex number?*

To access the real and imaginary parts of a complex number in Python, you can use the `real` attribute and the `imag` attribute. For instance, if you have a complex number `z`, you can access its real part by using `z.real` and its imaginary part with `z.imag`. These attributes allow you to retrieve the real and imaginary components of a complex number, which you can use in your Python programs for further calculations or manipulations.

---

## Strings

1. *How do you concatenate two strings?*

To concatenate two strings you could simply add them together. Left string plus right string equals both strings squished  together.

```python
x = "hello"
y = "world"
print(x + y)
# helloworld
```

---

2. *What are some methods for formatting strings in Python? Can you give examples of each?*

Three methods of formatting strings are f-strings, format strings and, injections.

```python
# f-strings
name = "Trea'Von"
age = "19"
print(f"hello, I am {name}. I am {age} years old.")
# hello, I am Trea'Von. I am 19 years old.
```

```python
name = "Trea'Von"
age = "19"
greeting = "hello, I am {}. I am {} years old."
print(greeting.format(name, age))
# hello, I am Trea'Von. I am 19 years old.
```

```python
name = "Trea'Von"
age = 19
greeting = "hello, I am %s. I am %i years old."
print(greeting % (name, age))
# hello, I am Trea'Von. I am 19 years old.
```

---

3. *What is string slicing? Give an example of how you might use it.*

String slicing is outputing a certain index of a string provided.

```python
examples = []
for _ in range(3):
    num = random.randint(1, 100)
    string = f"This is {num}"
    examples.append(string)

print(examples)
# ['This is 96', 'This is 91', 'This is 61']

for example in examples:
    print(example[8:])
# 96
# 91
# 61
```

---

4. *What is the difference between a string’s `find()` and `index()` methods?*

The difference between a [[string-methods-find-and-index|string's find and index methods]] lies in their behavior when the specified substring is not found in the original string.

1. `find()` method: If the substring is not found in the string, the `find()` method will **return -1**. This allows you to check for the presence of the substring without raising an error.

2. `index()` method: If the substring is not found in the string, the `index()` method will **raise ValueError**. This means you need to handle the exception using try-except blocks if you are unsure whether the substring exists in the string.

Here's an example illustrating the difference:

```python
string = "Hello, World!"

# Using find() method
pos1 = string.find("World")  # pos1 = 7
pos2 = string.find("Universe")  # pos2 = -1

# Using index() method
try:
    pos3 = string.index("World")  # pos3 = 7
    pos4 = string.index("Universe")  # Raises ValueError
except ValueError as e:
    print("Substring not found.")
```

So, if you want to check for the existence of a substring without raising an error, use `find()`. If you want to raise an error when the substring is not found, use `index()`.

---

5. *What are escape sequences in Python strings, and when might you use them?*

In Python strings, [[escape-sequences|escape sequences]] are combinations of characters that begin with a backslash `\`. These sequences are used to represent certain special characters that have specific meanings. Common escape sequences in Python include `\n` for a newline, `\t` for a tab, `\\` for a backslash, `\'` for a single quote, and `\"` for a double quote. When you use an escape sequence in a string, the backslash indicates that the character following it should be treated as a special character, not its literal representation.

You might use escape sequences in Python strings in various situations. Here are some examples:

1. **Newlines and Tabs**: When you want to insert newlines or tabs for formatting purposes, you can use `\n` and `\t` respectively.

2. **Quotes inside Strings**: If you need to include single or double quotes within a string, you can escape them with `\'` or `\"` to avoid prematurely ending the string.

3. **File Paths**: In file paths, backslashes are used as directory separators on Windows. To avoid any issues with escape sequences in file paths, you can use [[raw-strings|raw strings]] (`r"..."`) or double backslashes (`"C:\\path\\to\\file"`).

4. **Regular Expressions**: Regular expressions often contain special characters. To simplify writing regular expressions, escape sequences can be used.

In summary, escape sequences in Python strings are a powerful tool for including special characters and maintaining the correct interpretation of characters within strings for various purposes like formatting, handling file paths, or constructing regular expressions.

---

1. *How would you convert a number to a string? And a string to a number?*



---


## Booleans

1. *What values in Python are considered “false”?*



---

2. *What is the difference between `==` and `is` when comparing variables in Python?*

---

3. *How would you use the `and`, `or`, and `not` boolean operators in Python?*

---

4. *Can you explain short-circuit evaluation in the context of boolean operations?*