## Ans 1
Multiprocessing refers to the ability of a system to support more than one processor at the same time.Applications in a multiprocessing system are broken to smaller routines that run independently. We use multiprocessing because the more tasks you must do at once, the more difficult it gets to keep track of them all, and keeping the timing right becomes more of a challenge.

## Ans 2
-> In Multiprocessing, CPUs are added for increasing computing power. While In Multithreading, many threads are created of a single process for increasing computing power.

-> In Multiprocessing, Many processes are executed simultaneously. While in multithreading, many threads of a process are executed simultaneously.

-> In Multiprocessing, process creation is a time-consuming process. While in Multithreading, process creation is according to economical.

-> In Multiprocessing, every process owned a separate address space. While in Multithreading, a common address space is shared by all the threads.

## Ans 3
	


```python
import multiprocessing
def print_cube(num):
	print("Cube: {}".format(num * num * num))

if __name__ == "__main__":
	p1 = multiprocessing.Process(target=print_cube, args=(100, ))
	
	p1.start()
	
	p1.join()
```

    Cube: 1000000


## Ans4
Multiprocessing pool is used to create number of processes and a number of methods and passes it to the workers. It is used because it is more convenient and we d not have to manage it manually.

## Ans 5
The syntax to create a pool object is multiprocessing.Pool(processes, initializer, initargs, maxtasksperchild, context).


## Ans 6


```python
import multiprocessing
def print_cube(num):
	print("Cube: {}".format(num * num * num))

def print_square(num):
	print("Square: {}".format(num * num))
    
def difference(x,y):
    print("Difference: {}".format(x-y))
    
def add(x,y):
    print("Addition: {}".format(x+y))

if __name__ == "__main__":
    p1 = multiprocessing.Process(target=print_square, args=(9, ))
    p2 = multiprocessing.Process(target=print_cube, args=(11, ))
    p3 = multiprocessing.Process(target=difference, args=(10,9))
    p4 = multiprocessing.Process(target=add, args=(10,9))
    
    p1.start()
    p2.start()
    p3.start()
    p4.start()

    p1.join()
    p2.join()
    p3.join()
    p4.join()
```

    Square: 81
    Cube: 1331
    Difference: 1
    Addition: 19



```python

```
