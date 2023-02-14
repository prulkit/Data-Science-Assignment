## Ans1 
An exception is an event, which occurs during the execution of a program that disrupts the normal flow of the program's instructions. In general, when a Python script encounters a situation that it cannot cope with, it raises an exception. An exception is a Python object that represents an error.


Difference b/w error and exception

Syntax errors occur when the parser detects an incorrect statement while exception error occurs whenever syntactically correct Python code results in an error.

## Ans2
The runtime system will abort the program and an exception message will print to the console. 



## Ans 3
Try and except statements are used to catch and handle exceptions in python.


```python
try:
    numerator = 10
    denominator = 0

    result = numerator/denominator

    print(result)
except:
    print("Error: Denominator cannot be 0.")
```

    Error: Denominator cannot be 0.


## Ans 4


```python
## try and else
try:
    num = int(input("Enter a number: "))
    assert num % 2 == 0
except:
    print("Not an even number!")
else:
    reciprocal = 1/num
    print(reciprocal)
```

    Enter a number:  99


    Not an even number!



```python
## finally
try:
    numerator = 10
    denominator = 0

    result = numerator/denominator

    print(result)
except:
    print("Error: Denominator cannot be 0.")
    
finally:
    print("This is finally block.")
```

    Error: Denominator cannot be 0.
    This is finally block.



```python
## Raise
x = "hello"

if not type(x) is int:
    raise TypeError("Only integers are allowed")
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    Cell In[6], line 5
          2 x = "hello"
          4 if not type(x) is int:
    ----> 5     raise TypeError("Only integers are allowed")


    TypeError: Only integers are allowed


## Ans 5

In Python, we can define custom exceptions by creating a new class that is derived from the built-in Exception class. 



```python
# define Python user-defined exceptions
class InvalidAgeException(Exception):
    "Raised when the input value is less than 18"
    pass

# you need to guess this number
number = 18

try:
    input_num = int(input("Enter a number: "))
    if input_num < number:
        raise InvalidAgeException
    else:
        print("Eligible to Vote")
        
except InvalidAgeException:
    print("Exception occurred: Invalid Age")
```

    Enter a number:  10


    Exception occurred: Invalid Age


## Ans 6


```python
class SalaryNotInRangeError(Exception):
    """Exception raised for errors in the input salary.

    Attributes:
        salary -- input salary which caused the error
        message -- explanation of the error
    """

    def __init__(self, salary, message="Salary is not in (5000, 15000) range"):
        self.salary = salary
        self.message = message
        super().__init__(self.message)


salary = int(input("Enter salary amount: "))
if not 5000 < salary < 15000:
    raise SalaryNotInRangeError(salary)
```

    Enter salary amount:  200000000



    ---------------------------------------------------------------------------

    SalaryNotInRangeError                     Traceback (most recent call last)

    Cell In[8], line 17
         15 salary = int(input("Enter salary amount: "))
         16 if not 5000 < salary < 15000:
    ---> 17     raise SalaryNotInRangeError(salary)


    SalaryNotInRangeError: Salary is not in (5000, 15000) range



```python

```
