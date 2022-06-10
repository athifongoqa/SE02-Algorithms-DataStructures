# Binary Trees

A binary tree is a tree data structure with a special condition being that each node can have a maximum of two children (they can have 0, 1 or 2 children).

![](<../../../.gitbook/assets/image (33).png>)

**Accessing & Searching:**

Because there is no particular order to the elements in this structure, we may need to go through every single element in the tree if the value we are looking for does not exist, resulting in a time complexity of $$O(n)$$.

**Insertion:**

For us to insert a node into a Tree, we may have to change the positions of all the other nodes around the desired position and this will result in a time complexity of $$O(n)$$.

**Removal:**

This operation starts out as a search because we need to find the node we want to delete resulting in a time complexity of $$O(n)$$ . There are scenarios to keep in mind when removing nodes:

* If we are deleting a leaf, simply delete it and move on.
* If we are deleting an internal node:
  * with one child: take the internal node out, move the child up and attach it to the old node's parent.
  * with two/more children: promote a child up like before. If the child has children, we keep traversing down until we hit a leaf.

****

