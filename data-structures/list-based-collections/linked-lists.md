# Linked Lists

The linked list data structure can be visualized as a chain of multiple nodes, where every node points to the next node. Each node has two sections within it: a data section which contains the element we want to store and a pointer section which points to the location of another node.

Each node in the linked list has to have a pointer to another node in the list. To reach a specific node, we follow the chain of pointers from one to another until we reach the node we are looking for.&#x20;

Below is an example of a linked list along with its data and pointer sections:

![https://www.tutorialspoint.com/data\_structures\_algorithms/linked\_list\_algorithms.htm](<../../.gitbook/assets/image (15).png>)

The previous linked list has forward links only. This means that at any point, we can easily find out what the next node is but there is no way of easily finding out what the previous node is. To find the the previous node, we would have to make a note of the current node (current\_node); start at the beginning again; and search for a node where the pointer has the same data as current\_node.

A **Doubly Linked List** is a variation of Linked List in which navigation is possible in both ways, either forward and backward and just as easily as in the **Singly Linked List shown above**.

![https://www.tutorialspoint.com/data\_structures\_algorithms/doubly\_linked\_list\_algorithm.htm](<../../.gitbook/assets/image (16).png>)

**Accessing & Searching:**

There is no way to directly access a node in a singly (or doubly) linked list because the positions of nodes are not identified by indexes like in the case of elements in an array. To find a node with the data (or value) we are looking for, we basically need to start at the head (or last element in a doubly linked list) and follow the pointers until we reach the node with the data we are looking for or run into a NULL value at the end of the chain. The time complexity in this case is $$O(n)$$.

**Insertion & Removal:**

A \[singly or doubly] linked list is easy to grow and shrink. Data is not stored in consecutive memory locations so each piece of data requires us to store an extra pointer. To insert a node, we first create the new node, thereafter we point it to the node we want to follow it and then point our intended previous node to the new node. To remove a node (AKA target\_node), we take the node before it and point it to the same node as target\_node. We then remove the link between target\_node and the node it points to. Both insertion and removal of any node in a list (this is assuming that the position of the insertion or removal is known) are very efficient and each run in a time complexity of $$O(1)$$ .&#x20;

**Caveat:**

In order to implement a list using a singly linked list structure, each value is put into its own node in the data section. Each node in the list is then linked with the next node by storing the address of the next node in the list. The memory usage in this case is at least one extra pointer for each piece of data. However, nodes are created on an as needed basis. There are never any unused nodes. Thus, the amount of memory used to store data in a linked list structure is typically lower than an array, at least whilst the array is not yet full. (Taken from: [CathyAtSeneca](https://cathyatseneca.gitbooks.io/data-structures-and-algorithms/content/lists/array\_implementation.html)) **Overall in theory, you want to use a linked list if you need to insert or delete data at arbitrary locations.**&#x20;
