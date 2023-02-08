1. Write a program to accept percentage from the user and display the grade according to the following 
2. Write a program to accept the cost price of a bike and display the road tax to be paid according to the 
   following criteria: 
3. Accept any city from the user and display monuments of that city. 
4. Check how many times a given number can be divided by 3 before it is less than or equal to 10. 
5. Why and When to Use while Loop in Python give a detailed description with example 
6. Use nested while loop to print 3 different pattern. 
7. Reverse a while loop to display numbers from 10 to 1. 
8. Reverse a while loop to display numbers from 10 to 1 


```python
## Answer1

marks=int(input("Enter your makrs"))
if marks > 90 :
    print ("Grade A")
elif marks > 80 and marks <= 90 :
        print ("Grade B")
elif marks >= 60 and marks< 80 :
         print("Grade C")
else:
         print("Grade D")
```

    Enter your makrs 80


    Grade D



```python
## Answer 2
cost_bike = int(input("Enter price"))
if cost_bike > 100000 :
    print (cost_bike*0.15)
elif cost_bike > 50000 and cost_bike <= 100000 :
    print (cost_bike*0.10)
elif cost_bike <= 50000:
        print (cost_bike*0.05)
```

    Enter price 10000


    500.0



```python
## Answer 3

city = (input("Enter city"))
if city == "Delhi":
    print("Red fort")
elif city == "Agra":
    print("Taj Mahal")
elif city == "Jaipur":
    print("Jal Mahal")
else :
    print("Mujhe nahi pata h mujhse mat pucho na")
```

    Enter city Goro


    Mujhe nahi pata h mujhse mat pucho na



```python
## Answer 4
n = int(input("Enter number"))
ans=0
while n > 10:
    n/=3
    ans+=1
print(ans)
```

## Answer 5
Loops are used to repeat the same code a number of times. This number of number times could be specific to
a certain nnumber


```python
## Example while loop
a= 2
while a<10:
    print(a)
    i+=1
```


```python
## Answer 6
num = int(input("Enter number of rows"))
i = 1
while i<=n:
    j=1
    while j<=i:
        print ("*",end=" ")
        j+=1
        print()
        i+=1
```


```python
num = int(input("Enter number of rows"))
i = 1
while i<=n:
    j=1
    while j>=i:
        print ("*",end=" ")
        j-=1
        print()
        i+=1
```


```python
rows =5
i=1
whilei<=rows:
    j=i
    while j<rows:
        print(" ",end=" ")
        j+=1
    k=1
    while k<=1
    print()
    i+=1
    
i=rows
while i>=1:
    j=i
    while j<= rows:
        print(" ", end = " ")
        j+=1
        k=1
        while k<i:
            print("*", end=" ")
            k+=1
            print("")
            i-=1
```


```python

```


```python
## Answer 7
## int = (1,2,3,4,5,6,7,8,9,10)
while int == range(1,10):
    print(int,-1)
```


```python
## Answer 8
## int = (1,2,3,4,5,6,7,8,9,10)
while int == range(1,10):
    print(int,-1)
```


```python

```
