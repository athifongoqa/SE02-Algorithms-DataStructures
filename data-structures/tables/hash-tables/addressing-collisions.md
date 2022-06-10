# Addressing Collisions

There are multiple approaches to dealing with collisions. For the time being, I will address:

**Closed Addressing:**

* **Chaining:**

The main idea with this method is that instead of storing key-value pairs directly in the array, we store them in a linked list and from each index in the array, we are going to have a pointer to said linked list. The linked list will contain all the key-value pairs that were assigned to the specific index in the array. The time complexity for inserting a key-value pair will be $$O(1)$$ and searching for a key-value pair will be $$O(1+\lambda)$$.

![https://simpledevcode.files.wordpress.com/2015/05/k7c89.png](<../../../.gitbook/assets/image (64).png>)

**Open Addressing:**

This approach deals with storing elements directly in the same array and not relying on separate data structures.&#x20;

* **Linear Probing:**

The main idea here is that we store key-value pairs directly in the array. If another key-value pair collides with it, we check if the element to the right (our current index plus 1) of the collision is empty. If it is, we place the newer key-value pair there. The time complexity for inserting or removing a key-value pair will be $$O(n)$$ and for searching it will be $$O(n)$$too. This approach can become inefficient due to elements forming clusters.

![https://courses.cs.washington.edu/courses/cse326/00wi/handouts/lecture16/img015.gif](<../../../.gitbook/assets/image (65).png>)

* **Double Hashing:**

Double Hashing mitigates the inefficiencies of elements forming clusters during linear probing and in searching. Double hashing uses the idea of applying a second hash function to key when a collision occurs. **** The value determined by the second hash function will be used to determine how many elements we want to check ahead. The time complexity for searching, inserting and removing will be $$O(n)$$ seeing as we may have to probe all the elements in the array.

![https://courses.cs.washington.edu/courses/cse326/00wi/handouts/lecture16/img025.gif](<../../../.gitbook/assets/image (66).png>)

****

****

