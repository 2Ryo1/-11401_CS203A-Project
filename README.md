# 11401_CS203A-Project
## Reason for Choosing This Topic
When I first learned about Linked Lists, I found them more difficult to understand compared to Arrays because of their different structure. It took me extra time to grasp the concept. Therefore, I decided to use the circuit design skills I practiced this semester in Digital System Design with Tinkercad to simulate the basic operations of a Linked List from another perspective. By visualizing the insertion and deletion processes with Arduino and LEDs, I aimed to re‑recognize and deepen my understanding of how Linked Lists work.
## What is a Linked List? 
A Linked List is a fundamental data structure used to store a sequence of elements. Unlike arrays, which keep elements in contiguous memory locations, a Linked List organizes data into separate nodes.
### Node Structure
- Each node contains two parts:
- **1.Data**  the actual value stored in the node.
- **2.Pointer (Next)**  a reference to the next node in the sequence.
### Head and Tail
- The head is the first node in the list.
- The tail is the last node, which points to NULL (indicating the end of the list).
### Key Characteristics
- **Dynamic size**: The list can grow or shrink easily without reallocating memory.
- **Efficient insertions/deletions at the head**: Adding or removing the first node only requires updating pointers.
- **Sequential access**: To reach a specific element, the list must be traversed node by node.
