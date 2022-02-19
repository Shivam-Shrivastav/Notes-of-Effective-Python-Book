
## Chapter 1: Python Thinking

- Follow the PEP 8 Style Guide

- Self is for Instance object, cls is for class method.

- Binary sequence!=string sequence use .encode('utf-8') to encode string to binary sequence and .decode('utf-8')

- use f'' (fstring) for formatting

- Move complex expressions into helper functions, especially if you need to use the same logic repeatedly.

- Prefer Multiple Assignment Unpacking Over Indexing
Eg:
Newbie:
```
snacks = [('bacon', 350), ('donut', 240), ('muffin', 190)]
for i in range(len(snacks)):
 item = snacks[i]
 name = item[0]
 calories = item[1]
 print(f'#{i+1}: {name} has {calories} calories')
 ```

Pro:
```
for rank, (name, calories) in enumerate(snacks, 1): # name, calories = snack ---> This is called Unpacking
 print(f'#{rank}: {name} has {calories} calories')
```

- Prefer enumerate instead of looping over a range and indexing into a 
sequence.

- If you have two or more related list, you can iterate them parallely with zip function
Eg:
Newbie:
```
names = ['Cecilia', 'Lise', 'Marie']
counts = [len(n) for n in names]
print(counts)
```
>>>
[7, 4, 5]
```
for i in range(len(names)):
 count = counts[i]
 if count > max_count:
 longest_name = names[i]
 max_count = count

print(longest_name)
```
>>>
Cecilia

Pro:
```
for name, count in zip(names, counts):
 if count > max_count:
 longest_name = name
 max_count = count
```

- Use the walrus operator (:=) to both assign and evaluate variable names in a single expression, thus reducing repetition.
Eg:
Newbie:
```
count = fresh_fruit.get('lemon', 0)
if count:
 make_lemonade(count)
else:
 out_of_stock()
```

here we are firstly assigning the count variable then evaluating it in the next line
this can be done in one line

Pro:
```
if count := fresh_fruit.get('lemon', 0):
 make_lemonade(count)
else:
 out_of_stock()
```










