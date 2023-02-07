Q1. Explain Class and Object with respect to Object-Oriented Programming. Give a suitable example.

Q2. Name the four pillars of OOPs.

Q3. Explain why the __init__() function is used. Give a suitable example.

Q4. Why self is used in OOPs?

Q5. What is inheritance? Give an example for each type of inheritance.

## Ans1
Class
A class encapsulates data and functionality - data as
attributes, and functionality as methods. It is a blueprint
to create concrete instances in the memory. Created only once and declared using class keyword.

Example : class dataset {}

Object
A piece of encapsulated data with functionality in your Python program that
is built according to a class definition. Can be created multiple times.

Example : dataset d1 = new datset():


## Ans 2
Four pillars of OOPS are as follow:
1. Inheritence
2. Encapsulation
3. Abstraction 
4. Polymorphism

## Ans 3
__in__it () function is executed when a class is being initiated. It is used to assign values to object properties 
or other operations that are necessary to do when the object is created.


```python
class dataset:
    def __init__(self, name, salary):
        self.name = name
        self.salary = salary
d1 = dataset("Pulkit",70000)
d2 = dataset("Nupur",80000 )
```


```python
d1.name
```




    'Pulkit'




```python
d2.name
```




    'Nupur'



## Ans 4
The first argument when defining any method is always the self argument.
This argument specifies the instance on which you call the method.
self gives the Python interpreter the information about the concrete
instance. To define a method, you use self to modify the instance
attributes. But to call an instance method, you do not need to specify self.

## Ans 5
Inheritence is defined as mechanism where the sub class inherits the properties and characteristics of the other derived class.
It also supports additional features of extracting properties from the child classs and using it into other derived class.
There are 4 types of inheritence. 


```python
## 1.Single Inheritence
## When child class is derived from only one parent class. This is called single inheritance.

class schools :
    school1 = "KVS"
    school2 = "DPS"
    
class students(schools) :
    stu1 = "Manan"
    stu2 = "Naman"
    
obj1 = students()
print(obj1.stu1+" is student of "+ obj1.school1 )
print(obj1.stu2+" is student of "+ obj1.school2 )
```

    Manan is student of KVS
    Naman is student of DPS



```python
## 2.Multiple inheritence
## When child class is derived or inherited from more than one parent class. This is called multiple inheritance.
## In multiple inheritance, we have two parent classes/base classes and one child class that inherits both parent classes properties.

class schools :
    school1 = "KVS"
    school2 = "DPS"
    
class students(schools) :
    stu1 = "Manan"
    stu2 = "Naman"
    
class place(students,schools) :
    place1 = " Delhi"
    place2 = " Noida"
    
obj1 = place()
print(obj1.stu1+" is student of "+ obj1.school1 + obj1.place1 )
print(obj1.stu2+" is student of "+ obj1.school2 + obj1.place2 )
```

    Manan is student of KVS Delhi
    Naman is student of DPS Noida



```python
## 3. Multilevel Inheritence
## In multilevel inheritance, we have one parent class and child class that is derived or inherited from that parent class.
## We have a grand-child class that is derived from the child class. See the below-given flow diagram to understand more clearly.

class schools :             ##parent
    school1 = "KVS"
    school2 = "DPS"
    
class students(schools) :
    stu1 = "Manan"           ##child
    stu2 = "Naman"
    
class place(students,schools) :
    place1 = " Delhi"         ##grandchild  
    place2 = " Noida"
    
obj1 = place()
print(obj1.stu1+" is student of "+ obj1.school1 + obj1.place1 )
print(obj1.stu2+" is student of "+ obj1.school2 + obj1.place2 )
```

    Manan is student of KVS Delhi
    Naman is student of DPS Noida



```python
## Hierarchical inheritance
## When we derive or inherit more than one child class from one(same) parent class.
## Then this type of inheritance is called hierarchical inheritance.

class A:
    def display(self, output):
        print(output)
        
class B(A):
    def display(self):
        super().display('Hello from B')
        
class C(A):
    def display(self):
        super().display('Hello from C')
        
b = B()
b.display()

c = C()
c.display()
```

    Hello from B
    Hello from C



```python
## 5. Hybrid inheritence
""" Hybrid inheritance in Python is a combination of more than one type of inheritance.
It is not any sequence or pattern of inheriting classes but is used as a naming convention 
where more than one type of inheritance is involved. """


class A:
    def display(self):
        print("Super Parent display method")


""" class B used as intermediate class
to call class A's display method """

class B(A):
    def display(self):
        super().display()

''' child classes '''
class C(B):
    def display(self):
        super().display()
        print("Class C display method")
        
class D(B):
    def display(self):
        super().display()
        print("Class D display method")

c = C()
c.display()

d = D()
d.display()
```

    Super Parent display method
    Class C display method
    Super Parent display method
    Class D display method



```python

```
