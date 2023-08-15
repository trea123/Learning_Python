**Create a list:**
courses = ['History', 'Math', 'Physics', 'CompSci']
print(courses)

**Print the length of a list:**
print(len(courses))

**print specific objects in a list:**

Note:
- -1 index prints the last value of a list
- If the index specified does not exits, the output will be an error saying "List index out of range"

print(courses[0])
print(courses[-1])

**access a range of values in a list:**
print(courses[:2])
print(courses[2:])

**modify a list:**
courses.append('Art')
print(courses)

**Insert an object to a specif index in a list:**
courses.insert(0, 'English')
print(courses)

**add multiple values to a list:**
courses_2 = ['Gym', 'Music', 'Lunch']
courses.extend(courses_2)
print(courses)

**remove values from a list:**
courses.remove('Math')
print(courses)
popped = courses.pop()
print(courses)

**reverse a list:**
courses.reverse()
print(courses)

**sort a list(alphabetical or ascending order):**
courses.sort()
print(courses)
sort_nums = [1, 7, 3, 9, 4, 6, 2]
sort_nums.sort()
print(sort_nums)

**sort in descending order:**
sort_nums.sort(reverse=True)
courses.sort(reverse=True)
print(courses)
print(sort_nums)

**create a sorted funciton without modifying the original list:**
sorted_courses = sorted(courses)
print(courses)

**find the minimum and maximum and sum of numbers in a list:**
print(min(sort_nums))
print(max(sort_nums))
print(sum(sort_nums))

**find the index of a value in a list:**
print(courses.index('CompSci'))

**output boolian values of wether a value is in a lists:**
print('CompSci' in courses)
print('Math' in courses)

**for loop:**
for item in courses:
print(item)

**use a for loop to print each index as well as the value:**

note:
- you can have the index start at a specific place

for course in enumerate(courses, start=1):
	print(course)

**turn a list into strings:**
course_str = ', '.join(courses)
print(course_str)

**turn a string into a list:**
new_list = course_str.split(', ')
print(new_list)

**create an empty list:**
empty_list = []