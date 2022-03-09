## Comprehensions and Generators

- Use Comprehension instead of map and filter

EG:

NEWBIE:


```
a = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
squares = []
for x in a:
 squares.append(x**2)
print(squares)
```

PRO:


```
squares = [x**2 for x in a] # List comprehension
print(squares)
```

NEBIE:

```
alt = map(lambda x: x**2, filter(lambda x: x % 2 == 0, a))
assert even_squares == list(alt)
```


PRO:

```
even_squares = [x**2 for x in a if x % 2 == 0]
print(even_squares)
```

Dictionaries and Set Comprehension Examples:


```
even_squares_dict = {x: x**2 for x in a if x % 2 == 0}
threes_cubed_set = {x**3 for x in a if x % 3 == 0}
print(even_squares_dict)
print(threes_cubed_set)
```

Output:
```
{2: 4, 4: 16, 6: 36, 8: 64, 10: 100}
{216, 729, 27}
```




- Consider Generators instead of returning List






