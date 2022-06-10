# Tree Traversal

**The traversals explained below are approaches derived from a class of Graph algorithms (Depth-First Search & Breadth-First Search) which I will cover in detail under the Algorithms sub-folder.**&#x20;

Traversal is a process to visit all the nodes of a tree. Trees are not linear so we cannot randomly access a node in a tree. We do, however, have three main approaches by which we can decide between to traverse our way through a given tree:

* In-order Traversal
* Pre-order Traversal
* Post-order Traversal

Generally, we traverse a tree to search or locate a given item or key in the tree.

**In-Order Traversal (left-child and back):**

![https://www.tutorialspoint.com/data\_structures\_algorithms/images/inorder\_traversal.jpg](<../../.gitbook/assets/image (37).png>)

Essentially, in this traversal we are moving through the nodes in the same order. We start at the root (A) but do not check it off. We only check off a node when we've seen its left child and come back to it. So, we instead move onto its left child (B) but also do not mark it off because B has a left child (D). We move onto D and mark it off. We now traverse back to B and mark it off and move onto its right child (E) and mark it off too. We have now successfully traversed through our left subtree. We traverse back up to the root (A) and mark it off too. We repeat the steps taken in the left subtree in the right subtree.&#x20;

The order upon completion should be: D, B, E, A, F, C, G.

**Pre-Order Traversal (mark as we traverse):**

![https://www.tutorialspoint.com/data\_structures\_algorithms/images/preorder\_traversal.jpg](<../../.gitbook/assets/image (36).png>)

The main idea here is to check off a node as we see it before we traverse any further in the tree. We start at the root (A) and mark that we've seen it. Next, we pick one of the children (convention dictates that we pick the left one, so B in this case) and mark it too. We continue traversing down the left-most nodes until we hit a leaf (D), then we mark off the leaf and go back to the parent (B). Now we traverse to the right child (E) and mark it off too. Since we are done with the subtree, we traverse back up to the root (A) and look at its right child (C). We follow the same steps as before until every node has been marked off.&#x20;

The order upon completion should be: A, B, D, E, C, F, G.

**Post-Order Traversal (all descendants first):**

![https://www.tutorialspoint.com/data\_structures\_algorithms/images/preorder\_traversal.jpg](<../../.gitbook/assets/image (38).png>)

Main idea in this approach is that we can only mark off a node when we've visited all of its descendants, or visited both of its children and returned. We start at the root but do not mark it off. We move onto its left child (B) but do not mark it off. We move onto its left child (D) and mark it off then move onto its right child (E) and mark it off. We move back up to the parent (B) and mark it off. We move onto the right subtree and repeat the process. Finally, after marking off all nodes in the right subtree, we mark off the root.&#x20;

The order upon completion should be: D, E, B, F, G, C, A.
