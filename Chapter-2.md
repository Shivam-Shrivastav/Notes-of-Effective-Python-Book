## Chapter 2: List and Dictionaries

-  Prefer Catch-All Unpacking Over Slicing

Eg:
Newbie:
```
car_ages = [0, 9, 4, 8, 7, 20, 19, 1, 6, 15]
car_ages_descending = sorted(car_ages, reverse=True)
oldest, second_oldest = car_ages_descending

oldest = car_ages_descending[0]
second_oldest = car_ages_descending[1]
others = car_ages_descending[2:]
print(oldest, second_oldest, others)

```
output-->20 19 [15, 9, 8, 7, 6, 4, 1, 0]


Pro:
```
oldest, second_oldest, *others = car_ages_descending # *other catch up all unpacked elements in a list
print(oldest, second_oldest, others)
```


output>>> 20 19 [15, 9, 8, 7, 6, 4, 1, 0]

- Prefer defaultdict Over setdefault to Handle Missing Items in Internal State
