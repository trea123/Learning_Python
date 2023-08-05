**Holding values:**
message = 'Hello world'
name = 'John'

**printing outputs:**
print(message)

**Find the length of a string contained in a value(characters):**
print(len(message))

**access index (specific characters) of a value:**
print(message[0])
print(message[-1])

**output a range of an index(multiple ways)**
print(message[0:5])
print(message[:5])
print(message[6:])

**Output all lowercase:**
print(message.lower())

**output all uppercase:**
print(message.upper())

**count the amount of times an arguement comes up in a value:**
print(message.count('o'))

**find the index at which a value is stored:**
if it doesn't exist, the output is -1
print(message.find('W'))

**replace parts of a value:**
print(message.replace('World', 'Universe'))

**concatinate multiple strings**
message = f'{message}, {name}. Welcome!.'
print(message)

**show all attributes and methods a variable is able to access:**
print(dir(name))

**get help on what a variable does:**
print(help(str.lower))
