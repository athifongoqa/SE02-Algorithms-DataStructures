# Heaps

A Heap is another specific type of tree with some of its own additional rules. In a Heap, elements are arranged in increasing or decreasing order. Heaps do not need to be binary trees (**but they can be, AKA Binary Heaps**) so parents can have any number of children. The root element is either the maximum or minimum value in the tree. Their respective names are Max Heaps and Min Heaps.

In a Max Heap, a parent must always have a greater value than its child. The root will always end up being the biggest element.

![Max Heap: https://www.tutorialspoint.com/data\_structures\_algorithms/images/max\_heap\_example.jpg](<../../.gitbook/assets/image (58).png>)

In a Min Heap, parents have lower values than their children. The root will always end up being the smallest element.&#x20;

![Min Heap: https://www.tutorialspoint.com/data\_structures\_algorithms/images/min\_heap\_example.jpg](<../../.gitbook/assets/image (59).png>)

**Searching & Accessing:**

Accessing the root node (the maximum value in a Max Heap or the minimum value in a Min Heap) will require us to perform a Peek operation which results in a time complexity of $$O(1)$$.&#x20;

When accessing or searching (by way of DFS or BFS which are explained later) for an element other than the root node in a Heap, we have no direct access to it in the form of an index so having to look through all the elements until we find the desired value which will result in a time complexity of $$O(n)$$.

**Insertion:**

1. Create a new node at the end of the heap, which can be done in $$O(1)$$ (if we use an array to store the Heap).
2. Assign the new value to the node.
3. Compare the value of this child node with its parent.
4. If the value of the parent is less than the child, swap the parent and child.
5. Repeat until the respective Heap property is true all around the structure. (aka **Heapify** operation)

Based these steps, we can confidently infer that the time complexity of insertion will be $$Θ(logn)$$since we traverse the height of the Tree.

**Removal:**

1. In the worst case, we will remove the root node. (aka **Extract** operation)
2. Move the right-most element of the last level to the root.
3. Compare the value of this child node with its parent.
4. If the value of the parent is less than this specific child node, we will swap them.
5. Repeat until the respective Heap property is true all around the structure.

Although we covered removing the root node, these steps apply to removing all internal nodes within the Heap. And just like insertion, based these steps, we can confidently infer that the time complexity of removal will be $$O(logn)$$since we traverse the height of the Tree.

**Caveat:**

Although they are represented as Trees, they are stored as arrays because this saves space. The reason being that we do not require respective pointers for each node.

![https://upload.wikimedia.org/wikipedia/commons/thumb/c/c4/Max-Heap-new.svg/330px-Max-Heap-new.svg.png](<../../.gitbook/assets/image (68).png>)

