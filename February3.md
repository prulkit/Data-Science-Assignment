Q1. Which keyword is used to create a function? Create a function to return a list of odd numbers in the
range of 1 to 25.

Q2. Why *args and **kwargs is used in some functions? Create a function each for *args and **kwargs to
demonstrate their use.

Q3. What is an iterator in python? Name the method used to initialise the iterator object and the method
used for iteration. Use these methods to print the first five elements of the given list [2, 4, 6, 8, 10, 12, 14, 16,
18, 20].

Q4. What is a generator function in python? Why yield keyword is used? Give an example of a generator
function.

Q5. Create a generator function for prime numbers less than 1000. Use the next() method to print the
first 20 prime numbers.

## Ans 1. def() is used to create a function.


```python
## function that returns list of odd numbers in the range of 1 to 25. 
def test1():
    for i in range(1,25,2):
        print (i)
```


```python
test1()
```

    1
    3
    5
    7
    9
    11
    13
    15
    17
    19
    21
    23


## Ans 2
*args and **kwargs are used when we are unsure about the number of arguments to pass in the functions.



```python
## *args
def list(*num):
    sum = 0
    
    for n in num:
        sum = sum + n

    print("Sum:",sum)
```


```python
list(2,3,4,5,6,7,8,9,10)
```


```python
## *kwargs
def intro(**data):
    print("\nData type of argument:",type(data))

    for key, value in data.items():
        print("{} is {}".format(key,value))
```


```python
intro(Firstname="Pulkit", Lastname="Singhvi", Age=22, Phone=99990347374)
```


```python

```

### Ans 3
Iterator in Python is an object that is used to iterate over iterable objects like lists, tuples, dicts, and sets. 
The method used to initialise the iterator object and the method used for iteration are iter() and next() respectively.



```python
list = [2, 4, 6, 8, 10, 12, 14, 16, 18, 20]
iter1 = iter(list)
print(next(iter1))
print(iter1.__next__())
print(next(iter1))
print(next(iter1))
print(next(iter1))

```

    2
    4
    6
    8
    10


### Ans 4.
A generator is a function that returns an iterator that produces a sequence of values when iterated over.
Generators are useful when we want to produce a large sequence of values, but we don't want to store all of them in memory at once.

Yield keyword is used to create a generator function. A type of function that is memory efficient and can be used like an iterator object.


```python
def table(n):
    for i in range(1,11):
        yield n*i
        i = i+1        

```


```python
for i in table(10):
    print(i)
```

    10
    20
    30
    40
    50
    60
    70
    80
    90
    100


## Ans 5


```python
def isPrime(num):
    for i in range(2,num):
        if num%1 ==0:
            return False
        return True
```


```python
def prime_num(n):
    num=2
    while n:
        if isPrime(num):
            yield num
            n=-1
            num+=1
            return
```


```python
prime = prime_num(10)
for i in prime:
    print(i)
```


```python

```
