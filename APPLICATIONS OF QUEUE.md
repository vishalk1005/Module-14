# Exp.No:40  
## IMPLEMENTATION OF CIRCULAR QUEUE USING PYTHON

### AIM  
To implement a Circular Queue using Python with operations such as enqueue, dequeue, and display, and to understand the behavior of the circular queue data structure.

### ALGORITHM  

1.Start
2.Define a class queue with:
3.A constructor to initialize queue, front, rear, and limit.
4.isempty() method to check if the queue is empty.
5.enqueue(item) method to insert elements if the queue is not full.
6.dequeue() method to delete elements if the queue is not empty.
7.display() method to show the current elements in the queue.
8.Create a queue object by getting the size from the user.
9.Accept input elements from the user and insert them using enqueue().
10.Call display() to print the current queue.
11.Call dequeue() to remove an element and display the queue.
12.End

### PROGRAM  

```
class queue:
    def __init__(self,limit):
        self.queue=[]
        self.rear=0
        self.front=0
        self.limit=limit
    def isempty(self):
        if len(self.queue)==0:
            return True
        else:
            return False
    def enqueue(self,item):
        if len(self.queue)==self.limit:
            print("Queue is full")
        else:
            self.queue.insert(self.rear,item)
            self.rear+=1
        
        
        
        
    def dequeue(self):
        if self.front==self.rear:
            print("Queue is underflow")
        else:
            self.queue.pop(self.front)
            self.front+=1
            print(self.queue)
        
        
        
    def display(self):
        print(self.queue)
        
a=int(input())
q=queue(a)
q.enqueue(int(input()))
q.enqueue(int(input()))
q.enqueue(int(input()))
q.display()
q.dequeue()
```

### OUTPUT
![Screenshot (262)](https://github.com/user-attachments/assets/601d35ad-edba-4202-bcb5-9341743721a4)

### RESULT
Thus the python program is initialised and executed successfully.
