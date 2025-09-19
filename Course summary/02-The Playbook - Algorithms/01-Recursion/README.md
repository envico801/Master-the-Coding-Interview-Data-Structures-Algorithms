Now that we have our toolkit of data structures, it's time to learn about **Algorithms**.

### What is an Algorithm?

If data structures are the containers for our data, **algorithms are the recipes that tell us what to do with that data.** They are the step-by-step processes we use to manipulate data and solve problems.

You've already been writing simple algorithms. A function that finds "Nemo" in an array is an algorithm. But just like with cooking, there are famous, well-tested recipes (algorithms) that are incredibly efficient for common tasks like sorting and searching. Learning these is crucial for writing scalable code.

---

### Diving into Recursion

We'll start with a powerful *concept* rather than a specific algorithm: **Recursion**.

**What is Recursion?**
In the simplest terms, recursion is when **a function calls itself.**

**Analogy: Russian Nesting Dolls**
Imagine you have a set of Russian nesting dolls and you want to open all of them. Your instructions could be:
1.  Open the doll.
2.  Is there another doll inside?
    *   If yes, repeat step 1 with the smaller doll.
    *   If no, you are done.

You are applying the *same* instruction ("open the doll") over and over to smaller and smaller versions of the same problem. This is the essence of recursion.

### The Anatomy of a Recursive Function

Every recursive function must have two parts to avoid an infinite loop:

1.  **The Base Case:** This is the **stopping condition**. It's the point at which the function stops calling itself. In our doll analogy, the base case is finding a doll that is empty.
2.  **The Recursive Case:** This is where the function **calls itself**, usually with a slightly modified input that brings it one step closer to the base case (like moving to a smaller doll).

```javascript
let counter = 0;
function inception() {
  // Base Case
  if (counter > 3) {
    return 'done!';
  }
  counter++;
  // Recursive Case
  return inception(); // The function calls itself
}
```

**The Danger: Stack Overflow**
What happens if you forget the base case? The function will call itself forever. Each function call gets added to the **call stack**. Eventually, you'll run out of memory for the call stack, and your program will crash. This is called a **Stack Overflow**.

### Recursion vs. Iteration (Loops)

Anything you can do with recursion, you can also do with a loop (iteration), and vice-versa. So why choose one over the other?

Let's look at the classic **Fibonacci sequence** problem: `0, 1, 1, 2, 3, 5, 8, ...` (each number is the sum of the two preceding ones).

*   **Iterative Solution (O(n)):**
    *   Create an array, start with `[0, 1]`.
    *   Loop `n` times, calculating the next number and pushing it to the array.
    *   **Time:** Fast, O(n). **Space:** O(n) to store the array.

*   **Recursive Solution (O(2^n)):**
    *   `fib(n) = fib(n-1) + fib(n-2)`
    *   **Time:** Horribly slow, **O(2^n) - Exponential Time**. For `fib(7)`, it has to calculate `fib(6)` and `fib(5)`. To calculate `fib(6)`, it has to calculate `fib(5)` and `fib(4)`, and so on. It ends up recalculating the same values many, many times.
    *   **Space:** O(n) because of the call stack depth.

### So, When Should You Use Recursion?

Based on the Fibonacci example, recursion seems terrible! But that's not the whole story.

**Pros of Recursion:**
*   **Readability & Simplicity:** For some problems, a recursive solution is much cleaner and easier to read than a complex iterative one. It can make your code more "DRY" (Don't Repeat Yourself).
*   **Perfect for Trees & Graphs:** When you're dealing with hierarchical data structures like trees, recursion is a natural fit. "Traversing" a tree often means performing the same operation on a node and then recursively performing it on its children. Trying to do this with loops is often a confusing mess.

**Cons of Recursion:**
*   **Large Stack Size:** Can lead to stack overflows if the recursion goes too deep.
*   **Performance:** Can be slower due to the overhead of function calls. A poorly written recursive function (like our Fibonacci example) can be extremely inefficient.

**The Rule of Thumb:**
Use recursion when it simplifies a complex problem, especially with data structures that are naturally recursive (like trees). It's a powerful tool for problems that can be broken down into smaller, self-similar subproblems. This is often called a "divide and conquer" approach.
