# Connected Components

Definition: Nodes v and w are connected if there is a path between them.
A connected componente is a maximal set of connected vertices.
Goal: Preprocess graph to answer queries of the from "is v connected to w?" in
constant time.

The relation "is connected to" is an equivalence relation:  
* Reflexive: v is connected to v  
* Symmetric: if v is connected to w, than w is connected to v  
* Transitive: if v is connected to w and w is connected to x, than v is connected to x

Implementation: For each unvisited vertex, run depth-first search to identify all vertices
discovered as part of the same component.