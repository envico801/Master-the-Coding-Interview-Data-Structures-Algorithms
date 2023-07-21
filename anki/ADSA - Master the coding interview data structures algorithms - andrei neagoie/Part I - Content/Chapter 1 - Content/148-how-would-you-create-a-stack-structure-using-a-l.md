Q: How would you create a stack structure using a linked list?
A: -
```javascript
class Node {
  constructor(value) {
    this.value = value;
    this.next = null;
  }
}
class Stack {
  constructor() {
    this.top = null;
    this.bottom = null;
    this.length = 0;
  }
  peek() {
    return this.top;
  }
  push(value) {
    const newNode = new Node(value);
    if (this.length === 0) {
      this.top = newNode;
      this.bottom = newNode;
    } else {
      const holdingPointer = this.top;
      this.top = newNode;
      this.top.next = holdingPointer;
    }
    this.length++;
    return this;
  }
  pop() {
    if (!this.top) {
      return null;
    }
    if (this.top === this.bottom) {
      this.bottom = null;
    }
    const holdingPointer = this.top;
    this.top = this.top.next;
    this.length--;
    return this;
  }
  //isEmpty
}
const myStack = new Stack();
myStack.peek();
myStack.push('google');
myStack.push('udemy');
myStack.push('discord');
myStack.peek();
myStack.pop();
myStack.pop();
myStack.pop();
//Discord
//Udemy
//google
```
<!--ID: 1689972344618-->



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
