# Data Structures

Here are some potential questions to assess your understanding of Python data structures like lists, tuples, sets, and dictionaries:

## List

1. *How would you add an element to the end of a Python list? How about inserting it at a specific index?*

In Python, you can add an element to the end of a list using the `append()` method, and you can insert an element at a specific index using the `insert()` method. Here's how you would do both:

1. **Adding an element to the end of a list using `append()`**:
```python
my_list = [1, 2, 3, 4]
new_element = 5

my_list.append(new_element)

print(my_list)  # Output: [1, 2, 3, 4, 5]
```

2. **Inserting an element at a specific index using `insert()`**:
```python
my_list = [1, 2, 3, 4]
new_element = 5
index_to_insert = 2

my_list.insert(index_to_insert, new_element)

print(my_list)  # Output: [1, 2, 5, 3, 4]
```

In the above example, the `insert()` method takes two arguments: the index at which you want to insert the new element and the element itself. The element is inserted before the specified index, shifting the elements at and after that index to the right. Keep in mind that indices in Python are zero-based, so the first element is at index 0, the second element is at index 1, and so on.

---

2. *What’s the difference between `list.pop(index)` and `del list[index]`?*

`del list()` and `list.pop()` are two different ways of modifying a Python list, but they serve distinct purposes.

1. `del list()`: This syntax is incorrect. You cannot use the `del` keyword with the list() constructor. The `del` statement
 is used to delete variables or items from a collection, but it is not directly used to create or modify a list.

For example, if you have a list named my_list and you want to delete the entire list, you can use `del my_list.` This will
 remove the entire list and free up the memory it was using.

```python
my_list = [1, 2, 3, 4, 5]                                                                                                     
del my_list                                                                                                                   
# Now the variable 'my_list' is deleted, and the list is removed from memory.                                                 
```                                                                                                                           

2. `list.pop()`: The `pop()` method is used to remove and return the last element from a list, modifying the list in place. If
 you provide an index to the `pop()` method, it will remove and return the element at that specific index.

```python
my_list = [1, 2, 3, 4, 5]                                                                                                     
popped_element = my_list.pop()                                                                                                
# The last element (5) is removed from 'my_list' and assigned to 'popped_element'.                                            
# 'my_list' is now [1, 2, 3, 4].                                    


second_popped_element = my_list.pop(1)                                                                                        
# The element at index 1 (2) is removed from 'my_list' and assigned to 'second_popped_element'.                               
# 'my_list' is now [1, 3, 4].                                                                                                 
```                                                                                                                           

To summarize:
- `del list()` is not a valid syntax for modifying a list; it is used to delete variables or items.
- `list.pop()` is a method specifically for removing and returning elements from a list.

---

3. *What is list comprehension and can you provide an example of it?*

list comprehension is a simplified and optimized way of running a for loop within an empty list. 

```python
x = [num for num in range(1, 11)]
print(x) # [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
```

---

4. *How would you sort a list in ascending order? How about descending order?*

The `list.sort()` function is used to sort a list. By default it will sort in an ascending order. To sort in descending order, the action is similar except you would pass in the reverse parameter. 

In the below example, the `list.sort()` function is used to sort the list.

```python
fruits = ["orange", "apple", "banana", "mango"]

fruits.sort()
print(fruits) # ['apple', 'banana', 'mango', 'orange']

```

In the below example, the `list.sort(reverse=True)`

```python
fruits = ["orange", "apple", "banana", "mango"]

fruits.sort(reverse=True)
print(fruits) # ['orange', 'mango', 'banana', 'apple']
```

---

5. *How can you reverse a list in Python?*

The `list.sort` function is a built-in function. It is used to sort an iterable in an ascending order by default.  To revers a list, you would pass in the `reverse` parameter.

```python
fruits = ["orange", "apple", "banana", "mango"]

fruits.sort(reverse=True)
print(fruits) # ['orange', 'mango', 'banana', 'apple']
```

---

6. *How can you remove duplicates from a list while preserving order?

To remove an item while preserving the order, you could use a list comprehension. Here is on example.

```python
def remove_duplicates_preserve_order(input_list):
    unique_elements = set()
    return [item for item in input_list if not (item in unique_elements or unique_elements.add(item))]

# Example usage
original_list = [3, 2, 1, 2, 4, 3, 5]
unique_list = remove_duplicates_preserve_order(original_list)
print(unique_list)  # Output: [3, 2, 1, 4, 5]

```

---

7. *Describe the difference between shallow copy and deep copy in the context of lists.*

It seems like there might be a typo in your question. I believe you're asking about "shallow copy" and "deep copy" in Python.

1. **Shallow Copy:**
A shallow copy creates a new object but does not create copies of the nested objects. Instead, it references the same nested objects as the original. In other words, it copies the top-level structure of the object, but not its contents. Shallow copies are made using the `copy()` method or the `copy` module's `copy()` function.

Example of creating a shallow copy:

```python
import copy

original_list = [1, [2, 3], 4]
shallow_copied_list = copy.copy(original_list)

# Modifying the nested list in the shallow copy affects the original
shallow_copied_list[1][0] = 99

print(original_list)           # Output: [1, [99, 3], 4]
print(shallow_copied_list)     # Output: [1, [99, 3], 4]
```

2. **Deep Copy:**
A deep copy creates a new object and recursively copies all the nested objects as well. It ensures that a completely independent copy of the original object is created, including copies of all the nested objects. Deep copies are made using the `copy` module's `deepcopy()` function.

Example of creating a deep copy:

```python
import copy

original_list = [1, [2, 3], 4]
deep_copied_list = copy.deepcopy(original_list)

# Modifying the nested list in the deep copy doesn't affect the original
deep_copied_list[1][0] = 99

print(original_list)           # Output: [1, [2, 3], 4]
print(deep_copied_list)        # Output: [1, [99, 3], 4]
```

In summary, a shallow copy creates a new object that references the same nested objects, while a deep copy creates a new object with fully independent copies of all nested objects. The choice between these two methods depends on your specific use case and whether you need a truly independent copy of the original object and its contents.

---


## Tuple

1. *How is a tuple different from a list?*

A tuple is an immutable data type. Once it is created, it cannot be modified whereas, a list is a mutable data type. Once created it can be modified. Here is an example. 

my_list = [1, 2, 3]
my_tuple = (1, 2, 3)

```python
my_list[0] = 10  # Valid, modifies the list
# my_tuple[0] = 10  # Invalid, would raise a TypeError since tuples are immutable

my_list.append(4)  # Valid, modifies the list
 my_tuple.append(4)  # Invalid, tuples don't have an append method

print(my_list)  # Output: [10, 2, 3, 4]
print(my_tuple)  # Output: (1, 2, 3)
```


---

2. *Can you modify an element of a tuple? Explain your answer.*

A tuple is an immutable data type. Once it is created all elements inside of it cannot be modified. By making tuples immutable, Python provides a way to create data structures that are stable, reliable, and efficient. While it might seem limiting that tuples cannot be modified after creation, this immutability is a deliberate design choice that brings many benefits, especially when dealing with use cases where data integrity and reliability are paramount. If you need a mutable collection, Python provides the list data type to fulfill that role.

---

3. *When would you use a tuple instead of a list?*

In some cases, a tuple preferred over a list because it provides stability, reliability and efficiency. If you have data that shouldn't be modified, is used for packing/unpacking, needs to be hashable, or represents a fixed collection of items, tuples are a suitable choice.

---

4. *How can you convert a tuple to a list and vice versa?*

You can convert a tuple to a list and vice versa using the built-in `list()` and `tuple()` functions in Python. Here's how to do it:

**Converting a Tuple to a List:**
You can use the `list()` function to convert a tuple to a list:

```python
my_tuple = (1, 2, 3)
my_list = list(my_tuple)
print(my_list)  # Output: [1, 2, 3]
```

**Converting a List to a Tuple:**
You can use the `tuple()` function to convert a list to a tuple:

```python
my_list = [4, 5, 6]
my_tuple = tuple(my_list)
print(my_tuple)  # Output: (4, 5, 6)
```

Both of these methods create new objects of the target type (list or tuple) with the same elements as the original collection. Keep in mind that while converting a list to a tuple or vice versa, you are creating a new object and not modifying the original one.

---

## Set

1. *What is a set in Python?*

A set is a built-in collection data type that represents an unordered collection of unique elements. Sets are used to store a collection of distinct items where the order of elements doesn't matter, and each element appears only once. 

Here's how you can create and work with sets in Python:
```python
# Creating a set
my_set = {1, 2, 3, 4, 5}

# Adding elements to a set
my_set.add(6)

# Removing elements from a set
my_set.remove(3)

# Checking for membership
print(2 in my_set)  # Output: True

# Iterating over a set
for element in my_set:
    print(element)

# Set operations
set1 = {1, 2, 3}
set2 = {3, 4, 5}
union = set1 | set2
intersection = set1 & set2
difference = set1 - set2

print(union)        # Output: {1, 2, 3, 4, 5}
print(intersection) # Output: {3}
print(difference)   # Output: {1, 2}

```

---

2. *What are the primary use cases for a set?*

Sets in Python are primarily used in situations where you need to work with collections of unique elements. Their unique characteristics make them well-suited for specific tasks and operations. Here are some primary use cases for sets:

1. **Removing Duplicates:** If you have a list or other iterable containing duplicate elements, converting it to a set will automatically remove the duplicates, leaving you with a collection of unique elements.

2. **Membership Testing:** Sets are very efficient for checking whether a specific element is present in a collection. This makes them suitable for tasks like checking if a value exists in a large dataset.

3. **Finding Distinct Elements:** When you want to extract the distinct or unique elements from a sequence, such as counting the number of different words in a text.

4. **Set Operations:** Sets are useful for performing set operations like union, intersection, and difference. These operations are often used in tasks involving data manipulation, filtering, and comparisons.

5. **Filtering Data:** You can use sets to filter out unwanted or duplicate elements from a collection.

6. **Counting Frequency:** Sets can be used to count the frequency of unique elements in a sequence. You can iterate over the sequence, adding elements to a set and incrementing a counter, ensuring each element is counted only once.

7. **Eliminating Order Dependency:** If you need to work with a collection where the order of elements doesn't matter, using a set can simplify your code and remove order dependencies.

8. **Hash-Based Lookup:** If you need fast and efficient lookups for unique elements, sets provide O(1) average time complexity for membership testing and element insertion.

9. **Removing Items from Collections:** Sets provide a convenient way to remove items from collections, ensuring you only remove each item once.

10. **Deduplication:** Before processing data, sets can be used to remove duplicates, ensuring that subsequent operations are performed on unique data.

11. **Caching and Memoization:** Sets can be used for caching or memoization purposes, where you store the results of expensive operations to avoid redundant calculations.

Keep in mind that sets are not suitable for preserving the order of elements or for cases where duplicate elements are important. For these cases, you may want to use other data structures like lists or dictionaries. Sets excel at tasks that involve uniqueness, membership testing, and efficient set operations.

---

3. *How can you add and remove elements from a set?*

You can add and remove elements from a set in Python using the following methods:

**Adding Elements:**

1. **`add()` Method:** You can use the `add()` method to add a single element to a set.

```python
my_set = {1, 2, 3}
my_set.add(4)
print(my_set)  # Output: {1, 2, 3, 4}
```

2. **`update()` Method:** The `update()` method allows you to add multiple elements to a set by providing an iterable (e.g., a list, tuple, or another set).

```python
my_set = {1, 2, 3}
my_set.update([3, 4, 5])
print(my_set)  # Output: {1, 2, 3, 4, 5}
```

**Removing Elements:**

1. **`remove()` Method:** You can use the `remove()` method to remove a specific element from a set. If the element doesn't exist, it will raise a `KeyError`.

```python
my_set = {1, 2, 3, 4, 5}
my_set.remove(3)
print(my_set)  # Output: {1, 2, 4, 5}
```

2. **`discard()` Method:** The `discard()` method is similar to `remove()`, but it won't raise an error if the element is not found.

```python
my_set = {1, 2, 3, 4, 5}
my_set.discard(3)
print(my_set)  # Output: {1, 2, 4, 5}
```

3. **`pop()` Method:** The `pop()` method removes and returns an arbitrary element from the set. Since sets are unordered, the element removed is not guaranteed to be any specific one.

```python
my_set = {1, 2, 3, 4, 5}
removed_element = my_set.pop()
print(removed_element)  # Output: The removed element (e.g., 1, 2, 3, 4, or 5)
print(my_set)           # Output: The set with one less element
```

4. **`clear()` Method:** The `clear()` method removes all elements from a set, leaving it empty.

```python
my_set = {1, 2, 3, 4, 5}
my_set.clear()
print(my_set)  # Output: set()
```

Keep in mind that the methods like `remove()`, `discard()`, and `pop()` are applied to specific elements, so you need to know the element you want to remove. If you want to remove multiple elements or elements based on a condition, you might need to use other techniques like list comprehensions or loops.

---

4. *Can you perform set operations like union, intersection, difference, and symmetric difference in Python? Give examples.*

Yes, you can perform set operations like union, intersection, difference, and symmetric difference in Python using various methods provided by the built-in `set` data type. These operations allow you to combine, compare, and manipulate sets in different ways.

Here are the set operations you can perform:

1. **Union (`|`):** Returns a new set containing all elements that are in either of the sets.

```python
set1 = {1, 2, 3}
set2 = {3, 4, 5}
union = set1 | set2
print(union)  # Output: {1, 2, 3, 4, 5}
```

2. **Intersection (`&`):** Returns a new set containing all elements that are common to both sets.

```python
set1 = {1, 2, 3}
set2 = {3, 4, 5}
intersection = set1 & set2
print(intersection)  # Output: {3}
```

3. **Difference (`-`):** Returns a new set containing elements that are in the first set but not in the second set.

```python
set1 = {1, 2, 3, 4, 5}
set2 = {3, 4}
difference = set1 - set2
print(difference)  # Output: {1, 2, 5}
```

4. **Symmetric Difference (`^`):** Returns a new set containing elements that are in either of the sets, but not in both.

```python
set1 = {1, 2, 3, 4, 5}
set2 = {3, 4, 5, 6}
symmetric_difference = set1 ^ set2
print(symmetric_difference)  # Output: {1, 2, 6}
```

These set operations allow you to manipulate sets and create new sets with specific characteristics. You can use these operations to perform various tasks, such as filtering data, finding common elements, or computing differences between sets.

---

5. *Why can’t a set contain mutable elements like lists or dictionaries?*

In Python, sets are implemented as hash tables, and their elements must be hashable. Hashability is a fundamental requirement for elements in sets because it allows for efficient membership testing and handling of collisions in the hash table. Mutability of an object can introduce complications in maintaining the hashability property.

When you add an element to a set, the set calculates a hash value for that element and stores it in a way that allows for efficient lookups and membership testing. If the element is mutable (like a list or a dictionary), it means that its value can change after it's added to the set. This can lead to unexpected behavior and inefficiencies:

1. **Hash Value Changes:** If the mutable object's value changes, its hash value may also change. Since the hash value is used to determine the position of the element in the hash table, this could lead to incorrect or inconsistent behavior when trying to retrieve or delete elements from the set.

2. **Unpredictable Membership Testing:** The behavior of membership testing (`in` or `not in`) becomes unpredictable if an element's hash value changes. It may not be found in the set even though you expect it to be there.

3. **Hash Collisions:** Hash collisions occur when two different elements have the same hash value. Sets use hash values to quickly locate elements. With mutable elements, if the hash value changes, the set may not be able to locate the element correctly.

4. **Mutable Elements in Immutable Sets:** While mutable elements cannot be directly added to sets, you can add immutable objects (like tuples or strings) that contain mutable objects. However, modifying the mutable objects within these tuples or strings won't affect the hash value, as the outer container remains unchanged.

By requiring elements to be hashable and immutable, Python ensures that sets provide consistent and efficient behavior for membership testing and set operations. If you need to create a collection that contains mutable elements, you can use other data structures like lists or dictionaries.

---


## Dict (Dictionary)

1. *What is a dictionary in Python and when is it typically used?*

A dictionary in Python is a collection of key-value pairs used to store and retrieve data. It's often used when you need to associate values with unique keys for quick lookups and efficient data retrieval.

---

2. *How would you add a new key-value pair to a dictionary? How would you modify an existing key-value pair?

To add a new key-value pair to a dictionary, use the syntax: `dictionary[key] = value`.

To modify an existing key-value pair, assign a new value to the existing key: `dictionary[key] = new_value`.

Adding a new key-value pair:
```python
my_dict = {"name": "John", "age": 25}
my_dict["city"] = "New York"

print(my_dict) # my_dict = {"name": "John", "age": 25}
```

Modifying an existing key-value pair:
```python
my_dict["age"] = 26
```

---

3. *How can you access all keys, all values, and all key-value pairs in a dictionary?*

To access all keys, values, and pairs, you could use the following functions. 

Accessing all keys:
```python
my_dict = {"name": "John", "age": 25, "city": "New York"}
keys = my_dict.keys()
print(keys)  # Output: dict_keys(['name', 'age', 'city'])
```

Accessing all values:
```python
my_dict = {"name": "John", "age": 25, "city": "New York"}
values = my_dict.values()
print(values)  # Output: dict_values(['John', 25, 'New York'])
```

Accessing all key-value pairs:
```python
my_dict = {"name": "John", "age": 25, "city": "New York"}
items = my_dict.items()
print(items)  # Output: dict_items([('name', 'John'), ('age', 25), ('city', 'New York')])
```

---

4. *How would you handle a situation where you try to access a key that doesn’t exist in a dictionary?*

You can handle this situation using either the `get()` method or by using a try-except block. Here are both approaches:

Using the `get()` method:
```python
my_dict = {"name": "John", "age": 25}
value = my_dict.get("city", "Default City")
print(value)  # Output: Default City
```

Using a try-except block:
```python
my_dict = {"name": "John", "age": 25}
try:
    value = my_dict["city"]
except KeyError:
    value = "Default City"
print(value)  # Output: Default City
```

---

6. *How would you merge two dictionaries?*

You can use the `update()` method to merge one dictionary into another. Here's an example:

```python
dict1 = {"name": "John", "age": 25}
dict2 = {"city": "New York", "country": "USA"}

dict1.update(dict2)
print(dict1)  # Output: {'name': 'John', 'age': 25, 'city': 'New York', 'country': 'USA'}
```

This modifies `dict1` to include the key-value pairs from `dict2`.

---

7. *Describe a situation where it might be useful to use a dictionary comprehension.*

A situation where a dictionary comprehension might be useful is when you need to transform or filter the elements of an iterable (such as a list or another dictionary) and create a new dictionary based on those transformations or filters. This can help you create dictionaries more concisely and efficiently.

For example, suppose you have a list of students' scores and you want to create a dictionary where the keys are the student names and the values are their scores, but only for students who have passed (scores above a certain threshold):

```python
student_scores = {"Alice": 85, "Bob": 72, "Eve": 90, "Charlie": 65}
passing_threshold = 75

passed_students = {name: score for name, score in student_scores.items() if score >= passing_threshold}
print(passed_students)  # Output: {'Alice': 85, 'Eve': 90}
```

In this example, the dictionary comprehension filters out students who didn't pass and creates a new dictionary containing only the passed students' names and scores.

---

_This [link](overview.md) will bring you back to the main assessment._