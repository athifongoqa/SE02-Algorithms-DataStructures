---
description: First In, First Out. Last In, Last Out.
---

# Queues

A queue is a data structure which, unlike s stack, is open at both its ends. One end is used to exclusively insert the newest items of data (**AKA enqueue**) and the other is used to exclusively remove the oldest items of data (**AKA dequeue**). It works on the basis of a FIFO (First In, First Out) structure. Basically a queue is a line up - just like how a line up of people at the bank is a queue.&#x20;

![https://www.tutorialspoint.com/data\_structures\_algorithms/images/queue\_diagram.jpg](<../../.gitbook/assets/image (24).png>)

**Accessing & Searching:**

Just like in a stack, peeking allows us to access the first element in the queue in a time complexity of $$O(1)$$ without removing it. To access an item in the queue (other than the front item) we must dequeue every item that comes before it until we reach the desired item. This operation results in a time complexity of $$O(n)$$.

**Insertion & Removal:**

To insert an item at the rear of the queue, we call this an Enqueue operation. We can only ever enqueue a new item to the rear so this operation will run in a time complexity of $$O(1)$$. To remove an item from the front, we call this a Dequeue operation. Just like the Enqueue operation, the time complexity of this operation will also be $$O(1)$$.

**Applications:**

Queues are a useful representation of problems for different applications. For example, jobs to a network printer are enqueued so that the earlier a job is submitted the earlier it will be printed. Call Center phone systems use queues to hold people calling them in an order, until a service representative is free. We will also see this data structure in action later when we implement a Breadth First Search.
