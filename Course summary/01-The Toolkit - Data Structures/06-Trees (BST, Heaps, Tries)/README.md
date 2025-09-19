### What is a Tree?

Unlike linear data structures like Arrays and Linked Lists, Trees have a **hierarchical structure**.

**Analogy: A Family Tree (or an upside-down tree)**
*   It starts with one ancestor at the top (the **root**).
*   Each person in the tree can have multiple children.
*   Each child has only one parent.
*   The people at the very bottom with no children are called **leaves**.



Trees are everywhere in computer science: the folder structure on your computer, the HTML that makes up a webpage (the DOM), and even the way AI might make decisions in a game of chess.

### A New Big O: O(log n) - Logarithmic Time

This is a big one! Trees introduce us to one of the most efficient time complexities: **O(log n)**.

**What does it mean?** It means that for every doubling of the input size, the number of operations only increases by one. This is incredibly scalable.

**Analogy: Searching a Phone Book**
Imagine you need to find "Smith" in a massive phone book with 1,000 pages. You wouldn't start at page 1 and read every name (that would be O(n)). Instead, you use a **"divide and conquer"** strategy:
1.  Open the book to the middle (page 500). The names there start with "M".
2.  You know "S" comes after "M", so you can completely ignore the first half of the book. You just cut your problem in half!
3.  You jump to the middle of the second half (page 750). The names there start with "R".
4.  You know "S" comes after "R", so you ignore the pages between 500 and 750. You've cut the problem in half again.

With each step, you eliminate half of the remaining data. This is the essence of O(log n). Even if the phone book had a million pages, it would only take you about 20 steps to find any name.

![O(log n) Graph](https://i.imgur.com/8Q2MvV9.png)

### The Main Types of Trees

#### 1. Binary Search Tree (BST)

This is the most common type of tree you'll encounter. It's a special kind of **Binary Tree** (where each node has at most two children) that follows specific rules, making it perfect for O(log n) searching.

**The Rules:**
*   All child nodes to the **left** of a node must have a value that is **less than** the parent node's value.
*   All child nodes to the **right** of a node must have a value that is **greater than** the parent node's value.



This strict ordering is what allows for the "divide and conquer" search. To find the number `6`:
1.  Start at the root (`9`). `6` is less than `9`, so go **left**.
2.  Now at `4`. `6` is greater than `4`, so go **right**.
3.  Found `6`! It only took 2 steps.

**The Catch: Unbalanced Trees**
The O(log n) performance only works if the tree is **balanced**. If you insert numbers in sorted order (1, 2, 3, 4...), the tree will become completely one-sided, effectively turning into a Linked List. In this worst-case scenario, all operations become **O(n)**. To fix this, more advanced trees like **AVL Trees** and **Red-Black Trees** automatically rebalance themselves. You usually don't need to code these in interviews, but you should know they exist to solve the balancing problem.

#### 2. Binary Heaps

Heaps are another type of binary tree, but they have a different rule. They are primarily used for **priority**.

**The Rule:**
*   In a **Max Heap**, every parent node is **greater than** its children. (The largest item is always at the root).
*   In a **Min Heap**, every parent node is **less than** its children. (The smallest item is always at the root).

**Important Note:** Unlike a BST, there is no ordering rule between the left and right children.

**Use Case: Priority Queue**
Heaps are perfect for building **Priority Queues**. Think of an emergency room: patients aren't treated in the order they arrive (FIFO), they're treated based on the severity of their condition (priority). A heap allows you to always access the highest-priority item instantly (O(1)) while keeping insertions and deletions efficient (O(log n)).

#### 3. Tries (Prefix Trees)

Tries are a special kind of tree optimized for searching text, especially for features like **autocomplete**.

**How it works:**
*   Each node represents a character.
*   By following a path from the root, you can spell out a word.
*   If multiple words share a prefix (like "app", "apple", "apply"), they will share the same initial path in the trie.

This structure is extremely fast for checking if a word or prefix exists. The time complexity is **O(L)**, where L is the length of the word you're searching for—it doesn't matter how many words are in your dictionary
