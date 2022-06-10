# Graph Representation

![Both code blocks below are representations of this graph.](<../../.gitbook/assets/image (81).png>)

Graphs can be functionally the same but built in a bunch of different ways, namely:

* **Adjacency List:**

The main purpose of the adjacency list data structure is to display a list of the neighbors of a given vertex. Within this 2-Dimensional array, each node ID will correspond with an index in the list. At each index will be an array which will store the node IDs of the nodes which each respective node is connected to. This would be the fastest way to determine node degree.&#x20;

```
# Indices are represented on the left (0-6)  
  [
0   [1,2],
1   [0,2,3],
2   [0,1,4],
3   [1,4],
4   [2,3,5],
5   [4,6],
6   [5]
  ]
```

**Add Vertex:**

Adding a vertex would mean that all we have to do is append the new node to the list resulting in a time complexity of $$O(1)$$.

**Add Edge:**

To add an edge, we would add the corresponding node IDs in two different sub arrays resulting in a time complexity of$$O(1)$$.

**Remove Vertex:**

To remove a vertex, we must also remove all the edges to it stored in the other sub arrays resulting in a time complexity of $$O(|V| + |E|)$$.

**Remove Edge:**

To remove an edge, we must search through every sub array and find the two nodes it connects and remove the edge from the respective vertices resulting in a time complexity of $$O(|E|)$$.

* **Adjacency Matrix:**

A matrix is a 2-Dimensional array but arrays within it are all the same length (AKA rectangular array) whose rows and columns are indexed by vertices.

Indices in the outer array represent nodes with those respective IDs (just like in an adjacency list). The arrays inside represent cells which contain a Boolean value that indicates whether an edge is present between the vertices corresponding to the row and column of the cell. If an edge exists, a 1 is placed at the intersection or else we place a 0 (zero) to represent no edge.&#x20;

```
      0 1 2 3 4 5 6   # Respective indices represented on the left and top
  [   
0    [0,1,1,0,0,0,0],
1    [1,0,1,1,0,0,0],
2    [1,1,0,0,1,0,0],
3    [0,1,0,0,1,0,0],
4    [0,0,1,1,0,1,0],
5    [0,0,0,0,1,0,1],
6    [0,0,0,0,0,1,0]
  ]
```

**Add Vertex:**

To be able to successfully add a vertex, we must add a corresponding column in each sub array and new array in the outer array resulting in a time complexity of$$O(|V^2|)$$.

**Add Edge:**

To add an edge, we update the intersections between to two nodes involved resulting in a time complexity of $$O(1)$$.

**Remove Vertex:**

Removing a vertex means that we must not only remove vertex's row but also update every other sub array by removing the corresponding column $$O(|V^2|)$$.

**Remove Edge:**

To remove an edge, we update the intersections between the two respective nodes, resulting in a time complexity of $$O(1)$$.

**Note:**

$$|V| =$$ magnitude of the set of vertices

$$|E| =$$magnitude of the set of edges



