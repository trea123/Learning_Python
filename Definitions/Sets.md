**Notes:**
- sets use curly bracets to list values

cs_courses = {'History', 'Math', 'Physics', 'CompSci', 'Math'}
art_courses = {'History', 'Math', 'Art', 'Design'}
Test to see if a value is in a set
print("Math" in cs_courses)

**show similarities between sets:**
print(cs_courses.intersection(art_courses))

**Show the difference between sets:**
print(cs_courses.difference(art_courses))

**show all specified sets as one:**
print(cs_courses.union(art_courses))

**create and empty set:**
empty_set = set()