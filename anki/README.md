# ADSA - Master the coding interview data structures algorithms - andrei neagoie

## Questions

### 3. Big O

#### C2

Q: What is the official term for Big O?  
A: The official term is Big O asymptomatic analysis. It can tell us how well a problem is solved.

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
A: Constant time means that the number of steps does not depend on the input size. Also known as O(1). Predictability is always good

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
A: It means that you are adding a loop for every element  
We will find ourselves writing algorithms with factorial time complexity when calculating permutations and combinations.

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
A: 1.Analytic Skills - How can you think through problems and analyze things?  
2.Coding Skills - Do you code well, by writing clean, simple, organized, readable code?  
3.Technical knowledge - Do you know the fundamentals of the job you're applying for?  
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
A: O(1)
e.g. We traverse the entire array to check if an element is present.

Q: What is the Big O of an Array push/append operation? (aka **insertion**: Array.push(value))  
A: O(1) if the array is static  
O(n) if the array is dynamic and has to grow when the new value is added.
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
