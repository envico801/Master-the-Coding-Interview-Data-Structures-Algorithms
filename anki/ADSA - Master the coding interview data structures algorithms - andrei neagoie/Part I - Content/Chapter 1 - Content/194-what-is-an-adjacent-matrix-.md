Q: What is an adjacent matrix?  
A: A graph representation by an array matrix which contain 0s and 1s that show the relationship of vertices to other vertices in the graph.  
It will indicate if node X has a connection to node Y, 0 means NO, 1 means YES  
If you have a weighted graph you can add weights here instead of 1 (is replaced by the weight) and 0
```javascript
// The index in this case is the value of the actual graph node
// We can use an object to apply keys instead of indexes
const graph = [
  [0, 0, 1, 0], // 0 -> 2
  [0, 0, 1, 1], // 1 -> 2,3
  [1, 1, 0, 1], // 2 -> 0,1,3
  [0, 1, 1, 0], // 3 -> 1,2
];
```
<!--ID: 1690032123599-->

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
