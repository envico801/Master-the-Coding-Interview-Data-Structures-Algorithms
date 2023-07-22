Q: Implement a function that reverses a string using iteration...and then recursion!
```javascript
function reverseString(str) {}
reverseString('yoyo mastery');
//should return: 'yretsam oyoy'
```  
A: -
```javascript
function reverseString(str) {
  let arrayStr = str.split('');
  let reversedArray = [];
  //We are using closure here so that we don't add the above variables to the global scope.
  function addToArray(array) {
    if (array.length > 0) {
      reversedArray.push(array.pop());
      addToArray(array);
    }
    return;
  }
  addToArray(arrayStr);
  return reversedArray.join('');
}
reverseString('yoyo master');
function reverseStringRecursive(str) {
  if (str === '') {
    return '';
  } else {
    return reverseStringRecursive(str.substr(1)) + str.charAt(0);
  }
}
reverseStringRecursive('yoyo master');
```
<!--ID: 1690032123549-->

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
