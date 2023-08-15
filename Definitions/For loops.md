nums = [1, 2, 3, 4, 5]

**for loops:**
for num in nums:
	print(num)

**break statement:**
for num in nums:
	if num == 3:
		print('found 3')
		break
print(num)

**Continue statement:**
for num in nums:
	if num == 3:
		print('found 3')
		continue
	print(num)

**loop within a loop:**
for num in nums:
	for letter in 'abc':
		print(num, letter)

**loop a specific amount of times:**
for i in range(1, 10):
	print(i)