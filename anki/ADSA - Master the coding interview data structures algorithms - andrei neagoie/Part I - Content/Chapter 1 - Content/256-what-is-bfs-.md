Q: What is BFS?  
A: In this technique, each neighboring vertex is inserted into the queue if it is not visited. This is done by looking at the edges of the vertex. Each visited vertex is marked visited once we visit them hence, each vertex is visited exactly once, and all edges of each vertex are checked. So the complexity of BFS is V + E  
**Pseudocode for BFS:**
> create a queue Q
>
> v.visited = true
>
> Q.push(v)  
> while Q is non-empty  
>    remove the head u of Q  
>    mark and enqueue all (unvisited) neighbours of u
Since we are only iterating over the graph’s edges and vertices only once, hence the time complexity for both the algorithms is linear **O(V+E)**.  
Auxiliary Space Taken is O(V) at worst case.
<!--ID: 1690376045610-->

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

QUESTION STATUS: Safe to store