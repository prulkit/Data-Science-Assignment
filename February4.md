Q1. Create a python program to sort the given list of tuples based on integer value using a
lambda function.
[('Sachin Tendulkar', 34357), ('Ricky Ponting', 27483), ('Jack Kallis', 25534), ('Virat Kohli', 24936)]

Q2. Write a Python Program to find the squares of all the numbers in the given list of integers using
lambda and map functions.
[1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

Q3. Write a python program to convert the given list of integers into a tuple of strings. Use map and
lambda functions
Given String: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
Expected output: ('1', '2', '3', '4', '5', '6', '7', '8', '9', '10')

Q4. Write a python program using reduce function to compute the product of a list containing numbers
from 1 to 25.

Q5. Write a python program to filter the numbers in a given list that are divisible by 2 and 3 using the
filter function.
[2, 3, 6, 9, 27, 60, 90, 120, 55, 46]

Q6. Write a python program to find palindromes in the given list of strings using lambda and filter
function.
['python', 'php', 'aba', 'radar', 'level']

## Ans1 


```python
player = [('Sachin Tendulkar', 34357), ('Ricky Ponting', 27483), ('Jack Kallis', 25534), ('Virat Kohli', 24936)]
```


```python
player.sort(key= lambda a: a[1])
print(player)
```

    [('Virat Kohli', 24936), ('Jack Kallis', 25534), ('Ricky Ponting', 27483), ('Sachin Tendulkar', 34357)]


## Ans 2


```python
number = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
```


```python
list(map(lambda x: x**2,number))
```




    [1, 4, 9, 16, 25, 36, 49, 64, 81, 100]



## Ans 3


```python
String = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10] 
tuple (map(lambda x: str(x),String))
```




    ('1', '2', '3', '4', '5', '6', '7', '8', '9', '10')



## Ans 4


```python
from  functools import reduce
lst1= [1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20,21,22,23,24,25]
reduce(lambda x,y : x*y,lst1)
```




    15511210043330985984000000



## Ans 5


```python
l = [2, 3, 6, 9, 27, 60, 90, 120, 55, 46]
list(filter(lambda x: x%2==0 and x%3 ==0,l))
```




    [6, 60, 90, 120]



## Ans 6


```python
lst = ['python', 'php', 'aba', 'radar', 'level']
list(filter(lambda x: x == "".join(reversed(x)),lst ))
```




    ['php', 'aba', 'radar', 'level']




```python


```


```python

```
