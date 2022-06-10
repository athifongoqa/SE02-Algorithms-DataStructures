# Graphs

A graph is a data structure designed to show relationships between objects. It is made up of a set of vertices and edges that form connections between vertices. It is worth pointing out that the Tree structure we covered earlier is actually a specific type of Graph.&#x20;

![](<../../.gitbook/assets/image (81).png>)

### Definitions <a href="#definitions" id="definitions"></a>

* **Adjacency** - Two nodes connected together by an edge.&#x20;
* **Edge** - A connection between two nodes. Edges can contain data too, often this data will be the strength of a connection. Edges can also have direction, which can mean that the relationship between two nodes only applies one way and not the other.
* **Path** - An ordered sequence of vertices where a connection must exist between consecutive pairs in the sequence.
* **Path length** - Number of edges in a path.
* **Cycle** - A path where the starting and ending node is the same. Cycles can cause infinite loops so one should always make sure that graphs used in production are acyclic.
* **Directed graph** - A term for a graph where edges have a 'sense' of direction.&#x20;
* **Undirected graph** - A term for a graph where edges have no 'sense' of direction.&#x20;
* **Connectivity:** An important metric used to measure the amount of elements that need to be removed for a graph to become disconnected. Specific types of connectivity are:
  * **Disconnected** - If there is some vertex or group of vertices can not be reached by another vertex or group of vertices present.&#x20;
  * **Strongly connected** - If there exists some path from every vertex to every other vertex, the graph is strongly connected.
  * **Weakly connected** - If by removing a specific edge from one vertex to another, we could potentially caused disconnected vertices or groups or vertices.&#x20;
* **Node degree** - The number of edges connected to a node.
* **Eulerian Path** - A path that travels through every edge once.
* **Eulerian Cycle** - All vertices have an even node degree.
* **Hamiltonian Path** - A path which goes through every vertex once.&#x20;
* **Hamiltonian Cycle** - A path that visits every vertex only once and ends up at the starting vertex.

**Applications:**

Graphs can be used to model data where we are interested in connections and relationships between data, such as your network of friends on Facebook.
