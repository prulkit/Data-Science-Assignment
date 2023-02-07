1.	What are the characteristics of the tuples? Is tuple immutable?
2.	What are the two tuple methods in python? Give an example of each method. Give a reason why tuples have only two in-built methods as compared to Lists.
3.	Which collection datatypes in python do not allow duplicate items? Write a code using a set to remove duplicates from the given list.
      List = [1, 1, 1, 2, 1, 3, 1, 4, 2, 1, 2, 2, 2, 3, 2, 4, 3, 1, 3, 2, 3, 3, 3, 4, 4, 1, 4, 2, 4, 3, 4, 4]
  
4.	Explain the difference between the union() and update() methods for a set. Give an example of each method.
5.	What is a dictionary? Give an example. Also, state whether a dictionary is ordered or unordered.
6.	Can we create a nested dictionary? If so, please give an example by creating a simple one-level nested dictionary.
7.	Using setdefault() method, create key named topics in the given dictionary and also add the value of the key as this list                                                    ['Python', 'Machine Learning’, 'Deep Learning']
            dict1 = {'language' : 'Python', 'course': 'Data Science Masters'}
8.	 What are the three view objects in dictionaries? Use the three in-built methods in python to display these three view objects for the given dictionary.

     dict1 = {'Sport': 'Cricket' , 'Teams': ['India', 'Australia', 'England', 'South Africa', 'Sri Lanka', 'New Zealand']}'''
     

### Answer1 

Ans 1. Tuple is a collection of values separated by comma and enclosed in parenthesis. 
Characteristics 
●	Tuple are immutable.
●	Tuple contains elements in order.
●	Indexing/slicing is possible.
●	Allowes duplicate elements.

Yes, tuple is immutable.


## Answer 2
There are only two tuple methods count() and index() that a tuple object can call.
Tuple has only two built-in functions because of immutability hence it doesn't allow much operations.


```python
## count ()  
fruits = ('a', 'p', 'p', 'l', 'e',)
print(fruits.count('p'))  
print(fruits.index('l'))  
```

    2
    3



```python
## index ()
letters = ("p", "u", "l", "k", "i", "t")
print(letters[0]) 
```

    p


## Answer 3
Set, dictionary do no allow duplicate items.


```python

List = {1, 1, 1, 2, 1, 3, 1, 4, 2, 1, 2, 2, 2, 3, 2,4, 3, 1, 3, 2, 3, 3, 3, 4, 4, 1, 4, 2, 4, 3, 4, 4}

```


```python
List
```




    {1, 2, 3, 4}



## Answer 4
Both update() and union() perform the union operation. However, update() adds all missing elements to the 
set on which it is called whereas union() creates a new set. Consequently, the return value of update() is None 
and the return value of union() is a set.


```python
## Example
##Update
set = {1, 2, 3}
set.update ({4, 5})

```


```python
set
```




    {1, 2, 3, 4, 5}




```python
##  Union
s = {1, 2, 3}
s.union({4, 5})
```




    {1, 2, 3, 4, 5}



##  Answer 5
The dictionary is a useful data structure for storing (key, value) pairs.  
Dictionary is ordered.



```python
marks = {"sohan" : 38, "mohan" : 39, "rohan" : 40}
```


```python
marks
```




    {'sohan': 38, 'mohan': 39, 'rohan': 40}



## Answer 6 
Yes, we can create a nested dictionary.

nested_dict = { 'dictA': {'key_1': 'value_1'}

'dictB': {'key_2': 'value_2'}}


```python
## Example: 
people = {1: {'name': 'Tony', 'age': '27', 'sex': 'Male'},
            2: {'name': 'Bunty', 'age': '22', 'sex': 'Male'}}
```


```python
people
```




    {1: {'name': 'Tony', 'age': '27', 'sex': 'Male'},
     2: {'name': 'Bunty', 'age': '22', 'sex': 'Male'}}



## Answer 7


```python
dict1 = {'language':'Python','course':'Data Science Masters'}
dict1.setdefault('Topics',['Python','Machine Learning','Deep Learning'])
print(dict1)

```

    {'language': 'Python', 'course': 'Data Science Masters', 'Topics': ['Python', 'Machine Learning', 'Deep Learning']}


## Answer 8
The objects returned by dict.keys(), dict.values(), and dict.items() are view objects.


```python
dict1 = {'Sport': 'Cricket' , 'Teams': ['India', 'Australia', 'England', 'South Africa', 'Sri Lanka', 'New Zealand']} 
```


```python
dict1.items()
```




    dict_items([('Sport', 'Cricket'), ('Teams', ['India', 'Australia', 'England', 'South Africa', 'Sri Lanka', 'New Zealand'])])




```python
dict1.values()
```




    dict_values(['Cricket', ['India', 'Australia', 'England', 'South Africa', 'Sri Lanka', 'New Zealand']])




```python
dict1.keys()
```




    dict_keys(['Sport', 'Teams'])




```python

```
