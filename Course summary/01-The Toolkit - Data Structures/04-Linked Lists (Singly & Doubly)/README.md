### What is a Linked List?

Arrays store data next to each other in memory. Hash tables scatter data all over the place. A linked list is a happy medium: it scatters data but keeps it in order by linking each piece of data to the next.

**Analogy: A Scavenger Hunt**
*   You start at the beginning (the **head**).
*   The first clue (a **node**) tells you its value (e.g., "apples") and gives you a hint pointing to the location of the next clue (the **pointer**).
*   You follow this chain of clues until you reach the last one (the **tail**), which tells you the scavenger hunt is over (it points to **null**).

Each "clue" in this chain is a **node**. A node contains two pieces of information:
1.  **The data** (e.g., the number 10)
2.  **A pointer** to the next node in the sequence.



A key concept here is the **pointer**. It's simply a reference (a memory address) to another object. It's the "link" in the "linked list."

### Why Use a Linked List?

Linked lists shine where arrays struggle.

*   **Fast Insertion and Deletion:** Remember how adding an item to the beginning of an array was slow (O(n)) because we had to shift every other element? With a linked list, it's incredibly fast (O(1)).

    **Analogy:** To add a new person to the front of a conga line, you just have them grab the hands of the first person. No one else has to move. You just update one or two "pointers" (the hand-holding).

*   **Ordered Data:** Unlike hash tables, linked lists maintain a specific order. You can traverse them from start to finish.

However, they have a major downside:

*   **Slow Lookups:** To find the 5th item in a linked list, you *must* start at the head and follow the chain five times. You can't just jump directly to it like you can with an array's index. This makes lookups and searches an **O(n)** operation.

### Singly vs. Doubly Linked Lists

There are two main types of linked lists:

1.  **Singly Linked List:** (The one we've been talking about)
    *   Each node only knows about the **next** node.
    *   It's a one-way street; you can only traverse forward.
    *   **Pros:** Simpler, uses slightly less memory.
    *   **Cons:** You can't go backward. If you're at a certain node, you have no idea what came before it.

2.  **Doubly Linked List:**
    *   Each node has two pointers: one to the **next** node and one to the **previous** node.
    *   It's a two-way street; you can traverse both forwards and backward.
    *   **Pros:** More flexible. You can easily traverse in reverse or delete a node without needing a reference to the node before it.
    *   **Cons:** Uses a little more memory (for the extra pointer) and is slightly more complex to implement.



### The Big O of Linked Lists

Here’s a summary of their performance:

| Operation       | Singly Linked List | Why?                                                                      |
|:----------------|:-------------------|:--------------------------------------------------------------------------|
| **prepend** (add to front) | `O(1)`             | Just change the head pointer. Super fast.                                 |
| **append** (add to end)  | `O(1)`             | Just change the tail pointer. Super fast.                                 |
| **lookup/search**  | `O(n)`             | You have to start at the head and traverse the list one by one.           |
| **insert** (in middle) | `O(n)`             | You first have to traverse to the right spot (`O(n)`), then do the quick insertion (`O(1)`). |
| **delete** (in middle) | `O(n)`             | Same as insert: you have to traverse first.                               |

### Interview Tip: Reversing a Linked List

A very common interview question is to reverse a singly linked list. This is a great test of your understanding of pointers. You can't just use a `.reverse()` method; you have to manually go through the list and flip the direction of each pointer one by one. It's tricky but demonstrates a solid grasp of how the data structure works.

**In summary,** linked lists are a foundational data structure, perfect for when you need an ordered list that requires frequent insertions and deletions at the beginning or end.
