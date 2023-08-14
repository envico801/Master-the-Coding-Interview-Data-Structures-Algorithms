Q: How would you implement selection sort?  
A: -
```javascript
const numbers = [99, 44, 6, 2, 1, 5, 63, 87, 283, 4, 0];
function selectionSort(array) {
  const length = array.length;
  for (let i = 0; i < length; i++) {
    // set current index as minimum
    let min = i;
    let temp = array[i];
    for (let j = i + 1; j < length; j++) {
      if (array[j] < array[min]) {
        //update minimum if current is lower that what we had previously
        min = j;
      }
    }
    array[i] = array[min];
    array[min] = temp;
  }
  return array;
}
selectionSort(numbers);
console.log(numbers);
```


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