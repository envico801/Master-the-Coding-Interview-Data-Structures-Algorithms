Q: What is DFS?  
A: While iterating with this technique, we move over each node and edge exactly once, and once we are over a node that has already been visited then we backtrack, which means we are pruning possibilities that have already been marked. So hence the overall complexity is reduced from exponential to linear.  
**Pseudocode for DFS:**
> DFS(Graph, vertex)  
>     vertex.visited = true  
>     for each v1 ∈ Graph.Adj\[vertex\]  
>         if v1.visited ==  false  
>             DFS(Graph, v1)
<!--ID: 1693659888919-->

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