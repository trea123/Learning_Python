# Built-in Functions

  

Here are some questions to gauge your understanding of Python’s built-in functions:

1. *What is the difference between `len()`, `max()`, `min()`, and `sum()` functions?*

  The `len()`, `max()`, `min()`, and `sum()` functions are used to find specific details of an object value such as the length, maximum value, minimum value, and the sum of numbers within a list or range. 

The `len()` function returns the number of values within an object 

```python
list1 = [1, 5, 3, 4, 2]
string = "Hello World"

print(len(list1)) # 5
print(len(string)) # 11
```

The `max()` function returns the maximum value within a set of values. 

```python
list1 = [23, 56, 76, 90, 67]
list2 = ['f', 'e', 'q', 'j', 'x', 'o']

print(max(list1)) # 90
print(max(list2)) # x
```

The `min()` function returns the minimum value within a set of values

```python
list1 = [23, 56, 76, 90, 67]
list2 = ['f', 'e', 'q', 'j', 'x', 'o']

print(min(list1)) # 23
print(min(list2)) # e
```

The `sum()` function returns the total of a set of numeric values.

```python
list1 = [23, 56, 76, 90, 67]
list2 = ['f', 'e', 'q', 'j', 'x', 'o']

print(sum(list1)) # 312
print(sum(list2)) # TypeError: unsupported operand type(s) for + 'int' and 'str'
```

As seen in the above example the sum of `list2` gave an error because it is not a numerical set of values. 

---

2. *How would you use the `enumerate()` function in a for loop?*

  The `enumerate` function is a built-in function in Python. it i used to iterate over a sequence while keeping track of the index or position of each item in the sequence. The primary purpose of `enumerate` is to provide both the value and the index of each element in the sequence during iteration. You can use the `enumerate` function in a for loop to iterate over a sequence while simultaneously accessing both the index and the value of each element.
```python
fruits = ['apple', 'banana', 'orange', 'grape', 'pear']


for index, fruit in enumerate(fruits):
	print(f"Index {index}: {fruit}")
# Index 0: apple
# Index 1: banana
# Index 2: orange
# Index 3: grape
# Index 4: pear
```

---

3. *What does the `type()` function do? Can you provide an example where it might be useful?*

The `type()` function is a built-in function in Python. It returns the data type of an object. 

---

4. *Explain how the `map()` function works. Provide an example.*

---

5. *Similarly, explain how the `filter()` function works. Provide an example.*

---

6. *What is the purpose of the `range()` function? How does it differ from `xrange()` in Python 2?*

---

7. *How does the `zip()` function work? Give an example.*

---

8. *Explain the difference between `sorted()` and `list.sort()`.*

---

9. *How can you use the `any()` and `all()` functions in Python? When might they be useful?*

---

10. *What does the `isinstance()` function do?*

---

11. *How would you use the `input()` function in a script that interacts with a user?*

---

12. *What are `ord()` and `chr()` functions? In what scenarios can they be useful?*

---

13. *What is the purpose of `globals()` and `locals()` functions?*

---

14. *How do `str()`, `int()`, `float()`, and `bool()` functions behave differently?*

---
  
15. *Explain the `eval()` function and the security implications of using it.*

---

_This [link](overview.md) will bring you back to the main assessment._
