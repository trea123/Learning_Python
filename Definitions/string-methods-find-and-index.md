# String Methods - find() and index()

The `find()` and `index()` methods belong to a string instance object.

- The string method `find()` is used to find the position of the first occurrence of a specified substring within the original string, **returning -1 if the substring is not found**.

- The string method `index()` is used to find the position of the first occurrence of a specified substring within the original string, but it **raises a ValueError if the substring is not found**.

The optional arguments in the `find()` and `index()` methods of Python's string allow you to define a specific search range within the string. The `start` argument represents the index from which the search should begin (**inclusive**), and the `end` argument represents the index where the search should end (**exclusive**).

---

Here is an example that shows how to use the string's `find()` and `index()` methods.

```python
string = "example"
substring = "amp"
```

We will use these variables throughout the example.

---

This is a working use case for looking up a substring in a string that exists.

```python
string.find(substring)  # 2
string.index(substring)  # 2
```

When the `find()` or `index()` method is called, it is implying two questions...
1. Is the substring within the string?
2. If it is, what is the position of the first character of the substring in the string?

---

This is an example of a substring that does not exist in a string.

```python
string.find("hello")  # -1
string.index("hello")  # raises ValueError: substring not found
```

- When using the `find()` method on a substring that does not exist in a string, the function call will **return -1**.

- When using the `index()` method on a substring that does not exist in a string, the function call will **raise ValueError**.

---

This is an example of using the optional arguments, `start` and `end`, correctly.

```python
string.find(substring, 2, 5)  # 2
string.index(substring, 2, 5)  # 2
```

The arguments after *substring*, `start` and `end`, are used to define the the lower and upper bound of the substring's position in the string.

---

This is an example of using the optional arguments, `start` and `end`, with an invalid range.

```python
string.find(substring, 2, 4)  # -1
string.index(substring, 2, 4)  # raises ValueError: substring not found
```

- When using the `find()` method on a substring with an invalid `start` and `end` range, the function call will **return -1**.

- When using the `index()` method on a substring with an invalid `start` and `end` range, the function call will **raise ValueError**.

#python #definition #string 
