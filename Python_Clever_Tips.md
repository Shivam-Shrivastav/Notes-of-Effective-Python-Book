### Tip-1: Multiple input at once

```
x, y, z, p, q, r = input("Enter numbers with spaces: ").split()
print(x, y, z, p, q, r)
```

### Tip-2: Fullfilling many conditions

```
subs = 2400
likes = 200
comments = 56

conditions = [ subs > 20, likes > 50, comments > 10]

if all(conditions): # all for and
	print('Awesome Video')

if any(conditions): # all for or
	print('Awesome Video')

```

### Tip-3 Passing multiple parameters to a fuction

```
def sum (*a):
	result = 0
	for i in a:
		result = result + i
	return result

res = sum(2, 3, 4, 5)

print(res)

output: 14
```

### Tip-4 Use interative shell to access function and variable in terminal using:

```
python -i file_name.py
```

### Tip-5 Debug your code in terminal by import pdb in your code

### Tip-6 You can use lambda, map and filter for one liner code

### Tip-7 Use underscore as comma to read a very large number

```
num1 = 10_00_000 # 10,00,000 - 10 Lakh _ is working as , here
```

### Tip-8 Use enumerate method to iterate index and a certain list simultaneously

```
heroes = ['Peter', 'Bruce', 'Tony', 'Levi']

for idx, name in enumerate(heroes):
	print(f'{idx}: {name}')

```

### Tip-9 Use zip function to iterate over two or more list simultaneously

```
names = ['peter', 'tony', 'bruce']
heroes = ['spiderman', 'ironman', 'batman']

for name, hero in zip(names, heroes):
	print(f'{name} is actually {hero}')
```

### Tip-10 Use getpass function to mask the password when you are accepting password as input

```
from getpass import getpass

username = input("Username: ")
password = getpass("Password: ")

print("Logging In...")
```
