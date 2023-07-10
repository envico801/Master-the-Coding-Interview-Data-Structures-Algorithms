# ADSA - Master the coding interview data structures algorithms - andrei neagoie

## Questions

### 3. Big O

#### C2

Q: What is the official term for Big O?  
A: The official term is Big O asymptomatic analysis.

Q: What can big O tell us about a problem?
A: It can tell us how well a problem is solved.

#### C4

Q: What is good code?  
A: Is the code that is:
1.Readable (is your code clean? can others understand your code?)
2.Scalable (when we grow bigger and bigger with our input how much does the algorithm or function slow down?)

#### C5

Q: What is algorithmic efficiency?  
A: The term algorithmic efficiency is used to describe those properties of algorithms that are related to the amount of resources used by the algorithm. Usually referred to as scalability(Big O)

#### C6

Q: What does linear time mean?  
A: If an algorithm is in the order of O(n), or linear time complexity, the number of operations it performs scales in direct proportion to the input.
e.g. (for loops, while loops through n items)

#### C7

Q: What does constant time mean?  
A: Constant time means that the number of steps/operations does not depend on the input size. Also known as O(1). Predictability is always good

#### C13

Q: What does the rule of "worst-case" mean?
A: It means that we always worry about the worst case, because when we talk about scalability we can never assume that things are going to go well (you don't know how the input is going to be). When we talk about Big O we always talk about the worst case scenario.

#### C14

Q: What does the rule of "eliminating constants" mean?
A: As the name says, if Big 0 is the product of multiple terms, constant terms are eliminated (constant terms are like static numbers, numbers like 1, 4, 5, basically anything that is not a variable).
We only care about when it scales, when the size of the input is getting larger and larger.

Q: What is the big O of iterating over half a collection?
A: It ends up being O(n) because if we apply basic mathematics we can transform the division into a multiplication **(n/2 = 1/2 x n)** and then apply the rule of eliminating constants.

#### C15

Q: What does the rule of "different terms for inputs" mean?
A: It means that different notations/variables are used for different inputs, because since we do not know the length of each one, we cannot assume that they are the same.  
1.**O(n) is different from O(a + b)**  
2.**O(n^2) is different from O(a \* b)**

Q: When calculating big O and having steps in order (one below the other), which operation should be used?
A: Addition (+) must be used for steps in order

Q: When calculating large O and having nested steps (a loop within a loop), which operation should be used?
A: Multiplication (\*) must be used for nested steps.

#### C16

Q: What does quadratic time mean?  
A: It means that the number of operations it performs is proportional to the square of the input.
e.g. Every element in a collection needs to be compared to ever other element. Two
nested loops

#### C17

Q: What does the rule of "drop non dominants" mean?
A: It means that we prioritize the term that has more weight (scale) at the moment of calculating the big O.  
1.**O(n^2+3n+100+n/2) is equal to O(n^2)**

#### C19

Q: What are data structures?
A: They are a way of storing data.  
You could say they are a collection of values and these values can have relationships between them and functions can be applied to them.  
The most important thing is that each data structure is good and specialized in its own thing.

Q: What are algorithms?
A: These are the steps or processes we put in place to manipulate our data structures to write our programs (instructions for our computer).

#### C20

Q: What does factorial time mean?  
A: It means that the number of operations will be proportional to the factorial of the input.
**We will find ourselves writing algorithms with factorial time complexity when calculating permutations and combinations.**
Factorial is the multiplication of all positive integer numbers less than itself. For instance:
The factorial of 5, or _5!_, is:

```text
5 * 4 * 3 * 2 * 1 = 120
```

#### C21

Q: What are the 3 pillars of good coding?
A: 1.Readable: (clean code) that can be maintained and others can read.
2.Speed: (time complexity) that has a Big O that is efficient, scales well.
3.Memory: (space complexity)

#### C22

Q: What causes Space complexity? **(how much memory or resources it occupies as the input grows)**
A: 1.Variables (assignments and mutability with objects)
2.Data Structures (both custom and native)
3.Function Call (function calls, e.g. a recursive one, which is stored in memory as a stack.)
4.Allocations (when we create variables, functions or anything else that is stored in the memory)

#### C24

Q: What would you say is the Big O in the following sentence?

```javascript
'asdasdljasdk'.length;
```

A: It depends on the language you are working with, we need to know how the method is implemented to be able to give an accurate answer.

#### Extras

Q: What can cause time in a function? **(how long does it take to traverse / solve something as the input grows, how many operations does it have to perform?)**
1.Operations (+, -, \*, /)
2.Comparisons (<, >, ==)
3.Looping (for, while)
4.Outside Function call (function()) (can be a call to a recursive function or to a regular function.)

Q: List the common Big O complexities from worst to best (there are 7)  
A: O(n!)  
O(2^n)  
O(n^2)  
O(n log n)  
O(n)  
O(log n)  
O(1)

Q: Space complexity is not concerned with the size of the input per se but the...  
A: ...memory that is being allocated for each operation.

### 4. How To Solve Coding Problems

#### C2

Q: What skills does the interviewer look for?
A: 1.Analytic Skills - How can you think through problems and analyze things? - (e.g. can you come up with alternatives to solve the problem?)  
2.Coding Skills - Do you code well, by writing clean, simple, organized, readable code? - (e.g. Big O)  
3.Technical knowledge - Do you know the fundamentals of the job you're applying for? - (e.g. language JavaScript)  
4.Communication skills: Does your personality match the companies’ culture?

### 5. Data Structures: Introduction

#### C3

Q: What is RAM used for?  
A: RAM is used for immediate data storage and retrieval

Q: What is a memory address?  
A: It is a reference to a specific memory location

Q: What is a bit (binary digit)?  
A: A bit (binary digit) is the smallest unit of data that a computer can process and store.  
A bit is always in one of two physical states, similar to an on/off light switch. The state is represented by a single binary value, usually a 0 or 1.

Q: What is a byte?  
A: A byte is a sequence of 8 bits that are treated as a single unit.

Q: What is a memory controller?  
A: A memory controller is a device that manages the data flow between the CPU and system RAM.  
The memory controller acts as the middleman in these operations, ensuring that the proper information is retrieved from the right locations.  
**The closer the information is to the CPU and the less it has to travel, the faster a program can be executed.**

Q: What is CPU cache?  
A: It is a cache memory that is used to reduce the average memory access time.  
**It's like a mini RAM integrated in the CPU.**

Q: Why is it said that there are no integers in JavaScript?  
A: There is only the [Number](http://www.ecma-international.org/ecma-262/6.0/index.html#sec-ecmascript-language-types-number-type) data type in JS that represents numbers.  
**Internally it is implemented as [IEEE 754](http://www.ecma-international.org/ecma-262/6.0/index.html#sec-terms-and-definitions-number-value) double precision floating point number.**  
What it means is that - technically there is no dedicated data type that represents integer numbers.  
Practically it means that we can safely use only numbers that are safely representable by the aforementioned standard. And it includes integer values in the range: `[-9007199254740991; 9007199254740991]`. Both values are defined as constants: [`Number.MIN_SAFE_INTEGER`](http://www.ecma-international.org/ecma-262/6.0/index.html#sec-number.min_safe_integer) and [`Number.MAX_SAFE_INTEGER`](http://www.ecma-international.org/ecma-262/6.0/index.html#sec-number.max_safe_integer) correspondingly.  
[Is there or isn't there an integer type in JavaScript?](https://stackoverflow.com/questions/33773296/is-there-or-isnt-there-an-integer-type-in-javascript)

#### C5

Q: What are the actions that can be performed on a data structure?
A:
1.Insertion: Add a new data item in a given collection of items
2.Deletion: Delete data from a collection
3.Traversal: Access to each data item exactly once so it can be processed
4.Searching: Find the location of the data item if it exists in a given collection
5.Sorting: Having data that is sorted
6.Access: How do we access this data that we have on our computer

#### Extras

Q: What are the 2 pillars of Data Structures?  
A: How to build one  
How to use one

### 6. Data Structures: Arrays

#### C1

Q: What is an array?
A: An array is a collection of items stored at contiguous memory locations.

Q: What is the Big O for an Array lookup operation? (aka **access**: Array\[2\])  
A: O(1)

Q: What is the Big O for an Array find operation? (aka **search**: Array.find(callbackFn))  
A: O(n)
e.g. We traverse the entire array to check if an element is present.

Q: What is the Big O of an Array push/append operation? (aka **insertion**: Array.push(value))  
A: O(1) if the array is static  
O(n) if the array is dynamic and has to grow when the new value is added.
or if we are using other methods like (shift(), splice())
**Note that the worst case is still O(n).**

Q: What is the Big O of an Array shift operation? (aka **insertion**: Array.shift(value))  
A: O(n)

Q: What is the Big O of an Array pop operation? (aka **deletion**: Array.pop())  
A: O(1)
**Note that the worst case is still O(n). - (unshift, splice, etc)**

Q: What is the Big O of an Array unshift operation? (aka **deletion**: Array.unshift())  
A: O(n)

#### C2

Q: What are the 2 types of Arrays?  
A: Dynamic and Static

Q: What is a dynamic array?  
A: An array that can grow in size when it needs to. No specification of size is needed when it is initiated.

Q: What is a static array?  
A: A fixed size array. Must specify the size when it is initiated.

#### C5

Q: In JavaScript, what data structure is an Array actually?  
A: An Object which contains properties and methods which make it Array-like.

Q: How would you create an array structure?
A: You may use an object:

```javascript
class MyArray {
  constructor() {
    this.length = 0;
    this.data = {};
  }
  get(index) {
    return this.data[index];
  }
  push(item) {
    this.data[this.length] = item;
    this.length++;
    return this.data;
  }
  pop() {
    const lastItem = this.data[this.length - 1];
    delete this.data[this.length - 1];
    this.length--;
    return lastItem;
  }
  deleteAtIndex(index) {
    const item = this.data[index];
    this.shiftItems(index);
    return item;
  }
  shiftItems(index) {
    for (let i = index; i < this.length - 1; i++) {
      this.data[i] = this.data[i + 1];
    }
    console.log(this.data[this.length - 1]);
    delete this.data[this.length - 1];
    this.length--;
  }
}

const myArray = new MyArray();
myArray.push('hi');
myArray.push('you');
myArray.push('!');
myArray.pop();
myArray.deleteAtIndex(0);
myArray.push('are');
myArray.push('nice');
myArray.shiftItems(0);
console.log(myArray);
```

#### C6

Q: How should we handle questions related to strings?
A: We should treat it as an array question, strings are an array of characters.
e.g. reverse a string.

#### C12

Q: What are the pros of using arrays?
A: 1.Fast lookups (accessing information where you know which index you want to look at)
2.Fast push/pop (adding or removing things at the end of an array)
3.Ordered (having something that is ordered and close to each other in memory makes it really fast)

Q: What are the cons of using arrays?
A: 1.Slow inserts (we have to shift the array when at the very end of the array)
2.Slow deletes (same as inserts)
3.Fixed size\* (sometimes you have to declare the memory ahead of time and how large of an array you want. Most modern languages have dynamic arrays that help with this)

### 7. Data Structures: Hash Tables

#### C1

Q: What are Hash Tables?  
A: **Collections of { Key: Value } pairs**
A Hash table is defined as a data structure used to insert, look up, and remove key-value pairs quickly.  
It operates on the [hashing concept](https://www.geeksforgeeks.org/what-is-hashing/), where each key is translated by a hash function into a distinct index in an array. The index functions as a storage location for the matching value. In simple words, it maps the keys with the value. (it will store the key and the value at the same address in memory - a "bucket")

```text
Input = Grape
Output (is always) = G7xpLLQ4
G7xpLLQ4 -> key:value
```

#### C2

Q: What is a Hash function?  
A: A function that generates a value of fixed length for each input it receives. For any given input, the output will always be the same.  
Examples:

```text
Input = Grape
Output (is always) = G7xpLLQ4
Input = 5
Output (is always) = Ax67def0
```

Q: What does it mean for a function to be "idempotent"?
A: It is a fancy way of saying that a function given an input always outputs the same output

#### C3

Q: What is the Big O for insertion into a Hash Table?  
A: O(1)  
Unless there is a collision, then it would be O(n / k) where k = the length of the address being accessed.

Q: What is the Big O for a lookup (access) in a Hash Table?  
A: O(1)
Unless there is a collision, then it would be O(n / k) where k = the length of the address being accessed.

Q: What is the Big O for deletion in a Hash Table?  
A: O(1)
Unless there is a collision, then it would be O(n / k) where k = the length of the address being accessed.

Q: What is the Big O for a search in a Hash Table?  
A: O(1)
e.g. `object["key"]` It will return if that key is present in the object (undefined otherwise), that's why it is O(1).
Unless there is a collision, then it would be O(n / k) where k = the length of the address being accessed.

Q: What is a collision in regards to a Hash Table?  
A: When a new item is added to the same "address" as an already existing item in a Hash Table.  
This could slow down the lookup for a Hash Table from O(1) to O(n / k) where k = the size of the address being accessed.

#### C4

Q: What kind of _data-type_ is a **Key** in a typical Hash Table?  
A: A String

Q: In ES6, what kind of _data-types_ can a **Key** be for a Map?  
A: Any kind of data-type

Q: In ES6, what kind of Hash Table maintains insertion order?  
A: A Map

Q: Does a Set store values in JavaScript?  
A: No, only Keys which are unique (no two keys can be the same in a Set).

#### C6

Q: How would you create an object structure?
A: You may use an array:

```javascript
class HashTable {
  constructor(size) {
    this.data = new Array(size);
    // this.data = [];
  }

  _hash(key) {
    let hash = 0;
    for (let i = 0; i < key.length; i++) {
      hash = (hash + key.charCodeAt(i) * i) % this.data.length;
    }
    return hash;
  }

  set(key, value) {
    let address = this._hash(key);
    if (!this.data[address]) {
      this.data[address] = [];
    }
    this.data[address].push([key, value]);
    return this.data;
  }

  get(key) {
    const address = this._hash(key);
    const currentBucket = this.data[address];
    if (currentBucket) {
      for (let i = 0; i < currentBucket.length; i++) {
        if (currentBucket[i][0] === key) {
          return currentBucket[i][1];
        }
      }
    }
    return undefined;
  }
}

const myHashTable = new HashTable(50);
myHashTable.set('grapes', 10000);
myHashTable.get('grapes');
myHashTable.set('apples', 9);
myHashTable.get('apples');
```

#### C7

Q: Which data-structure is more efficient at looping over data: An Array or a Hash Table?  
A: An Array.  
If your Hash Table has 50 addresses but only 3 addresses contain Keys, you would still have to access all 50 addresses to obtain those Keys.  
An Array is sequential in memory, which makes it more efficient in this regard.

#### C12

Q: What are the pros of using hash tables?
A: 1.Fast lookups\* (Good collision resolution needed, usually we dont need to worry about this because our language underneath the hood take care of that for us)
2.Fast inserts (same as lookups)
3.Flexible keys (depending on the type of hash tables, such as maps, we can have flexibles keys instead of an array that has numbered indexes)

Q: What are the cons of using hash tables?
A: 1.Unordered (its hard to really go through everything in order)
2.Slow key iteration (if i want to grab all the keys from a hash table I will have to go through the entire memory space)

### 8. Data Structures: Linked Lists

#### C1

Q: Can Linked Lists help solve collision issues in a Hash Table?  
A: Yes

#### C2

Q: What is a Linked List?  
A: A collection of nodes and pointers.  
Data is stored in the node itself and a pointer is a reference to the next node in the list.  
The end of a Linked List is signified by a "null" value.

Q: How its called the first node in a linked list?
A: Head.

Q: How its called the last node in a linked list?
A: Tail.
Some people call the tail anything that is after the head.

Q: How do you know that you have reached the end of a Linked List?  
A: Linked Lists are "null-terminated" which means the end of the list is denoted by the value "null".

#### C4

Q: What kind of structure do Linked Lists have?  
A: A 'loose' structure. You can easily insert a new data as you only have to change 2 pointers (depending on if it is singly linked, doubly linked, etc..)

Q: What is the main difference between a Linked List and an Array?  
A: Arrays are indexed, Linked Lists are not.  
If you want to access the 5th element in a Linked List, you have to start from the beginning of the list and traverse to the 5th element.  
In an Array, you can simply access the element at index 4 ( arr\[4\] ) to get the value of the 5th element.

Q: Are nodes in a Linked List stored sequentially in memory?  
A: No. They are scattered over memory which makes traversal of a Linked List slower than traversal of an Array.

Q: Whats one advantage that linked list have over hash tables?
A: That there is some sort of order to link list, each node points to the next node.

Q: What is the Big O for a prepend (add to the beginning of the list) operation on a Linked List/Double link list?  
A: O(1)

Q: What is the Big O of an append (add to the end of the list) operation on a Linked List/Double link list?  
A: O(1)

Q: What is the Big O of a lookup (traversal) operation on a Linked List/Double link list?  
A: O(n)
e.g. We go through the whole linked list to check if an element is present. In the case of a double linked list it would technically be O(n/2) because we can start at both ends and if we know in which half of the list is what we are looking for, we can choose the optimal place to start.

Q: What is the Big O of an insertion operation on a Linked List/Double link list?  
A: O(n)

Q: What is the Big O of a deletion operation on a Linked List/Double link list?  
A: O(n)

#### C5

Q: What is a pointer?  
A: A pointer is a reference to another place in a memory (another node). Kind of like a variable referencing another variable.

#### C14

Q: What does a Doubly Linked List have that a Singly Linked List does not?  
A: A 'previous' pointer which references the node before it. You can traverse forwards and backwards through a Doubly Linked List. You can only traverse forwards in a Singly Linked List.

Q: Does a Doubly Linked List use more memory than a Singly Linked List?  
A: Yes. The 'previous' pointer will require more memory for the Doubly Linked List to be implemented.

#### C16

Q: How would you create a double linked list structure?
A:-

```javascript
class DoublyLinkedList {
  constructor(value) {
    this.head = {
      value: value,
      next: null,
      prev: null,
    };
    this.tail = this.head;
    this.length = 1;
  }
  append(value) {
    const newNode = {
      value: value,
      next: null,
      prev: null,
    };
    console.log(newNode);
    newNode.prev = this.tail;
    this.tail.next = newNode;
    this.tail = newNode;
    this.length++;
    return this;
  }
  prepend(value) {
    const newNode = {
      value: value,
      next: null,
      prev: null,
    };
    newNode.next = this.head;
    this.head.prev = newNode;
    this.head = newNode;
    this.length++;
    return this;
  }
  printList() {
    const array = [];
    let currentNode = this.head;
    while (currentNode !== null) {
      array.push(currentNode.value);
      currentNode = currentNode.next;
    }
    return array;
  }
  insert(index, value) {
    //Check for proper parameters;
    if (index >= this.length) {
      return this.append(value);
    }

    const newNode = {
      value: value,
      next: null,
      prev: null,
    };
    const leader = this.traverseToIndex(index - 1);
    const follower = leader.next;
    leader.next = newNode;
    newNode.prev = leader;
    newNode.next = follower;
    follower.prev = newNode;
    this.length++;
    console.log(this);
    return this.printList();
  }
  traverseToIndex(index) {
    //Check parameters
    let counter = 0;
    let currentNode = this.head;
    while (counter !== index) {
      currentNode = currentNode.next;
      counter++;
    }
    return currentNode;
  }
}

let myLinkedList = new DoublyLinkedList(10);
myLinkedList.append(5);
myLinkedList.append(16);
myLinkedList.prepend(1);
myLinkedList.insert(2, 99);
// myLinkedList.insert(20, 88)
// myLinkedList.printList()
// myLinkedList.remove(2)
// myLinkedList.reverse()
```

#### C17

Q: What are the advantages of a **linked list** over a double linked list?
A: 1.Fairly simple implementation (compared to the double link list)
2.Requires less memory (when we do things like delete and insert because there is technically less operation, we dont have to move around the previous property, its a little bit faster)

Q: What are the disadvantages of a **linked list** over a double linked list?
A: 1.It cannot be iterated in reverse or traverse from back to front (if we ever lose the reference to `this.head` of the list, the list can actually be lost in memory forever)

Q: What are the advantages of a **double linked** list over a linked list?
A: 1.It can be iterated or traversed both from the front or from the back.
2.Easy insert or delete (if you need to delete a previous node, you don't need to traverse from the head node and find what the previous node is)

Q: What are the disadvantages of a **double linked** list over a linked list?
A: 1.Fairly complex (it requires more memory and storage because of this extra property and there are some actual operations that we need to perform to make sure that we when we do insert and delete that the previous property is updated as well).

Q: What are the pros of using linked lists?
A: 1.Fast insertion (if we had a large number of elements in an array and kept adding to that array we would have to have excessive overhead copying the array into memory and doubling the space when it reached the limit to create a larger array. Versus a linked list where we can have fast insertion and fast deletion especially once we have a reference to where we want to insert or delete that node).
2.Fast deletion (same as insertion)
3.Ordered (linked lists allow us to have this sort of order.)
4.Flexible size (this is the primary reason to choose a linked list over something like an array is simplicity and ability to grow and shrink as needed.)

Q: What are the cons of using linked lists?
A: 1.Slow lookup (we have to traverse through the list if we're searching for something.)
2.More memory (we store more properties in memory, in the case of a double linked list we are storing the `value - next - prev`)

#### C19

Q: How would you create a linked list structure?
A:-

```javascript
class LinkedList {
  constructor(value) {
    this.head = {
      value: value,
      next: null,
    };
    this.tail = this.head;
    this.length = 1;
  }
  append(value) {
    const newNode = {
      value: value,
      next: null,
    };
    console.log(newNode);
    this.tail.next = newNode;
    this.tail = newNode;
    this.length++;
    return this;
  }
  prepend(value) {
    const newNode = {
      value: value,
      next: null,
    };
    newNode.next = this.head;
    this.head = newNode;
    this.length++;
    return this;
  }
  printList() {
    const array = [];
    let currentNode = this.head;
    while (currentNode !== null) {
      array.push(currentNode.value);
      currentNode = currentNode.next;
    }
    return array;
  }
  insert(index, value) {
    //Check for proper parameters;
    if (index >= this.length) {
      console.log('yes');
      return this.append(value);
    }

    const newNode = {
      value: value,
      next: null,
    };
    const leader = this.traverseToIndex(index - 1);
    const holdingPointer = leader.next;
    leader.next = newNode;
    newNode.next = holdingPointer;
    this.length++;
    return this.printList();
  }
  traverseToIndex(index) {
    //Check parameters
    let counter = 0;
    let currentNode = this.head;
    while (counter !== index) {
      currentNode = currentNode.next;
      counter++;
    }
    return currentNode;
  }
  remove(index) {
    // Check Parameters
    const leader = this.traverseToIndex(index - 1);
    const unwantedNode = leader.next;
    leader.next = unwantedNode.next;
    this.length--;
    return this.printList();
  }
  reverse() {
    if (!this.head.next) {
      return this.head;
    }
    let first = this.head;
    this.tail = this.head;
    let second = first.next;

    while (second) {
      const temp = second.next;
      second.next = first;
      first = second;
      second = temp;
    }

    this.head.next = null;
    this.head = first;
    return this.printList();
  }
}

let myLinkedList = new LinkedList(10);
myLinkedList.append(5);
myLinkedList.append(16);
myLinkedList.prepend(1);
myLinkedList.printList();
myLinkedList.insert(2, 99);
myLinkedList.insert(20, 88);
myLinkedList.printList();
myLinkedList.remove(2);
myLinkedList.reverse();
```

### 9. Data Structures: Stacks + Queues

#### C1

Q: What kind of data-structure are Stack and Queues?  
A: Linear data-structures. They must be traversed one by one.

Q: What is the difference between a Stack and a Queue?  
A: The order in which the elements are processed.  
A Stack pops the most recent element from the top (Last In First Out)  
A Queue processes the first element that went in (First In First Out)

#### C2

Q: What is the Big O for a lookup operation in a Stack?  
A: O(n)
Q: What is the Big O for a pop operation in a Stack?  
A: O(1)

Q: What is the Big O for a push operation in a Stack?  
A: O(1)

Q: What is the Big O for a peek operation in a Stack? (view the top of the stack)  
A: O(1)

Q: What does LIFO stand for in regard to a Stack?  
A: Last In First Out

#### C3

Q: What is the Big O for a lookup operation in a Queue?  
A: O(n)

Q: What is the Big O for a enqueue operation in a Queue?  
A: O(1)

Q: What is the Big O for a dequeue operation in a Queue?  
A: O(1) - If you did not use an Array to implement the queue.  
An Array unshift operation would be O(n).

Q: What is the Big O for a peek operation in a Queue? (see who is the fist in the queue)  
A: O(1)

Q: What does FIFO stand for in regards to a Queue?  
A: First In First Out

#### C7

Q: What is a program?
A: Well a program has to do some simple things.
1.It has to allocate memory. Otherwise we would be able to have variables or even have a file on our computer.
2.It also has to parse and execute scripts which means read and run commands.

Q: How many parts has a engine (javascript)?
A: Now the engine consists of two parts a memory heap and a call stack.
1.Now the memory heap. This is where the memory allocation happens.
2.And then the call stack. This is where your code is read and execute it. It tells you where you are in the program.

Q: What is a memory leak?
A: Memory leak occurs when programmers create a memory in heap and forget to delete it.

Q: What does it mean that javascript is a single threaded language that can be nonblocking?
A: Single threaded means that it has only one call stack. And one call stack only you can only do one thing at a time Now other languages can have multiple calls. And these are called multi-thread.

Q: Why was javascript designed to be single threaded?
A: While running code on a single thread can be quite easy since you don't have to deal with complicateda scenarios that arise in multithreaded environment. You just have one thing to worry about.

Q: What is a deadlock?
A: A deadlock is a situation where a set of processes are blocked because each process is holding a resource and waiting for another resource acquired by some other process.

#### C9

Q: How would you create a stack structure using a linked list?
A:-

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

#### C11

Q: How would you create a stack structure using an array?
A:-

```javascript
class Stack {
  constructor() {
    this.array = [];
  }
  peek() {
    return this.array[this.array.length - 1];
  }
  push(value) {
    this.array.push(value);
    return this;
  }
  pop() {
    this.array.pop();
    return this;
  }
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

#### C13

Q: How would you create a queue structure using a linked list?
A:-

```javascript
class Node {
  constructor(value) {
    this.value = value;
    this.next = null;
  }
}

class Queue {
  constructor() {
    this.first = null;
    this.last = null;
    this.length = 0;
  }
  peek() {
    return this.first;
  }
  enqueue(value) {
    const newNode = new Node(value);
    if (this.length === 0) {
      this.first = newNode;
      this.last = newNode;
    } else {
      this.last.next = newNode;
      this.last = newNode;
    }
    this.length++;
    return this;
  }
  dequeue() {
    if (!this.first) {
      return null;
    }
    if (this.first === this.last) {
      this.last = null;
    }
    const holdingPointer = this.first;
    this.first = this.first.next;
    this.length--;
    return this;
  }
  //isEmpty;
}

const myQueue = new Queue();
myQueue.peek();
myQueue.enqueue('Joy');
myQueue.enqueue('Matt');
myQueue.enqueue('Pavel');
myQueue.peek();
myQueue.dequeue();
myQueue.dequeue();
myQueue.dequeue();
myQueue.peek();
```

#### C14

Q: How would you create a queue using 2 stacks?
A:-

```javascript
class CrazyQueue {
  constructor() {
    this.first = [];
    this.last = [];
  }

  enqueue(value) {
    const length = this.first.length;
    for (let i = 0; i < length; i++) {
      this.last.push(this.first.pop());
    }
    this.last.push(value);
    return this;
  }

  dequeue() {
    const length = this.last.length;
    for (let i = 0; i < length; i++) {
      this.first.push(this.last.pop());
    }
    this.first.pop();
    return this;
  }
  peek() {
    if (this.last.length > 0) {
      return this.last[0];
    }
    return this.first[this.first.length - 1];
  }
}

const myQueue = new CrazyQueue();
myQueue.peek();
myQueue.enqueue('Joy');
myQueue.enqueue('Matt');
myQueue.enqueue('Pavel');
myQueue.peek();
myQueue.dequeue();
myQueue.dequeue();
myQueue.dequeue();
myQueue.peek();
```

#### C15

Q: What are the pros of using stacks and queues?
A: 1.Fast operations (such as removing or inserting, such as the end of the data structure)
2.Fast peek (we can access the very first item in a queue or the very top item in a stack)
3.Ordered (we have all our data ordered)

Q: What are the cons of using stacks and queues?
A: 1.Slow lookup (we dont usually use ours stack or queues to do any sort of look up or search through the data structure, all we are interested in is the end bits of the data structure)

### 10. Data Structures: Trees

#### C1

Q: What is a Tree data-structure?  
A: A hierarchical data-structure consisting of a root node and parent/child nodes.  
A Linked List is technically a type of Tree but it is linear instead of having multiple 'branches' or paths.

Q: What is a abstract syntax tree?
A: This is how programs and code is usually run

#### C2

Q: What is the rule for implementing a Binary Tree?  
A: Each node can have a max of 2 children.  
So a node can have 0, 1, or 2 children.
And each child can only have one parent
Each node represent a certain state

Q: What is a perfect binary tree?
A: A perfect binary tree has everything filled in, that means that all the leaf nodes are full and there is no node that only has one child, a node either has zero or two children. Also, the bottom layer of the tree is completely filled, nothings is missing

Q: What is a full binary tree?
A: A full binary tree says that a node has either 0 or 2 children, but never one child

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

Q: What is the time complexity for a perfect binary tree's search(lookup), insert, and delete methods?  
A: O(log n)

#### C3

Q: What does logarithmic time mean?  
A: All that is saying is that the choice of the next element on which to perform some sort of action is one of several possibilities and only one needs to be chosen.
e.g. (usually searching algorithms have log n if they are sorted (Binary Search))

#### C4

Q: What is a binary search tree?
A: BSTs excel at preserving relationships, making them suitable for scenarios where maintaining order and structure is important.  
For instance, while a hash table lacks such relationships, organizing folders on a computer necessitates a hierarchical structure with parent and subfolders, which can be achieved using a binary search tree.  
1.In a BST, all child nodes to the right of a root node must have values greater than the current node. This implies that moving to the right within the tree leads to nodes with increasing values, while moving to the left results in nodes with decreasing values.
2.Due to its nature as a binary tree, each node in a BST can have a maximum of two children.

#### C5

Q: If a binary tree is unbalanced, what is its worst case time complexity?  
A: O(n) for lookup(search), insert and delete

Q: How does a binary tree become unbalanced?  
A: A binary tree becomes unbalanced when new nodes are continually placed to the right of one node and its children or to the left of one node and its children (as opposed to spreading them out evenly to keep the left and right sides about the same height, the tree becomes really long on on side).

Q: How can you tell if a binary tree is balanced?  
A: A binary tree is balanced when every node has roughly the same amount of children.

#### C6

Q: What are the pros of using BSTs?
A: 1.Better than O(n) (most operations are log n, assuming that the BST is balanced)
2.Ordered
3.Flexible size (because we can place a node anywhere in memory we can just have flexible size , we can keep growing our tree)

Q: What are the cons of using BSTs?
A: 1.No O(1) operations (we usually have to do some sort of traversal for any sort of operation)

#### C9

Q: What does divide and conquer refers to?
A: Divide and conquer simply means we are dividing up so that we dont visit all the nodes, each node that we visit we make a decision to go left or right

#### C11

Q: How would you create a BST structure?
A:-

```javascript
class Node {
  constructor(value) {
    this.left = null;
    this.right = null;
    this.value = value;
  }
}

class BinarySearchTree {
  constructor() {
    this.root = null;
  }
  insert(value) {
    const newNode = new Node(value);
    if (this.root === null) {
      this.root = newNode;
    } else {
      let currentNode = this.root;
      while (true) {
        if (value < currentNode.value) {
          //Left
          if (!currentNode.left) {
            currentNode.left = newNode;
            return this;
          }
          currentNode = currentNode.left;
        } else {
          //Right
          if (!currentNode.right) {
            currentNode.right = newNode;
            return this;
          }
          currentNode = currentNode.right;
        }
      }
    }
  }
  lookup(value) {
    if (!this.root) {
      return false;
    }
    let currentNode = this.root;
    while (currentNode) {
      if (value < currentNode.value) {
        currentNode = currentNode.left;
      } else if (value > currentNode.value) {
        currentNode = currentNode.right;
      } else if (currentNode.value === value) {
        return currentNode;
      }
    }
    return null;
  }
  remove(value) {
    if (!this.root) {
      return false;
    }
    let currentNode = this.root;
    let parentNode = null;
    while (currentNode) {
      if (value < currentNode.value) {
        parentNode = currentNode;
        currentNode = currentNode.left;
      } else if (value > currentNode.value) {
        parentNode = currentNode;
        currentNode = currentNode.right;
      } else if (currentNode.value === value) {
        //We have a match, get to work!

        //Option 1: No right child:
        if (currentNode.right === null) {
          if (parentNode === null) {
            this.root = currentNode.left;
          } else {
            //if parent > current value, make current left child a child of parent
            if (currentNode.value < parentNode.value) {
              parentNode.left = currentNode.left;

              //if parent < current value, make left child a right child of parent
            } else if (currentNode.value > parentNode.value) {
              parentNode.right = currentNode.left;
            }
          }

          //Option 2: Right child which doesnt have a left child
        } else if (currentNode.right.left === null) {
          currentNode.right.left = currentNode.left;
          if (parentNode === null) {
            this.root = currentNode.right;
          } else {
            //if parent > current, make right child of the left the parent
            if (currentNode.value < parentNode.value) {
              parentNode.left = currentNode.right;

              //if parent < current, make right child a right child of the parent
            } else if (currentNode.value > parentNode.value) {
              parentNode.right = currentNode.right;
            }
          }

          //Option 3: Right child that has a left child
        } else {
          //find the Right child's left most child
          let leftmost = currentNode.right.left;
          let leftmostParent = currentNode.right;
          while (leftmost.left !== null) {
            leftmostParent = leftmost;
            leftmost = leftmost.left;
          }

          //Parent's left subtree is now leftmost's right subtree
          leftmostParent.left = leftmost.right;
          leftmost.left = currentNode.left;
          leftmost.right = currentNode.right;

          if (parentNode === null) {
            this.root = leftmost;
          } else {
            if (currentNode.value < parentNode.value) {
              parentNode.left = leftmost;
            } else if (currentNode.value > parentNode.value) {
              parentNode.right = leftmost;
            }
          }
        }
        return true;
      }
    }
  }
}

const tree = new BinarySearchTree();
tree.insert(9);
tree.insert(4);
tree.insert(6);
tree.insert(20);
tree.insert(170);
tree.insert(15);
tree.insert(1);
tree.remove(170);
JSON.stringify(traverse(tree.root));

//     9
//  4     20
//1  6  15  170

function traverse(node) {
  const tree = { value: node.value };
  tree.left = node.left === null ? null : traverse(node.left);
  tree.right = node.right === null ? null : traverse(node.right);
  return tree;
}
```

#### C12

Q: What type of specialized binary trees can you use to maintain balance in a binary tree?  
A: An AVL tree or a Red/Black tree.

Q: For an AVL tree, what is the equation of the balance factor?  
**|h1 - h2|  <= 1** (Balance factor)  
**|h1 - h2|** can be equal to **\-1,0, or 1**.  
**h1** and **h2** are _subtrees of the same node_.  
The balance factor determines whether or not any given subtree of a tree is balanced.

Q: How many types of node-swapping operations does an AVL tree have to balance itself? What are they?  
A: **2** types of node-swapping operations:  
**Single Rotations** and **Double Rotations**.

Q: What are the 4 rules of a Red/Black Binary Tree?  
A: 1.Each node must be either Red or Black  
2.Root node must always be black  
3.A red node must always have a black parent node and black child nodes  
4.Every branch path (the path from root node to an empty leaf node \[null\]) must posess the exact same number of black nodes.  
Extras:  
A null leaf node is always considered to be black, even if it is marked red.  
A chain of 3 nodes can never be a valid Red/Black Tree.

#### C14

Q: What is a binary heap?  
A: A binary heap is a binary tree with the following properties:  
1.It's a complete tree. All levels are completely filled except possibly the last level, which will have elements positioned as left as possible.  
2.It is either a Min Heap or a Max Heap.  
In a Min Heap the root element must be the smallest (or the one with the least importance) among all elements present in the tree.  
In a Max Heap the root element must be the largest (or the one with the higher importance) of all elements present in the tree.
3.And have a max of 2 children (like a BT)

Q: What is the Big O for a lookup(search) operation in a Binary Heap?  
A: O(n) (because is less ordered than a than a BST, in this data structure left and right can be any value)

Q: What is the Big O for an insertion operation in a Binary Heap?  
A: O(log n) - O(1) in the best scenario, but if the order is broken it is possible to bubble upwards and this would result in the worst case (log n).

Q: What is the Big O for a deletion operation in a Binary Heap?  
A: O(log n)

Q: Where a BH (binary heap) can be used?
A: A BH can be used in any algorithm where ordering is important.

Q: What data-structure are Binary Heaps typically used to implement?  
A: A Priority Queue, data storage, sorting algorithms

Q: For what BH (binary heap) are good?
A: They are great at doing comparative operations
e.g. I want people that have a value over 33

#### C16

Q: Is a Binary Heap always balanced?  
A: Yes. Insertion order is left to right so they easily preserve their insertion order as well.

Q: What is a priority queue?
A: Is similar to a queue but with the difference that there are "vips" or higher priority values that usually take the first or last positions.

Q: What are the pros of using BH?
A: 1.Better than O(n)
2.Priority (searching may be slow, but you have an idea of priority, because insertion is done in order)
3.Flexible size
4.Fast insert (we might have to bubble up inserts every once in a while. But most of the time you get really fast inserts)

Q: What are the cons of using BH?
A: 1.Slow lookup (it must be taken into account that many times there is a method to find the minimum or maximum which is O(1) - (it all depends if it is a min heap or max heap))

#### C17

Q: What is a Trie (aka prefix tree)?  
A: A Trie is a unique type of tree that is an efficient infromation retrieval data structure. It commonly uses alphabetical characters to store data, like words. Often used to implement auto-correct for typing.  
In most cases it can outperform BSTs, hash tables and most others data structures. It will depend on what type of search we are doing

### 11. Data Structures: Graphs

#### C1

Q: What is a Graph?  
A: A Graph is a non-linear data structure consisting of nodes and edges. The nodes are sometimes referred to as vertices and the edges are lines or arcs that connect any two nodes in the graph.  
Technically Trees and Linked Lists are types of a Graph.

#### C2

Q: What is a directed graph?  
A: A graph whose nodes (vertexes) point in one direction. Like a one-way street going to the next node (vertex).

Q: What is an undirected graph?  
A: A graph whose nodes (vertexes) have no defined direction. A node (vertex) can only link to another node (vertex) if that other node (vertex) is also aware of the first node (vertex).  
Think of how Facebook works with friends. You cannot be someones friend on Facebook unless they are also your friend.

Q: What is a weighted graph?  
A: A graph whose edges have a value.  
This is useful in shortest path algorithms, like Dijkstra's algorithm.  
Weighted graphs are really common in cyclic graphs

Q: What is a cyclic graph?  
A: A graph which contains a cycle.  
You can start at one node (vertex) and make your way back to that same node by following other nodes back to the node you started on.  
Cyclic graphs are really common in weighted graphs

Q: What is an acyclic graph?  
A: A graph that contains no cycles.  
You cannot get back to a node you started from once you have left it.

#### C4

Q: What is an edge list?  
A: A collection of edges (connections) which represent a graph.
e.g.

```javascript
// a third element can be inserted into each array to apply a weight graph e.g. [0, 2 ,88]
const graph = [
  [0, 2],
  [2, 3],
  [2, 1],
  [1, 3],
];
```

Q: What is an adjacent list?  
A: A collection of vertices and their neighboring vertices which represents a graph.

```javascript
// The index is the node and the value is the nodes neighbors (we can use arrays, objects, linked lists)
// The index in this case is the value of the actual graph node
const graph = [
  [2], // 0
  [2, 3], // 1
  [0, 1, 3], // 2
  [1, 2], // 3
];
```

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

#### C6

Q: How would you create a graph structure?
A:-

```javascript
class Graph {
  constructor() {
    this.numberOfNodes = 0;
    this.adjacentList = {};
  }
  addVertex(node) {
    this.adjacentList[node] = [];
    this.numberOfNodes++;
  }
  addEdge(node1, node2) {
    //uniderected Graph
    this.adjacentList[node1].push(node2);
    this.adjacentList[node2].push(node1);
  }
  showConnections() {
    const allNodes = Object.keys(this.adjacentList);
    for (let node of allNodes) {
      let nodeConnections = this.adjacentList[node];
      let connections = '';
      let vertex;
      for (vertex of nodeConnections) {
        connections += vertex + ' ';
      }
      console.log(node + '-->' + connections);
    }
  }
}

var myGraph = new Graph();
myGraph.addVertex('0');
myGraph.addVertex('1');
myGraph.addVertex('2');
myGraph.addVertex('3');
myGraph.addVertex('4');
myGraph.addVertex('5');
myGraph.addVertex('6');
myGraph.addEdge('3', '1');
myGraph.addEdge('3', '4');
myGraph.addEdge('4', '2');
myGraph.addEdge('4', '5');
myGraph.addEdge('1', '2');
myGraph.addEdge('1', '0');
myGraph.addEdge('0', '2');
myGraph.addEdge('6', '5');

myGraph.showConnections();
```

#### C7

Q: What are the pros of using graphs?
A: 1.Relationships (some data needs to be in a graph form)

Q: What are the cons of using graphs?
A: 1.Scaling is hard (they can get complicated, you need a big company or at least a lot of resources and engineering power to make sure that you build graphs that scale well)

### 12. Algorithms: Recursion

#### C1

Q: What is an algorithm?  
A: Steps to complete a desired action in computers. Technically all functions are algorithms.
Algorithms allow us to use data structures to perform actions on data

```text
Data structures + Algorithms = Programs
Class {}        + function() = Programs
```

#### C2

Q: What is recursion?  
A: When a function refers to itself (calls on itself). Think of inception (the movie).  
It is good for tasks that have repeated subtasks to do

#### C4

Q: How do you terminate a recursive funtion?  
A: With a base case. Recursion breaks a task down into smaller tasks which terminate at the base case. This base case termination prevents the function from calling itself infinitely.

Q: What are the 3 rules for recursion?  
A: 1.Identify the base case  
2.Identify the recursive case  
3.Return something in the base case and return your recursive calls so the value from the base case persists through the call stack

#### C6

Q: Write two functions that finds the factorial of any number. One should use recursive, the other should just use a for loop

```javascript
function findFactorialRecursive(number) {
  //code here
  return answer;
}

function findFactorialIterative(number) {
  //code here
  return answer;
}
```

A:-

```javascript
function findFactorialIterative(number) {
  let answer = 1;
  // you actually no longer need the if statement because of the for loop
  // if (number === 2) {
  //   answer = 2;
  // }
  for (let i = 2; i <= number; i++) {
    answer = answer * i;
  }
  return answer;
}

function findFactorialRecursive(number) {
  if (number === 2) {
    return 2;
  }
  return number * findFactorialRecursive(number - 1);
}

findFactorialIterative(5);
findFactorialRecursive(5);

//If you want, try to add a base case condition for the recursive solution if the parameter given is less than 2
```

#### C8

Q: What does exponential time mean?
A: It means that every additional element in a function we get an increase in function calls exponentially
e.g. (recursive algorithms that solves a problem of size N)

Q: How can a recursive function be optimized?  
A: Dynamic programming and memoization!

Q: Given a number N return the index value of the Fibonacci sequence, where the sequence is:

```javascript
// 0, 1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89, 144 ...
// the pattern of the sequence is that each value is the sum of the 2 previous values, that means that for N=5 → 2+3

//For example: fibonacciRecursive(6) should return 8

function fibonacciIterative(n) {
  //code here;
}
fibonacciIterative(3);

function fibonacciRecursive(n) {
  //code here;
}

fibonacciRecursive(3);
```

A:-

```javascript
function fibonacciIterative(n) {
  let arr = [0, 1];
  for (let i = 2; i < n + 1; i++) {
    arr.push(arr[i - 2] + arr[i - 1]);
  }
  return arr[n];
}
fibonacciIterative(3);

function fibonacciRecursive(n) {
  if (n < 2) {
    return n;
  }
  return fibonacciRecursive(n - 1) + fibonacciRecursive(n - 2);
}

fibonacciRecursive(6);
```

#### C9

Q: What are the pros of using recursion?
A: 1.DRY (simpler, have less loops happening with confusing code)
2.Readability (generally is more readable than an iterative aproach)

Q: What are the cons of using recursion?
A: 1.Large stack (it creates an extra memory footprint, because every time we add a function to the call stacks it adds extra piece of memory)

Q: What is tail call optimization?
A: There's something called tail call optimization in many languages And for example in Javascript with 6 it allows recursions to be called without increasing the call stack  
There are certain ways to write recursion So there are more memory efficient.

#### C10

Q: When shall we use recursion?
A: When it gets to complicated problems like traversing or searching through trees or graphs (DFS & BFS) recursion is really really useful and better than iterative aproaches
When we're sorting through items there's also cases that will see that recursion is preferred
e.g. (merge sort, quick sort)

Q: What are the rules/factors to consider when deciding to write a recursive function?  
A: **Every time you are using a tree or converting Something into a tree, consider recursion.**  
1.Divided into a number of subproblems that are smaller instances of the same problem. e.g.(fibonacci / factorial problems)  
2.Each instance of the subproblem is identical in nature. (the calculations that we need to do are pretty much the same)  
3.The solutions of each subproblem can be combined to solve the problem at hand. (if you solve the smaller problems and you combine them that solves the problem at hand)  
**Divide and Conquer using Recursion**
e.g. (looking through a phone book when you're looking for Bell in the phone book You're not going to start from a and simply go one page at a time from left to right. o you usually split the phonebook in the middle or try to go to the B section of the phone book and start dividing up the problem page by page until you get closer and closer)

#### C11

Q: Implement a function that reverses a string using iteration...and then recursion!

```javascript
function reverseString(str) {}

reverseString('yoyo mastery');
//should return: 'yretsam oyoy'
```

A:-

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

### 13. Algorithms: Sorting

#### C1

Q: Why should we review the documentation of the (native) methods we are using?
A: To understand how it works in the language, it can also serve as a reference and a guide.  
For example, in the case of javascript the implementation of the sort() method will vary depending on the environment where it is executed, ECMAScript says how it should look like (grab this argument and return this), but does not talk anything about the implementation.

#### C4

Q: What are the algorithms found in the "elementary sorts" category?
A: Bubble sort, insertion sort, selection sort  
**They are, let's say, the first ones you would think of if you were told to implement some kind of order.**

Q: What is bubble sort?
A: Bubble Sort is the simplest sorting algorithm that works by repeatedly swapping the adjacent elements if they are in the wrong order. This algorithm is not suitable for large data sets as its average and worst-case time complexity is quite high.

Q: What is the time and space complexity of Bubble Sort? (worst case)  
A: Time: O(n^2)  
Space: O(1)

#### C6

Q: How would you implement bubble sort?
A:-

```javascript
const numbers = [99, 44, 6, 2, 1, 5, 63, 87, 283, 4, 0];

function bubbleSort(array) {
  const length = array.length;
  for (let i = 0; i < length; i++) {
    for (let j = 0; j < length; j++) {
      if (array[j] > array[j + 1]) {
        //Swap the numbers
        let temp = array[j];
        array[j] = array[j + 1];
        array[j + 1] = temp;
      }
    }
  }
}

bubbleSort(numbers);
console.log(numbers);
```

#### C7

Q: What is selection sort?
A: Selection sort is a simple and efficient sorting algorithm that works by repeatedly selecting the smallest (or largest) element from the unsorted portion of the list and moving it to the sorted portion of the list (usually the beginning of an array).

Q: What is the time and space complexity of Selection Sort? (worst case)  
A: Time: O(n^2)  
Space: O(1)

#### C9

Q: How would you implement selection sort?
A:-

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

#### C11

Q: What is insertion sort?
A: Insertion sort is a simple sorting algorithm that works similar to the way you sort playing cards in your hands. The array is virtually split into a sorted and an unsorted part. Values from the unsorted part are picked and placed at the correct position in the sorted part.

Q: What is the time and space complexity for Insertion Sort? (worst case)  
A: Time: O(n^2)  
Space: O(1)

#### C13

Q: How would you implement insertion sort?
A:-

```javascript
const numbers = [99, 44, 6, 2, 1, 5, 63, 87, 283, 4, 0];

function insertionSort(array) {
  const length = array.length;
  for (let i = 0; i < length; i++) {
    if (array[i] < array[0]) {
      //move number to the first position
      array.unshift(array.splice(i, 1)[0]);
    } else {
      // only sort number smaller than number on the left of it. This is the part of insertion sort that makes it fast if the array is almost sorted.
      if (array[i] < array[i - 1]) {
        //find where number should go
        for (var j = 1; j < i; j++) {
          if (array[i] >= array[j - 1] && array[i] < array[j]) {
            //move number to the right spot
            array.splice(j, 0, array.splice(i, 1)[0]);
          }
        }
      }
    }
  }
}

insertionSort(numbers);
console.log(numbers);
```

#### C14

Q: What does Log Linear time mean?
A: It means that:  
1.Has linear behavior nested in log steps  
2.Is bigger than O(n) but smaller than O(n^2)
e.g. usually sorting operations

Q: What is merge sort?
A: Merge sort is defined as a sorting algorithm that works by dividing an array into smaller subarrays, sorting each subarray, and then merging the sorted subarrays back together to form the final sorted array.

Q: What technique do the merge sort and quick sort algorithms use?
A: Divide & Conquer

Q: What is the time and space complexity of Merge Sort? (worst case)  
A: Time: O(n log n)  
Space: O(n)

Q: What does it mean when a sorting algorithm is stable?  
A: If a sorting algorithm is stable then it will retain the original order of the data after sorting is completed.  
If there are duplicates of data then the duplicate piece of data that was on the left will remain on the left and the right will remain to the right after sorting is done.

#### C16

Q: How would you implement merge sort?
A:-

```javascript
const numbers = [99, 44, 6, 2, 1, 5, 63, 87, 283, 4, 0];

function mergeSort(array) {
  if (array.length === 1) {
    return array;
  }
  // Split Array in into right and left
  const length = array.length;
  const middle = Math.floor(length / 2);
  const left = array.slice(0, middle);
  const right = array.slice(middle);
  // console.log('left:', left);
  // console.log('right:', right);

  return merge(mergeSort(left), mergeSort(right));
}

function merge(left, right) {
  const result = [];
  let leftIndex = 0;
  let rightIndex = 0;
  while (leftIndex < left.length && rightIndex < right.length) {
    if (left[leftIndex] < right[rightIndex]) {
      result.push(left[leftIndex]);
      leftIndex++;
    } else {
      result.push(right[rightIndex]);
      rightIndex++;
    }
  }
  // console.log(left, right)
  return result.concat(left.slice(leftIndex)).concat(right.slice(rightIndex));
}

const answer = mergeSort(numbers);
console.log(answer);
```

#### C18

Q: What is quick sort?
A: QuickSort is a sorting algorithm based on the Divide and Conquer algorithm that picks an element as a pivot and partitions the given array around the picked pivot by placing the pivot in its correct position in the sorted array.

Q: What is the time and space complexity of Quick Sort? (worst case)  
A: Time: O(n^2) # This can usually be avoided with a good 'pivot' point  
Space: O(log(n))

#### C19

Q: How would you implement quick sort?
A:-

```javascript
const numbers = [99, 44, 6, 2, 1, 5, 63, 87, 283, 4, 0];

function quickSort(array, left, right) {
  const len = array.length;
  let pivot;
  let partitionIndex;

  if (left < right) {
    pivot = right;
    partitionIndex = partition(array, pivot, left, right);

    //sort left and right
    quickSort(array, left, partitionIndex - 1);
    quickSort(array, partitionIndex + 1, right);
  }
  return array;
}

function partition(array, pivot, left, right) {
  let pivotValue = array[pivot];
  let partitionIndex = left;

  for (let i = left; i < right; i++) {
    if (array[i] < pivotValue) {
      swap(array, i, partitionIndex);
      partitionIndex++;
    }
  }
  swap(array, right, partitionIndex);
  return partitionIndex;
}

function swap(array, firstIndex, secondIndex) {
  var temp = array[firstIndex];
  array[firstIndex] = array[secondIndex];
  array[secondIndex] = temp;
}

//Select first and last index as 2nd and 3rd parameters
quickSort(numbers, 0, numbers.length - 1);
console.log(numbers);
```

#### C20

Q: When should you use insertion sort?
A: Insertion sort is recommended when dealing with a small number of items or when the items are already mostly sorted. It is fast in such cases. Additionally, insertion sort requires minimal space and is easy to implement in code.

Q: When should you use bubble sort and selection sort?
A: To be honest you're never going to use bubble/selection sort. It's only really used for educational purposes as a way to teach sorting. But it's very rare that you'll find this in real life because is just not very efficient.

Q: When should you use merge sort?
A: The main reason is its efficient time complexity of O(n log(n)) in both best and worst case scenarios. If one is concerned about worst case scenarios, merge sort is a suitable choice.  
However, if the goal is to sort data in memory and space complexity is a concern, merge sort can be costly because it requires O(n) space complexity. This means it uses a significant amount of memory.  
On the other hand, if there are large files that cannot be sorted within memory limits, external sorting is required. In this case, merge sort becomes a good option because space complexity matters less. External sorting involves using a process outside of the main memory to sort the data.  
In summary, merge sort is a favorable algorithm due to its efficient time complexity, making it suitable for worst case scenarios. However, if sorting in memory and space complexity is a concern, alternatives may be considered. For external sorting, such as with large files, merge sort is a good choice as space complexity becomes less significant.

Q: When should you use quick sort?
A: Quicksort is superior to merge sort in terms of average case time complexity and space complexity. It has comparable speed to merge sort, but with lower space requirements. Quicksort is considered one of the most popular sorting algorithms.  
However, a drawback of Quicksort is its worst case scenario, where if the pivot is not chosen properly, the sorting process can become significantly slower. Therefore, it is important to exercise caution when using Quicksort, particularly if worst case scenarios are a concern. In such cases, it may be advisable to choose a different sorting algorithm.

Q: When should you use heap sort?
A: Heapsort is similar to quicksort and merge sort but has a space complexity of O(1), meaning it uses a constant amount of memory. However, in terms of average performance, heapsort is generally slower than quicksort in most cases.  
Heapsort is recommended only when there is a significant concern about worst-case scenarios and memory usage. In most situations, the text suggests that quicksort or merge sort would be the preferred choices for sorting algorithms.

Q: What is the time and space complexity of Heap Sort? (worst case)  
A: Time: O(n log n)
Space: O(1)

---

TARGET DECK: Javascript::Interview::ADSA - Master the coding interview data structures algorithms - andrei neagoie

FILE TAGS: Javascript Interview

Tags:

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```
