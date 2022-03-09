## Functions

- Use atmost three variables for unpacking

- Prefer Raising Exceptions over Returning None

EG:

NEWBIE:

```
def careful_divide(a, b):
 try:
 return a / b
 except ZeroDivisionError:
 return None

 x, y = 1, 0
result = careful_divide(x, y)
if result is None:
 print('Invalid inputs')
 ```


PRO:

```
def careful_divide(a, b):
 try:
 return a / b
 except ZeroDivisionError as e:
 raise ValueError('Invalid inputs') # Raised Exception

```


- Closure: A Closure is a function object that remembers values in enclosing scopes even if they are not present in memory

- In the Closure process we can call the inner function which is in enclosing scope

EG:
```
def outer():
	msg = "hello"
	def inner():
		print(msg)
	return inner #reference of inner function

a = outer() 
a() # Calling the inner function by its reference

```

-  Reduce Visual Noise with Variable Positional Arguments

Eg:

NEWBIE:

```
def log(message, values):
 if not values:
 print(message)
 else:
 values_str = ', '.join(str(x) for x in values)
 print(f'{message}: {values_str}')
log('My numbers are', [1, 2])
log('Hi there', [])
```

Output: 
My numbers are: 1, 2
Hi there


PRO:

```
def log(message, *values): # The only difference
 if not values:
 print(message)
 else:
 values_str = ', '.join(str(x) for x in values)
 print(f'{message}: {values_str}')
log('My numbers are', 1, 2)
log('Hi there') # Much better
```
Output:
My numbers are: 1, 2
Hi there