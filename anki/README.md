# ADSA - Master the coding interview data structures algorithms - andrei neagoie

## Questions

### 2. Big O

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
