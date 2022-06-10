# Breadth-First Search

The main idea around this approach is visiting every node on the same level we are currently on before visiting child nodes. As opposed to Depth-First Search, this algorithm goes broad first (to its neighbors) before going deeper.&#x20;

From the starting node, we enqueue it and place its direct neighbors in the queue. Once all the direct neighbors of the vertex at the front have been visited, we dequeue the vertex at the front and visit all the direct neighbors of the new front vertex. We repeat this until the queue is empty.

![https://www.tutorialspoint.com/data\_structures\_algorithms/images/breadth\_first\_traversal.jpg](<../../.gitbook/assets/image (83).png>)

As in the example given above, BFS algorithm starts at S and enqueues it, the traverses from S to A, from S to B, then from S to C first (respectively enqueueing each and dequeuing S). Thereafter, from A to D (enqueuing D and dequeuing A), from B to E (enqueueing E and dequeuing B), from C to F (enqueueing F and dequeuing C) and lastly, from D to G (enqueueing G and dequeuing D and thereafter, dequeuing E and then F).

**Goal:**

Return the breadth-ward path traversed from the starting vertex to final visited vertex.

**Termination:**

When the queue is empty.

**Steps:**

* Enqueue the first/starting vertex
* Mark it as visited
* Repeat until all the first vertex's adjacent vertices are visited:
  * Visit next adjacent vertex
  * Mark it as visited
  * Enqueue this vertex
* Repeat until queue is empty:
  * Dequeue the vertex at the front of the queue
  * Repeat until all adjacent vertices are visited:
    * Visit next unvisited vertex adjacent to the vertex at the front of the queue
    * Mark it as visited&#x20;
    * Enqueue this vertex

**Time Complexities:**

**Worst & Average Case:**

In a graph (assuming we represent it in an adjacency list), in the worst case this algorithm will visit all the nodes and vertices resulting in a worst and average time complexity of $$Θ=O(|E| + |V|)$$where $$E$$ is the number of edges and $$V$$ is the number of vertices.

**Best Case:**

If an entire tree is traversed with Depth-First Search, it will result in a time complexity of $$Ω(V)$$ where $$V$$ is the number of nodes.

**Implementation:**

```
graph = {
  'A' : ['B','C'],
  'B' : ['D', 'E'],
  'C' : ['F'],
  'D' : [],
  'E' : ['F'],
  'F' : []
}

def bfs(visited, graph, node):
  
  visited = []
  queue = []
  
  visited.append(node)
  queue.append(node)

  while queue:
    current = queue.pop(0) 

    for neighbour in graph[current]:
      if neighbor not in visited:
        visited.append(neighbor)
        queue.append(neighbor)
        
return visited
```

