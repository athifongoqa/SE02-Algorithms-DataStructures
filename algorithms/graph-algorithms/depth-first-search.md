# Depth-First Search

The main idea around this approach is that exploring child nodes is the priority. In a Depth-First Search, we follow a path from a starting vertex until we reach the last vertex on that path. Thereafter, we backtrack until we come across a path to an unvisited vertex and follow it until we reach the last unvisited vertex on that path again and repeat until all vertices are visited. We use a Stack data structure to help us remember to get the next vertex to start a search, when a dead end occurs in any iteration.

![https://www.tutorialspoint.com/data\_structures\_algorithms/images/depth\_first\_traversal.jpg](<../../.gitbook/assets/image (82).png>)

As in the example given above, DFS algorithm traverses from S to A to D to G to E to B first (respectively adding each to the stack as we go), backtracks from B to E (popping B off the stack in the process) because there is no direct path from B to an unvisited vertex, backtracks from E to G (popping E off the stack in the process) for the same reason as before, then goes from G to F (because F is an unvisited vertex) and lastly, from F to C (adding each to the stack respectively) for the same reason as before. Thereafter it notices that there is no direct path from C to an unvisited vertex, it backtracks from C to F to G to D to A to S (respectively popping each one off of the stack as we go until the stack is empty).

**Goal:**

Return the depth-ward path traversed from the starting vertex to final visited vertex.

**Termination:**

When the stack is empty.

**Steps:**&#x20;

* Push the first/starting vertex onto the stack
* Mark this vertex as visited
* Repeat until the stack is empty:
  * Visit the next unvisited vertex adjacent to the one on top of the stack
  * Push this vertex onto the top of the stack
  * Mark this vertex as visited
    * If there isn't an unvisited vertex to visit, pop this vertex off of the stack.

**Time Complexities:**

**Worst & Average Case:**

In a graph (assuming we represent it in an adjacency list), in the worst case this algorithm will visit all the nodes and vertices resulting in a worst and average time complexity of $$Θ=O(|E| + |V|)$$where $$E$$ is the number of edges and $$V$$ is the number of vertices.

**Best Case:**

If an entire tree is traversed with Depth-First Search, it will result in a time complexity of $$Ω(V)$$ where $$V$$ is the number of nodes.&#x20;

**Implementation:**

I chose to implement this algorithm iteratively instead of recursively because I felt that it represented the relationship with the stack in a more intuitive way than the latter.&#x20;

```
graph = {'A': ['B', 'C', 'D'],
         'B': ['A', 'E'],
         'C': ['A', 'D', 'F'],
         'D': ['A', 'C', 'E', 'G'],
         'E': ['B', 'D', 'G'],
         'F': ['C', 'G'],
         'G': ['D', 'E', 'F']}


def dfs(graph, start):
    
    stack = [start]
    path = []

    while stack:
        top = stack.pop()
        if top in path:
            continue
        path.append(top)
        for neighbor in graph[top]:
            stack.append(neighbor)

    return path


print(dfs(graph, 'C'))                    # ['C', 'F', 'G', 'E', 'D', 'A', 'B']
```



