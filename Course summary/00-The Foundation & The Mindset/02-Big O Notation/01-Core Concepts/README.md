### What is "Good Code"?

When programmers talk about "good code," they usually mean two things:

1.  **Readable:** Is the code clean and easy for other humans to understand?
2.  **Scalable:** How well does the code perform when the amount of data it has to work with gets really, really big?

**Big O notation is the language we use to talk about scalability.**

### Why Do We Need Big O?

Imagine you and a friend write two different programs to find the name "Nemo" in a list of fish. You run your code on your super-fast gaming computer, and it takes 2 seconds. Your friend runs their code on an old laptop, and it takes 5 seconds.

Does that mean your code is better? Not necessarily! Your computer might just be faster.

We need a way to measure the *efficiency of the code itself*, not the computer it's running on. Instead of measuring time in seconds, **Big O measures the number of steps an algorithm has to take relative to the size of its input.**

This helps us answer the question: "If our list of fish grows from 100 to 1,000,000, how much slower will our program get?"

---

Let's look at the two most common types of Big O.

### 1. O(n) — Linear Time

**Analogy: Looking for a friend in a line of people.**

Imagine you have a function whose job is to find "Nemo" in an array of fish names.

```javascript
const fish = ['dory', 'bruce', 'marlin', 'nemo', 'gill'];

function findNemo(array) {
  for (let i = 0; i < array.length; i++) {
    if (array[i] === 'nemo') {
      console.log('Found NEMO!');
    }
  }
}
```

This code goes through the list one by one.
*   If the list has **10** items, it performs about **10** checks.
*   If the list has **1,000,000** items, it performs about **1,000,000** checks.

The number of operations grows in a straight, direct line with the size of the input. We call this **Linear Time**, or **O(n)**. The "n" simply represents the number of items in the input.

On a performance graph, O(n) is a straight diagonal line. As the number of items (input) increases, the time it takes (operations) increases at the same rate.

![O(n) Graph](https://lukasmestan.com/assets/images/o-n.png)

### 2. O(1) — Constant Time

**Analogy: Grabbing the first person in a line.**

Now, what if our function only ever looks at the *first* fish in the array?

```javascript
function grabFirstFish(array) {
  console.log(array[0]);
}
```

*   If the list has **10** items, it performs **1** operation.
*   If the list has **1,000,000** items, it still only performs **1** operation.

The size of the input doesn't matter. The function always takes the same amount of time to run. We call this **Constant Time**, or **O(1)**.

Even if the function grabbed the first *three* fish (O(3)), we still simplify it to O(1). The key idea is that the number of operations stays constant and doesn't grow with the input.

On a performance graph, O(1) is a flat horizontal line. No matter how much the input grows, the time it takes is always the same. This is extremely efficient and considered the gold standard for scalability.

![O(1) Graph](https://lukasmestan.com/assets/images/o-1.png)

### Summary

| Big O      | Name          | What it means                                                | Analogy                             |
| :--------- | :------------ | :----------------------------------------------------------- | :---------------------------------- |
| **O(n)**   | Linear Time   | As the input grows, the number of operations grows with it.  | Searching for a name in a phonebook page by page. |
| **O(1)**   | Constant Time | The input size doesn't matter; it always takes the same time. | Opening a phonebook to the first page. |
