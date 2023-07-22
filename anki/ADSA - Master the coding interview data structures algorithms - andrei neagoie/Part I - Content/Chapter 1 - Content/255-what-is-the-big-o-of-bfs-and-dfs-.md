Q: What is the big O of BFS and DFS?  
A: O(n)  
**BFS:**  
Time complexity is `O(|V|)`, where `|V|` is the number of nodes. You need to traverse all nodes.  
Space complexity is `O(|V|)` as well - since at worst case you need to hold all vertices in the queue.  
**DFS:**  
Time complexity is again `O(|V|)`, you need to traverse all nodes.  
Space complexity - depends on the implementation, a recursive implementation can have a `O(h)` space complexity \[worst case\], where `h` is the maximal depth of your tree.  
Using an iterative solution with a stack is actually the same as BFS, just using a stack instead of a queue - so you get both `O(|V|)` time and space complexity.  
(\*) Note that the space complexity and time complexity is a bit different for a tree than for a general graphs becase you do not need to maintain a `visited` set for a tree, and `|E| = O(|V|)`, so the `|E|` factor is actually redundant.
<!--ID: 1690027053744-->

---

DECK INFO

TARGET DECK: Javascript::Interview::ADSA - Master the coding interview data structures algorithms - andrei neagoie::Part I - Content::Chapter 1 - Content

FILE TAGS: Javascript Interview

Tags:

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```
