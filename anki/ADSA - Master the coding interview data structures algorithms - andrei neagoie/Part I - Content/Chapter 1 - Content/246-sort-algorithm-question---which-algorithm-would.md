Q: Sort algorithm question  
Which algorithm would you use for the following context?  
**Massive database (can't fit all into memory) needs to sort through past year's user data**
A: Merge sort  
We can fill all this data into memory to sort it So we probably need to sort it out externally and let's say we need to sort through past years user data So it's a ton of data and we need to sort it somehow let's say by some sort of a date. What based on the information that I got here it sounds like I need to do something called merge sort And the reason I would pick this is because well it sounds that we're not gonna be storing really in memory because the data is so big but because the data is so big I'm really worried about the performance. I don't want the worst case of quicksort of O(n^2).
<!--ID: 1690026322108-->

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
