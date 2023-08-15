# Escape Sequences

An escape sequence is a combination of characters used in strings or character literals to represent certain special characters that have a specific meaning in programming languages. Escape sequences typically start with a backslash `\` followed by one or more characters. The backslash indicates that the character(s) following it should be treated differently from their literal interpretation. For example, common escape sequences in Python include:

- `"\n"`: Newline character (line feed)
- `"\t"`: Tab character
- `"\\"`: Backslash character itself
- `"\'"`: Single quote character
- `\""`: Double quote character

Escape sequences are useful for inserting special characters into strings that are not easily typable or may have different interpretations in code, like newline characters for formatting or quotes within a string.

Here are some examples of escape sequences.

```python
print("This '\n' is a newline.")
# This '
# ' is a newline.

print("This '\\n' is a newline.")
# This '\n' is a newline.

print('That\'s alright.')
# That's alright.
```

---

The following are some examples of a [[raw-strings|raw string]].

```python
>>> x = "C:\\Users\\public"
>>> x
# 'C:\\Users\\public'
>>>
>>> y = "C:\Users\public"
# line 1
#    y = "C:\Users\public"
#                         ^
# SyntaxError: (unicode error) 'unicodeescape' codec can't decode bytes in position 2-3: truncated \UXXXXXXXX escape
>>>
>>> y = r"C:\Users\public"
>>> y
# 'C:\\Users\\public'
```



#python #definition #string 
