Q1, Create a vehicle class with an init method having instance variables as name_of_vehicle, max_speed
and average_of_vehicle.
Q2. Create a child class car from the vehicle class created in Que 1, which will inherit the vehicle class.
Create a method named seating_capacity which takes capacity as an argument and returns the name of
the vehicle and its seating capacity.
Q3. What is multiple inheritance? Write a python code to demonstrate multiple inheritance.
Q4. What are getter and setter in python? Create a class and create a getter and a setter method in this
class.
Q5.What is method overriding in python? Write a python code to demonstrate method overriding.

## Answer 1


```python
class vehicle:
    def __init__(self, name_of_vehicle, max_speed, average_of_vehicle ) :
        self.name_of_vehicle = name_of_vehicle
        self.max_speed = max_speed
        self.average_of_vehicle = average_of_vehicle
        
        def return_vehicle_detials(self):
            return self. name_of_vehicle,self.max_speed , self.average_of_vehicle
```


```python
 vehicle1 = vehicle("Sedan", 180,20)
```


```python
vehicle1.average_of_vehicle
```




    20



## Answer 2


```python
class car(vehicle):
    def __init__(self, seating_capacity) :
        self.seating_capacity = seating_capacity  
        print(self.seating_capacity, vehicle1.name_of_vehicle)

```


```python
car1 =car (4)
```

    4 Sedan


## Answer 3
When child class is derived or inherited from more than one parent class. This is called multiple inheritance.
In multiple inheritance, we have two parent classes/base classes and one child class that inherits both parent classes properties.


```python
## Example

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

## Answe 4
In Python, getters and setters are not the same as those in other object-oriented programming languages. Basically, the main purpose of using getters and setters in object-oriented programs is to ensure data encapsulation. Private variables in python are not actually hidden fields like in other object oriented languages. Getters and Setters in python are often used when:

We use getters & setters to add validation logic around getting and setting a value.

To avoid direct access of a class field i.e. private variables cannot be accessed directly or modified by external user.


```python
class vehicle:
    def __init__(self, name, max_speed, average_of_vehicle ) :
        self.__name = name
        self.__max_speed = max_speed
        self.__average_of_vehicle = average_of_vehicle
        self.__speed = 0 
        
    def set_speed(self , speed) : 
        self.__speed = 0 if speed < 0 else speed 
        
    def get_name(self):
        return self.__name
```


```python
 obj = vehicle("Sedan", 180,20)
```


```python
obj.get_name ()
```




    'Sedan'




```python
obj.set_speed(1234)
```


```python

```

## Answer 5
Method overriding is an ability of any object-oriented programming language that allows a subclass or child class to provide a specific implementation of a method that is already provided by one of its super-classes or parent classes. When a method in a subclass has the same name, same parameters or signature and same return type(or sub-type) as a method in its super-class, then the method in the subclass is said to override the method in the super-class.


```python
class Parent():
	
	def __init__(self):
		self.value = "Inside Parent"
		
	def show(self):
		print(self.value)
		
class Child(Parent):
	
	def __init__(self):
		self.value = "Inside Child"
		
	def show(self):
		print(self.value)
```


```python
obj1 = Parent()
obj2 = Child()

obj1.show()
obj2.show()
```

    Inside Parent
    Inside Child



```python

```
