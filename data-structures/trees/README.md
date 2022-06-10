# Trees

A Tree can conceptually be thought of as an extension of a linked list. A Tree represents the nodes connected by edges, much like how a linked list represents the nodes connected by pointers. The tree starts from a place called the root and the nodes stemming from it are referred to as its descendant nodes. Nodes in a tree are described as having parent-child and/or sibling relationships in relation to one another as indicated in the diagram below.&#x20;

![https://www.tutorialspoint.com/data\_structures\_algorithms/tree\_data\_structure.htm](<../../.gitbook/assets/image (35).png>)

### Important Terms:

* **Nodes** - The building blocks of the Tree, they contains data and pointers to children nodes
* **Edge** - Connection between nodes.&#x20;
* **Path** - Path refers to the sequence of nodes along the edges of a tree.
* **Root** - The node at the top of the tree is called root. There is only one root per tree and one path from the root node to any node.
* **Parent** - Any node except the root node has one edge upward to a node called parent. It is also referred to as an Internal Node.&#x20;
* **Child** - The node below a given node connected by its edge downward is called its child node.
* **Leaf** - The child node which does not have any descendant node is called the leaf node.
* **Subtree** - Subtree represents the descendants of a node.
* **Degree** - the number of children that a node has.&#x20;
* **Levels** - You can describe a tree in terms of levels. The level of a node represents the generation of a node. If the root node is at level 0, then its next child node is at level 1, its grandchild is at level 2, and so on.  The levels indicate how many connections it takes to reach the root from a specific node, plus one.&#x20;
* **Height** - The height of a node is the number of edges between it and the furthest leaf on a tree. A leaf has a height of 0 (zero). The height of a tree is just the height of a root node.&#x20;
* **Depth** - The depth of a node is the number of edges to the root. **Notice how height and depth move inversely.**&#x20;

**Accessing & Searching:**

When accessing or searching (by way of Breadth-First or Depth-First search) for an element in a Tree, we have no direct access to it in the form of an index so having to look through all the elements until we find the desired value will result in a time complexity of $$O(n)$$.

**Insertion:**

For us to insert a node into a Tree, we may have to change the positions of all the other nodes around the desired position and this will result in a time complexity of $$O(n)$$.&#x20;

**Removal:**

This operation starts out as a search because we need to find the node we want to delete resulting in a time complexity of $$O(n)$$ . There are scenarios to keep in mind when removing nodes:

* If we are deleting a leaf, simply delete it and move on.
* If we are deleting an internal node:
  * with one child: take the internal node out, move the child up and attach it to the old node's parent.
  * with two/more children: promote a child up like before. If the child has children, we keep traversing down until we hit a leaf.

**Applications:**

One reason to use trees might be because we want to store information that forms a hierarchy. For example, the Document Object Model used in web development.

