Q1. You are writing code for a company. The requirement of the company is that you create a python
function that will check whether the password entered by the user is correct or not. The function should
take the password as input and return the string “Valid Password” if the entered password follows the
below-given password guidelines else it should return “Invalid Password”.
Note: 
1. The Password should contain at least two uppercase letters and at least two lowercase letters.
2. The Password should contain at least a number and three special characters.
3. The length of the password should be 10 characters long.
Q2. Solve the below-given questions using at least one of the following:
1. Lambda functioJ
2. Filter functioJ
3. Zap functioJ
4. List ComprehensioI
B Check if the string starts with a particular letterY
B Check if the string is numericY
B Sort a list of tuples having fruit names and their quantity. [("mango",99),("orange",80), ("grapes", 1000)-
B Find the squares of numbers from 1 to 10Y
B Find the cube root of numbers from 1 to 10Y
B Check if a given number is evenY
B Filter odd numbers from the given list.
[1,2,3,4,5,6,7,8,9,10-
B Sort a list of integers into positive and negative integers lists.
[1,2,3,4,5,6,-1,-2,-3,-4,-5,0]

## Ans 1


```python
l,u,p,d = 0,0,0,0
pass1 = input()
caps = "ABCDEFGHIJKLMNOPQRRSTUVWX"
smalls = "abcdefghijklmnopqrstuvwxyz"
specials = "$@_"
digits = "0123456789"
if (len(pass1) >=10) :
    for i in pass1:
        if (i in smalls):
            l+=1
        
        if(i in caps):
            u+=1
            
            if (i in digits):
                d+=1
                
                if(i in specials):
                    p+=1
                    
if(l>=1 and u>=1 and p>=1 and d>=1 and l+u+p+d==len):
    print("Valid password")
else :
    print("Invalid password")
```

     webiu8@nfkn


    Invalid password


## Ans2


```python
## Check if the string starts with a particular letter

names = ["mohan","manmeet","martin","narung"]
letter = "m"
name = list(filter(lambda x : x.startswith(letter),names))
print(name)
```

    ['mohan', 'manmeet', 'martin']



```python
## Check if the string is numeric
number = "12345"
print(number.isnumeric())
```

    True



```python
##  Sort a list of tuples having fruit names and their quantity
fruits = [("mango",99),("orange",80), ("grapes", 1000)]
fruits.sort(key = lambda x : x[1])
print(fruits)
```

    [('orange', 80), ('mango', 99), ('grapes', 1000)]



```python
## Find the squares of numbers from 1 to 10
l = [1,2,3,4,5,6,7,8,9,10]
list(map(lambda x : x**2,l))
```




    [1, 4, 9, 16, 25, 36, 49, 64, 81, 100]




```python
## Find the cubes of numbers from 1 to 10
l = [1,2,3,4,5,6,7,8,9,10]
list(map(lambda x : x**3,l))
```




    [1, 8, 27, 64, 125, 216, 343, 512, 729, 1000]




```python
## Filter odd numbers from the given list. 
lst = [1,2,3,4,5,6,7,8,9,10]
list(map(lambda x : x%2 != 0,lst))
```




    [True, False, True, False, True, False, True, False, True, False]




```python
## Sort a list of integers into positive and negative integers lists. 
lst1 = [1,2,3,4,5,6,-1,-2,-3,-4,-5,0]
list(filter(lambda x : x>0,lst1))
```




    [1, 2, 3, 4, 5, 6]




```python
lst1 = [1,2,3,4,5,6,-1,-2,-3,-4,-5,0]
list(filter(lambda x : x<0,lst1))
```




    [-1, -2, -3, -4, -5]




```python

```
