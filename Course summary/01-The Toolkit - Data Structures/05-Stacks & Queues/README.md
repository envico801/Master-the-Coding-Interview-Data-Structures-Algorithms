### The Power of Limits

Stacks and Queues are what we call **linear data structures**. You can think of them as specialized versions of Arrays or Linked Lists, but with one key difference: they are *intentionally limited*.

With an Array, you have a lot of freedom: you can add, remove, and access items from anywhere. Stacks and Queues restrict what you can do. You can generally only interact with the beginning or the end of the list.

Why is this a good thing? Because by limiting the operations, you ensure that the operations you *can* do are extremely fast and efficient. It's like giving someone just a hammer and a nail; they know exactly what to do, and they can do it quickly.

---

### 1. Stacks (LIFO)

A stack follows the **LIFO** principle: **Last-In, First-Out**.

**Analogy: A Stack of Plates**
*   You can only place a new plate on the **top** of the stack.
*   You can only take a plate from the **top** of the stack.
*   The last plate you put on is the first one you take off.

**Common Uses:**
*   **Browser History:** When you click the "back" button, you're "popping" the most recent page off the stack of pages you've visited.
*   **Undo/Redo:** Each action you take is "pushed" onto a stack. Clicking "undo" pops the last action off.
*   **Function Calls:** When a function calls another function, it gets pushed onto the "call stack." This is how your program keeps track of where it is. (If you have too many nested function calls without returning, you get a "stack overflow" error!)

**Key Operations:**
*   `push`: Add an item to the top.
*   `pop`: Remove the top item.
*   `peek`: Look at the top item without removing it.

---

### 2. Queues (FIFO)

A queue follows the **FIFO** principle: **First-In, First-Out**.

**Analogy: A Line at the Grocery Store**
*   New people join at the **end** of the line.
*   The person at the **front** of the line is the next to be served.
*   The first person to get in line is the first person to get out.

**Common Uses:**
*   **Printers:** The first document you send to the printer is the first one to be printed.
*   **Waitlists:** Restaurant waitlists or ticket purchasing systems use queues to serve customers in the order they arrived.
*   **Messaging Systems:** Messages are often processed in the order they were received.

**Key Operations:**
*   `enqueue`: Add an item to the end of the queue.
*   `dequeue`: Remove the item from the front of the queue.
*   `peek`: Look at the item at the front of the queue.

---

### Implementation: Linked Lists vs. Arrays

Stacks and Queues aren't typically built-in data structures; you build them *using* either an Array or a Linked List. The choice matters!

#### For Stacks:

Both Arrays and Linked Lists work great.
*   **Arrays:** `push` and `pop` operations on an array are naturally `O(1)`, which is perfect for a stack. They are simple and often slightly faster due to how memory is organized (cache locality).
*   **Linked Lists:** `prepend` (push) and removing the head (pop) are also `O(1)`. They offer more flexible memory management.

**Verdict:** Both are excellent choices. Arrays are often simpler.

#### For Queues:

Linked Lists are the clear winner.
*   **Linked Lists:** To `enqueue`, you add a node to the tail (`O(1)`). To `dequeue`, you remove the head (`O(1)`). All operations are super efficient.
*   **Arrays:** To `enqueue`, you can `push` to the end (`O(1)`). But to `dequeue`, you have to remove the *first* element. As we know, this is an `O(n)` operation because every other element in the array has to be shifted over. This makes arrays a very poor choice for building an efficient queue.

**Verdict:** Always use a Linked List to build a Queue. This is a classic interview question!

| Data Structure | Best Implementation | Why?                                                                |
| :------------- | :------------------ | :------------------------------------------------------------------ |
| **Stack**      | Array or Linked List | Both provide efficient `O(1)` operations for the ends of the list.    |
| **Queue**      | Linked List         | Arrays are inefficient (`O(n)`) for removing the first element. |
