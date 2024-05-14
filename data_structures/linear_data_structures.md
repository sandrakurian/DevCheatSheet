# Linear Data Structures

## Arrays
- **What it is**: Contiguous block of memory storing elements of the same type.
- **Keeps track of**: Size (number of elements), individual elements accessible by index.
- **Pros**:
  - Constant-time access to elements using index.
  - Suitable for random access and fixed-size collections.
- **Cons**:
  - Fixed size (static arrays) or potential resizing overhead (dynamic arrays).
- **Runtime**:
  - Create: O(1) (static), O(n) with resizing (dynamic).
  - Read/Write (Access): O(1) based on index.
  - Insert/Delete: O(n) average case for dynamic arrays (resizing required).

## Linked Lists
- **What it is**: Collection of nodes where each node points to the next node in the sequence.
- **Keeps track of**: Head (first node), Tail (last node), Size.
- **Pros**:
  - Dynamic size, efficient insertion/deletion at any position.
- **Cons**:
  - No random access, traversal required for access.
- **Runtime**:
  - Create: O(1) for empty list.
  - Read: O(n) worst case (traversal from head to required node).
  - Insert/Delete: O(1) for operations at head/tail; O(n) for operations at specific positions.

## Stacks
- **What it is**: Last-In-First-Out (LIFO) collection of elements.
- **Keeps track of**: Top (pointer to the last element).
- **Pros**:
  - Simple and efficient for managing function calls, undo mechanisms, etc.
- **Cons**:
  - Limited access to elements (only top element accessible).
- **Runtime**:
  - Create: O(1) for empty stack.
  - Push/Pop (Insert/Delete): O(1).

## Queues
- **What it is**: First-In-First-Out (FIFO) collection of elements.
- **Keeps track of**: Front (pointer to the first element), Rear (pointer to the last element).
- **Pros**:
  - Useful for modeling scenarios like task scheduling, breadth-first search.
- **Cons**:
  - Access to elements requires dequeueing (no random access).
- **Runtime**:
  - Create: O(1) for empty queue.
  - Enqueue/Dequeue (Insert/Delete): O(1).

## Deques (Double-ended Queues)
- **What it is**: Generalization of queues where elements can be added or removed from both ends.
- **Keeps track of**: Front, Rear, Size.
- **Pros**:
  - Supports efficient insertion/deletion at both ends.
- **Cons**:
  - More complex than stacks or queues.
- **Runtime**:
  - Create: O(1) for empty deque.
  - Insert/Delete at ends: O(1).
