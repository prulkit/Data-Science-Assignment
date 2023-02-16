## Ans1
Multithreading is defined as the ability of a processor to execute multiple threads concurrently. It is used to improve the performance of a program by using multiple CPUs or CPU cores. Module used to handle threads in python is threading module which includes locking mechanism that allows to synchronize threads.

## Ans 2
Threading module includes locking mechanism that allows to synchronize threads that is why it is used. The use of the following functions are:

• activeCount() - Returns the number of thread objects that are active.

• currentThread() - Returns the number of thread objects in the caller's thread control.

• enumerate() - Returns a list of all thread objects that are currently active.

## Ans 3
• run()  − The run() method is the entry point for a thread.

• start()  − The start() method starts a thread by calling the run method.

• join()  − The join() waits for threads to terminate.

• isAlive()  − The isAlive() method checks whether a thread is still executing.

## Ans 4


```python
import threading
def print_square(num):
	print("Square: {}" .format(num * num ))


def print_cube(num):
	print("Cube: {}" .format(num*num*num))


if __name__ =="__main__":
	t1 = threading.Thread(target=print_square, args=(20,))
	t2 = threading.Thread(target=print_cube, args=(20,))

	
	t1.start()
	t2.start()

	
	t1.join()
	t2.join()
```

    Square: 400
    Cube: 8000


## Ans 5
Advantages of multithreading:
• It enables a program to continue running even if a section is blocked or executing a lengthy process, increasing user responsiveness.

• Thread synchronization functions could be used to improve inter-process communication. 

• The advantages of multithreading in a multiprocessor architecture is every thread could execute in parallel on a distinct processor.

• Multithreading on multiple CPU machines increases parallelism.

• Threads have a minimal influence on the system's resources. The overhead of creating, maintaining, and managing threads is lower than a general process.

Disadvantage of multithreading:

• It needs more careful synchronization.

• It can consume a large space of stocks of blocked threads.

• It needs support for thread or process.

• If a parent process has several threads for proper process functioning, the child processes should also be multithreaded because they may be required.

## Ans 6
A race condition occurs when two threads access a shared variable at the same time. The first thread reads the variable, and the second thread reads the same value from the variable. Then the first thread and second thread perform their operations on the value, and they race to see which thread can write the value last to the shared variable. The value of the thread that writes its value last is preserved, because the thread is writing over the value that the previous thread wrote.

Deadlock is a situation where a process or a set of processes is blocked, waiting for some other resource that is held by some other waiting process. It is an undesirable state of the system.The following are the four conditions that must hold simultaneously for a deadlock to occur.

Mutual Exclusion – A resource can be used by only one process at a time. If another process requests for that resource then the requesting process must be delayed until the resource has been released.
Hold and wait – Some processes must be holding some resources in the non-shareable mode and at the same time must be waiting to acquire some more resources, which are currently held by other processes in the non-shareable mode.
No pre-emption – Resources granted to a process can be released back to the system only as a result of voluntary action of that process after the process has completed its task.
Circular wait – Deadlocked processes are involved in a circular chain such that each process holds one or more resources being requested by the next process in the chain.


```python

```
