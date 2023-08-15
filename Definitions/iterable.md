# Iterable

An iterable is an object that can be iterated over, meaning you can loop through its elements one at a time. This is typically achieved using constructs like "for" loops. Iterables are an essential part of the Python language and are used extensively for working with collections of data.

Common examples of iterables in Python include lists, tuples, strings, dictionaries, sets, and more. When you iterate over an iterable, you can access each element sequentially and perform operations on them without needing to manually manage the underlying structure of the data.

Here's a simple example using a list as an iterable:

```python
my_list = [1, 2, 3, 4, 5]
for item in my_list:
    print(item)
```

In this code, `my_list` is an iterable, and the "for" loop iterates through each element in the list, printing them one by one.

Python also provides the concept of iterators, which are objects that facilitate the iteration process. Iterators are used behind the scenes when you loop over an iterable. An iterator implements methods like `__iter__()` and `__next__()` to control the iteration process. However, for most practical purposes, you can work with iterables directly using "for" loops and other iteration constructs.

#definition #python 