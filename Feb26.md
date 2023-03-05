Consider the below code to answer further questions:
import numpy as np
list_ = [ ‘1’ , ’2’ , ‘3’ , ‘4’ , ‘5’ ]
array_list = np.array(object = list_)

Q1. Is there any difference in the data type of variables list_ and array_list? If there is then write a code
to print the data types of both the variables.

Q2. Write a code to print the data type of each and every element of both the variables list_ and
arra_list.

Q3. Considering the following changes in the variable, array_list:
array_list = np.array(object = list_, dtype = int)
Will there be any difference in the data type of the elements present in both the variables, list_ and
arra_list? If so then print the data types of each and every element present in both the variables, list_
and arra_list.
Consider the below code to answer further questions:
import numpy as np
num_list = [ [ 1 , 2 , 3 ] , [ 4 , 5 , 6 ] ]
num_array = np.array(object = num_list)

Q4. Write a code to find the following characteristics of variable, num_array:
(i) shape
(ii) size

Q5. Write a code to create numpy array of 3*3 matrix containing zeros only, using a numpy array
creation function.
[Hint: The size of the array will be 9 and the shape will be (3,3).]

Q6. Create an identity matrix of shape (5,5) using numpy functions?
[Hint: An identity matrix is a matrix containing 1 diagonally and other elements will be 0.]

## Ans 1
Yes, there is a difference in data type of variables.


```python
import numpy as np
list_ = [ '1' , '2' , '3' , '4' , '5' ]
array_list = np.array(object = list_)
```


```python
type(array_list)
```




    numpy.ndarray




```python
type(list_)
```




    list



## Ans 2


```python
for x in list_:
    print(type(x))
```

    <class 'str'>
    <class 'str'>
    <class 'str'>
    <class 'str'>
    <class 'str'>



```python
for x in array_list:
    print(type(x))
```

    <class 'numpy.str_'>
    <class 'numpy.str_'>
    <class 'numpy.str_'>
    <class 'numpy.str_'>
    <class 'numpy.str_'>


## Ans 3
Yes there will a difference between data type of elements present in both the variables. 


```python
array_list = np.array(object = list_, dtype = int)
```


```python
for x in list_:
    print(type(x))
    
for x in array_list:
    print(type(x))    
```

    <class 'str'>
    <class 'str'>
    <class 'str'>
    <class 'str'>
    <class 'str'>
    <class 'numpy.int64'>
    <class 'numpy.int64'>
    <class 'numpy.int64'>
    <class 'numpy.int64'>
    <class 'numpy.int64'>


## Ans 4


```python
import numpy as np
num_list = [ [ 1 , 2 , 3 ] , [ 4 , 5 , 6 ] ]
num_array = np.array(object = num_list)

print("Shape of num_array :", num_array.shape) 
print("Size of num_array :", num_array.size) 
```

    Shape of num_array : (2, 3)
    Size of num_array : 6


## Ans 5


```python
np.zeros((3,3))
```




    array([[0., 0., 0.],
           [0., 0., 0.],
           [0., 0., 0.]])



## Ans 6


```python
np.identity(5)
```




    array([[1., 0., 0., 0., 0.],
           [0., 1., 0., 0., 0.],
           [0., 0., 1., 0., 0.],
           [0., 0., 0., 1., 0.],
           [0., 0., 0., 0., 1.]])




```python

```
