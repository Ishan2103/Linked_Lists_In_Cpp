# Singly Linked Lists in C++

## Aim
To study and implement **singly linked lists** in C++ and understand node creation, insertion, traversal, and basic operations.

## Software Required
- Visual Studio Code  
- Windows / Linux

---

## Theory

A **linked list** is a **linear data structure** where elements (nodes) are connected via **pointers**. Unlike arrays, elements are **not stored contiguously** in memory.

### Node Structure
Each node contains:
1. **Data** – stores the value of the node.
2. **Next pointer** – points to the next node in the list (or `NULL` if it’s the last node).

### Key Features
- Dynamic size: Nodes can be added or removed at runtime.
- Efficient insertion/deletion: No shifting of elements as in arrays.
- Traversal starts from the **head** node and continues till `NULL`.

### Types of Singly Linked Lists
1. **Single Node List** – simplest linked list with one node.
2. **Multiple Nodes (Manual Linking)** – nodes connected manually using `next`.
3. **Insertion at Head** – new nodes are added at the beginning.

---

## Algorithm

### Program 1: Insert at Head

**Objective:** Add nodes at the beginning of the list.

**Steps:**
1. Start
2. Define class `Link` with:
   - Data: `data`
   - Pointer: `next`
3. Constructor initializes `data` and sets `next = NULL`
4. Create function `insert_head(head, data)`:
   - Create new node
   - Point new node's `next` to current `head`
   - Update `head` to new node
5. Create function `disp(head)` to traverse and display the list
6. In `main()`:
   - Initialize `head = NULL`
   - Insert multiple nodes using `insert_head()`
   - Display list after each insertion
7. End

---

### Program 2: Manual Node Linking

**Objective:** Create a linked list by connecting nodes manually.

**Steps:**
1. Start
2. Define class `Node` with `val` and `next`
3. Constructor initializes `val` and sets `next = NULL`
4. In `main()`:
   - Dynamically create nodes (`n1`, `n2`, `n3`)
   - Connect nodes manually (`n1->next = n2`, etc.)
   - Use temporary pointer `temp` to traverse and display
5. End

---

### Program 3: Single Node Linked List

**Objective:** Create and traverse a linked list with only one node.

**Steps:**
1. Start
2. Define class `Node` with `val` and `next`
3. Constructor initializes `val` and sets `next = NULL`
4. In `main()`:
   - Create a single node dynamically
   - Traverse using `temp` pointer and print value
5. End

---

## Benefits of Linked Lists
- **Dynamic Memory Allocation:** Memory is used efficiently; nodes can be created and deleted at runtime.
- **Efficient Insert/Delete:** Unlike arrays, no shifting of elements is required.
- **Flexible Size:** The size of the linked list can grow or shrink dynamically.
- **Better than Arrays** for frequent insertions and deletions.

---

## Comparison: Linked List vs Array

| Feature               | Array                     | Linked List                   |
|-----------------------|--------------------------|-------------------------------|
| Memory Allocation     | Static                   | Dynamic                       |
| Size                  | Fixed                    | Flexible                      |
| Insertion/Deletion    | Costly (shifting required)| Efficient (pointer adjustment)|
| Access Time           | O(1) (random access)     | O(n) (sequential access)      |
| Memory Usage          | Contiguous memory        | Extra memory for `next` ptr   |

---

## Conclusion

Singly linked lists are a **fundamental data structure** in C++ that allow dynamic memory management and efficient insertion and deletion of elements. They are ideal when the size of the dataset is not known in advance and frequent insertions/deletions are required. Understanding linked lists is essential for mastering more complex data structures like **stacks, queues, and graphs**.
