# Non-Linear Data Structures

## Trees
- **What it is**: Hierarchical data structure consisting of nodes (parent-child relationship).
- **Keeps track of**: Root (topmost node), Parent, Children.
- **Pros**:
  - Efficient for hierarchical data representation, searching, and sorting.
- **Cons**:
  - Complex operations like balancing required in some tree types.
- **Runtime**:
  - Create: O(1) for empty tree.
  - Search/Insert/Delete: O(log n) average for balanced trees (e.g., AVL, Red-Black).

## Graphs
- **What it is**: Collection of nodes (vertices) connected by edges.
- **Keeps track of**: Nodes (vertices), Edges (connections between vertices).
- **Pros**:
  - Powerful for modeling relationships between entities.
- **Cons**:
  - Complex algorithms required for traversal and pathfinding.
- **Runtime**:
  - Create: O(1) for empty graph.
  - Traversal/Pathfinding: Depends on the algorithm (e.g., DFS, BFS).

## Hash Tables
- **What it is**: Data structure that implements associative arrays or mappings of keys to values.
- **Keeps track of**: Buckets (storage for key-value pairs), Hash functions.
- **Pros**:
  - Fast lookup, insertion, and deletion (average case).
- **Cons**:
  - Collision resolution strategies impact performance.
- **Runtime**:
  - Create: O(1) for empty hash table.
  - Insert/Search/Delete: O(1) average case, O(n) worst case (with poor hash function).

## Heaps
- **What it is**: Binary tree data structure where each parent node is less than or equal to its child nodes (min-heap) or greater than or equal to its child nodes (max-heap).
- **Keeps track of**: Root, Parent-Child relationships.
- **Pros**:
  - Efficient for maintaining a collection of largest or smallest elements.
- **Cons**:
  - Limited access to elements (only root accessible).
- **Runtime**:
  - Create: O(1) for empty heap.
  - Insert/Delete (Heapify): O(log n).
