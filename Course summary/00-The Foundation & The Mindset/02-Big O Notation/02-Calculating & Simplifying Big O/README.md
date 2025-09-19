### O(n²) — Quadratic Time

**Analogy: The Handshake Problem.**

Imagine you're at a party. You want to make sure everyone shakes hands with everyone else.

*   If there are **3** people (A, B, C), you need 3 handshakes (A-B, A-C, B-C). Okay, a bit more complex... Let's use a simpler analogy.
*   Let's say you have a list of people and you need to create a gift tag from every person to every *other* person, including themselves.
    *   If you have **3** people `[A, B, C]`, you'll make `3 x 3 = 9` tags: (A to A, A to B, A to C), (B to A, B to B, B to C), etc.
    *   If you have **10** people, you'll make `10 x 10 = 100` tags.

This is what happens when you put a loop **inside another loop**.

```javascript
function logAllPairs(array) {
  for (let i = 0; i < array.length; i++) {       // This loop runs n times
    for (let j = 0; j < array.length; j++) {   // This loop ALSO runs n times
      console.log(array[i], array[j]);         // This line runs n * n times
    }
  }
}
```

The number of operations doesn't just grow—it explodes. This is called **Quadratic Time**, or **O(n²)**. It's represented by a steep, curving line on the performance graph and is generally something to avoid if you can, as it gets very slow, very quickly.

![O(n^2) Graph](https://lukasmestan.com/assets/images/o-n2.png)

---

### The 4 Rules for Simplifying Big O

You'll almost never write down `O(2n + 100)` in an interview. We use these four rules to clean it up.

#### Rule 1: Always Assume the Worst Case

Let's go back to our "Finding Nemo" function. What if Nemo is the very first fish in the list? The function finds him on the first try and stops. That's the best case!

But what if Nemo is the very *last* fish? The function has to check every single fish to find him. This is the **worst case**.

**Big O is all about planning for the worst.** We always measure the worst-case scenario because it's the only way to guarantee performance. Even if the code *could* be fast, we calculate its Big O based on the maximum number of steps it might ever have to take.

*   `findNemo` is **O(n)**, even if Nemo is the first fish.

#### Rule 2: Remove Constants

A computer is incredibly fast. If a function runs 100 steps or 105 steps, the difference is meaningless. The same goes for `n` steps versus `2n` steps.

If you have a function that loops through a list once (`n` operations) and then loops through it *again* separately (`n` operations), the total is `2n`.

```javascript
// O(n + n) which is O(2n)
function twoLoops(array) {
  // First loop
  for (let i = 0; i < array.length; i++) { /* ... */ }

  // Second loop
  for (let i = 0; i < array.length; i++) { /* ... */ }
}
```

**Rule:** We drop the constants. We don't care if it's `O(2n)` or `O(n/2)` or `O(n + 1000)`. We simplify it all down to **O(n)**. The important part is that the trend is **linear**, not how steep the line is.

#### Rule 3: Use Different Variables for Different Inputs

What if a function takes in two separate lists?

```javascript
function processTwoLists(listA, listB) {
  // First loop depends on the size of listA
  for (let i = 0; i < listA.length; i++) { /* ... */ }

  // Second loop depends on the size of listB
  for (let i = 0; i < listB.length; i++) { /* ... */ }
}
```

We can't say this is `O(n)` because `listA` could have 1 item and `listB` could have 1,000,000 items. Their sizes are independent.

**Rule:** Use a different variable for each input. The Big O for this function is **O(a + b)**. If the loops were nested, it would be **O(a * b)**.

#### Rule 4: Drop Non-Dominant Terms

This is the most important rule. Imagine you have a function with a Big O of `O(n + n²)`.

*   When `n` is 10, this is `10 + 100 = 110`. The `n²` part (100) is already much bigger.
*   When `n` is 1,000, this is `1,000 + 1,000,000 = 1,001,000`. The `n` part (1,000) is now completely insignificant.

**Rule:** You only keep the most "powerful" or "dominant" term. The term that grows the fastest is the only one that matters at scale.

*   `O(n + n²)` simplifies to **O(n²)**.
*   `O(1 + n/2 + 100)` simplifies to **O(n)**.
*   `O(a*b + a)` simplifies to **O(a*b)**.

### Summary

| Rule                    | Example                          | Simplified To | Analogy                                                  |
| :---------------------- | :------------------------------- | :------------ | :------------------------------------------------------- |
| **1. Worst Case**       | Finding Nemo at the start vs. end| `O(n)`        | Plan for the longest possible line at the grocery store.   |
| **2. Remove Constants** | `O(2n)` or `O(n + 500)`          | `O(n)`        | An extra grain of sand doesn't matter on a huge beach.     |
| **3. Different Inputs** | `O(listA.length + listB.length)` | `O(a + b)`    | Counting items in two different people's shopping carts. |
| **4. Drop Non-Dominants**| `O(n² + n)`                      | `O(n²)`       | The roar of a jet engine (`n²`) drowns out a whisper (`n`). |
