# 11401_CS203A-Project
## Reason for Choosing This Topic
When I first learned about Linked Lists, I found them more difficult to understand compared to Arrays because of their different structure. It took me extra time to grasp the concept. Therefore, I decided to use the circuit design skills I practiced this semester in Digital System Design with Tinkercad to simulate the basic operations of a Linked List from another perspective. By visualizing the insertion and deletion processes with Arduino and LEDs, I aimed to re‑recognize and deepen my understanding of how Linked Lists work.
## What is a Linked List? 
A Linked List is a fundamental data structure used to store a sequence of elements. Unlike arrays, which keep elements in contiguous memory locations, a Linked List organizes data into separate nodes.
### Node Structure
Each node contains two parts:
- **Data**  The actual value stored in the node.
- **Pointer (Next)**  A reference to the next node in the sequence.
### Head and Tail
- The head is the first node in the list.
- The tail is the last node, which points to NULL (indicating the end of the list).
### Key Characteristics
- **Dynamic size**: The list can grow or shrink easily without reallocating memory.
- **Efficient insertions/deletions at the head**: Adding or removing the first node only requires updating pointers.
- **Sequential access**: To reach a specific element, the list must be traversed node by node.
## Linked List vs Array
Arrays and Linked Lists are both fundamental data structures, but they differ significantly in how they store and manage data.
### Memory Structure
- Array: Stores elements in a contiguous block of memory. Each element can be accessed directly by its index.
- Linked List: Stores elements (nodes) separately, each containing data and a pointer to the next node. Memory does not need to be contiguous.
### Insertion and Deletion
- **Array**: Inserting or deleting an element often requires shifting other elements, which takes **O(n)** time.
- **Linked List**: Insertion or deletion at the head is **O(1)**, since only pointers need to be updated.Deletion or insertion at arbitrary positions requires traversal, which is **O(n)**.
### Access/Search
- **Array**: Direct access by index in **O(1)**.
- **Linked List**: Must traverse nodes sequentially, so searching or accessing the i-th element takes **O(n)**.
### Flexibility
- **Array**: Fixed size once declared (unless using dynamic arrays).
- **Linked List**: Dynamic size, can grow or shrink easily without reallocating memory.
## Summary
Arrays are efficient for random access but costly for insertions and deletions. Linked Lists are efficient for dynamic insertions and deletions but slower for random access. This project demonstrates these differences by simulating Linked List operations with Arduino and LEDs, making the abstract behavior visible and easier to understand.

