# Stack vs Queue 

## what is stack ?
 is a linear data structure that follows the specific order to perform the operations.It follows Last In First Out (LIFO) principle.

 Stack supports two basic operations which are:

push — inserts into the stack.
pop — deletes from the stack.

## What is Queue?
The queue is a linear data structure in which we can insert the element from one side of the list and delete the element from the other side of the list.It follows First In First Out (FIFO) principle.

Basic operations
There are two basic operations used by Queues:
Enqueue — adds an item to the queue.
Dequeue — removes an item from the queue.



## What's the difference between Stack and Queue?
| Stack   |   Queue    | 
|----------|:-------------:|
| The stack is based on LIFO(Last In First Out) principle |  principle	The queue is based on FIFO(First In First Out) principle |
| Insertion Operation is called Push Operation	|  Insertion Operation is called Enqueue Operation |  
| Deletion Operation is called Pop Operation | Deletion Operation is called Dequeue Operation |  
|Push and Pop Operation takes place from one end of the stack    | Enqueue and Dequeue Operation takes place from a different end of the queue |
|The most accessible element is called Top and the least accessible is called the Bottom of the stack	|The insertion end is called Rear End and the deletion end is called the Front End. |
|Simple Implementation 	|Complex implementation in comparison to stack |
|Only one pointer is used for performing operations 	|Two pointers are used to perform operations |
|Empty condition is checked using Top==-1	|Empty condition is checked using Front==-1||Front==Rear+1 |
|Full condition is checked using Top==Max-1|Full condition is checked using Rear==Max-1 |
|There are no variants available for stack	|There are three types of variants i.e circular queue, double-ended queue and priority queue |
|Can be considered as a vertical collection visual	|Can be considered as a horizontal collection  visual |
|Used to solve the recursive type problems	|Used to solve the problem having sequential processing |


