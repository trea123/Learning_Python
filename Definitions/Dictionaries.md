**Create a dictionary:**
student = {'name': 'John', 'age': 25, 'courses': ['Math', 'CompSci']}

**Print specific keys of a dictionary:**
print(student['name'])
print(student['age'])
print(student['courses'])

**alternative to printing specific keys:**
print(student.get('name'))

**Add and update keys in an existing dictionary:**
student['phone'] = '555-5555'
student['name'] = 'Tyler'
print(student)

**Alternative to updating values in a dictionary:**
student.update({'name': 'Jane', 'age': 26, 'height': '5 feet'})
print(student)

**delete keys from a dictionary:**
del student['height']
print(student)

**alternative to deleting keys in a dictionary:**
age = student.pop('age')
print(student)
print(age)

**loop through all keys in a dictionary:**
print(len(student))
print(student.keys())
print(student.values())
print(student.items())
for key in student.items():
	print(key)