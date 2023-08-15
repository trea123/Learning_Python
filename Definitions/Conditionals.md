**Comparisons:**
- Equal:            ==
- Not Equal:        !=
- Greater Than:     >
- Less Than:        <
- Greater or Equal: >=
- Less or Equal:    <=
- Object Identity:  is

**Boolean operations:**
- and
- or
- not

  
language = 'Python'

**if statements:**
if language == 'Python':
	print('Conditional was true')

**else statements:**
if language == 'Python':
	print('Language is Python')
else:
	print('No match')

**elif statements:**
if language == 'Python':
	print('Python')
elif language == 'Java':
	print('Java')
else:
print('none')

user = 'Admin'
logged_in = True

**and statement:**
if user == 'Admin' and logged_in:
	print('Admin Page')
else:
	print('Bad creds')

**not statement:**
if not logged_in:
	print('Please Log In')
else:
	print('Welcome')

**is statements:**
a = [1, 2, 3]
 b = [1, 2, 3]
print(id(a))
print(id(b))
print(a is b)

a = [1, 2, 3]
b = a
print(id(a))
print(id(b))
print(a is b)

**false conditional examples:**
- False
- None
- Zero of any numeric type
- Any empty sequence. For example, '', (), [].
- Any empty mapping. For example, {}.

condition = None

if condition:
	print('Evaluated to True')
else:
	print('Evaluated to False')