---
description: >-
  Apologies for the quality of diagrams used. I could not find a resource to
  visualize BSTs in good quality.
---

# Binary Search Trees

Trees are inherently disorganized. When we use a tree, we know the overall structure but not where specific elements will be. We can add rules to the ordering of elements in our tree to accomplish certain tasks really fast.&#x20;

Enter Binary Search Trees (BSTs). BSTs are a more specific type of Binary Tree. It has a specific rule for how the values associated with each node are arranged. They consist of nodes with zero to two children each, and a designated root node. BSTs are sorted so that every value on the left of a particular parent node is smaller than it and every value on the right of a particular parent node is larger than it. Because BSTs have this structure, we can do operations like search, insert & delete really quickly.&#x20;

### Assume we have an array that we want to convert into a BST.&#x20;

**The contents of the array are:** \[5, 7, 1, 15, 9, 3, 6]



![First, we insert the first element as the root node.](<../../../.gitbook/assets/image (40).png>)

![To insert 7, we compare it to 5. ](<../../../.gitbook/assets/image (41).png>)

![It is larger so it goes to the right of 5.](<../../../.gitbook/assets/image (42).png>)

![Compare 1 to 5.](<../../../.gitbook/assets/image (43).png>)

![1 < 5, so it goes to the left of 5.](<../../../.gitbook/assets/image (44).png>)

![Compare 15 to 5.](<../../../.gitbook/assets/image (45).png>)

![15 > 5, so we move to the right. Compare 15 to 7.](<../../../.gitbook/assets/image (46).png>)

![15 > 7, so it goes to the right of 7.](<../../../.gitbook/assets/image (47).png>)

![Compare 9 to 5.](<../../../.gitbook/assets/image (48).png>)

![9 > 5, so we move to the right of 5. Compare 9 to 7.](<../../../.gitbook/assets/image (49).png>)

![9 > 7, so we move to the right of 7. Compare 9 to 15.](<../../../.gitbook/assets/image (50).png>)

![9 < 15, so it goes to the left of 15.](<../../../.gitbook/assets/image (51).png>)

![Compare 3 to 5.](<../../../.gitbook/assets/image (52).png>)

![3 < 5, so we go to the left of 5. Compare 3 to 1.](<../../../.gitbook/assets/image (53).png>)

![3 > 1, so we move to the right of 1 and place it there.](<../../../.gitbook/assets/image (54).png>)

![Compare 6 to 5.](<../../../.gitbook/assets/image (55).png>)

![6 > 5, so we move to the right of 5. Compare 6 to 7.](<../../../.gitbook/assets/image (56).png>)

![6 < 7, so we insert 6 to the left of 7.](<../../../.gitbook/assets/image (57).png>)



**Searching, Accessing & Insertion:**

In general, to search for, access or insert an item into a BST, we start at the root node and compare our node value to it and act accordingly (right if larger, left if smaller) and repeat this until we reach our intended destination. Searching/Accessing will result in a time complexity of $$O(h)$$ and insertion will result in an average time complexity of $$Θ(h)$$ (which can also be represented as $$O(logn)$$and $$Θ(logn)$$ respectively) where $$h$$ is the height of the tree.&#x20;

The worse case scenario for insertion would be if we had a Binary Search Tree which is unbalanced (meaning its skews exclusively in one direction), in which case the time complexity of insertion would be $$O(n)$$ because in this case the height $$(h)$$ would be equal to the number of nodes $$(n)$$.

**Removal:**

This operation starts out as a search (just like in BTs) because we need to find the node we want to delete resulting in a time complexity of $$O(n)$$ . There are scenarios to keep in mind when removing nodes:

* If we are deleting a leaf, simply delete it and move on.
* If we are deleting an internal node:
  * with one child: take the internal node out, move the child up and attach it to the old node's parent.
  * with two/more children: promote a child up like before. If the child has children, we keep traversing down until we hit a leaf.

**Applications:**

Used in many search applications where data is constantly entering and leaving, such as the map and set objects in many languages' libraries.
