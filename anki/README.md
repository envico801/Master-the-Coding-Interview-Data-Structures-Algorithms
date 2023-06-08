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

#### C15

Q: What does the rule of "different terms for inputs" mean?
A: It means that different notations/variables are used for different inputs, because since we do not know the length of each one, we cannot assume that they are the same.  
1.**O(n) is different from O(a + b)**  
2.**O(n^2) is different from O(a \* b)**

#### C16

Q: What does the rule of "drop non dominants" mean?
A: It means that we prioritize the term that has more weight (scale) at the moment of calculating the big O.  
1.**O(n^2+3n+100+n/2) is equal to O(n^2)**

### C19

Q: What are data structures?
A: They are a way of storing data

Q: What are algorithms?
A: They are functions or ways of using our data structures to write our programs (instructions for our computer).

### C21

Q: What are the 3 pillars of good coding?
A: 1.Readable: (clean code) that can be maintained and others can read.
2.Speed: (time complexity) that has a Big O that is efficient, scales well.
3.Memory: (space complexity)

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
