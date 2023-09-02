Q: What properties does a perfect binary tree has?  
A: 1.The number of total nodes doubles as we move down the tree  
2.The number of nodes on the last level is equal to the sum of the number of nodes on all the other levels plus 1
```text
Level 0: 2^0 = 1
Level 1: 2^1 = 2
Level 2: 2^2 = 4
Level 3: 2^3 = 8
```
Based on that formula, we can find the number of nodes in a tree:
\# of nodes = 2^h - 1 **(h is the level, starts from count of 1)**
log nodes = height/steps (simplified version)
log 100 = 2
10^2 = 100
<!--ID: 1693659893989-->

---

DECK INFO

TARGET DECK: Javascript::Interview::ADSA - Master the coding interview data structures algorithms - andrei neagoie::Part I - Content::Chapter 1 - Content

FILE TAGS: #Javascript #Interview

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```


QUESTION STATUS: Safe to store