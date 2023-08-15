**Create a function:**
def hello_func():
	print('Hello function!')
	
def hello_func2():
	return 'Hello function'

** executing the function:**
hello_func()
print(hello_func2().upper())

**pass a parameter into a function:**
def exa_param(greeting, name = 'You'):
	return '{}, {}'.format(greeting, name)
		print(exa_param('Hi', name = 'John'))

Note:
- arguments(args) and positional keyword arguements(kwargs)

def student_info(*args, **kwargs):
	print(args)
	print(kwargs)

**pass in args(1st line) and kwargs(2nd line):**
student_info('Math', 'Art', name='John', age=22)

**pass variables as args and kwargs into the function:**
courses = ['Math', 'Art']
info = {'nam': 'John', 'age': 22}
student_info(*courses, **info)