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
A: -
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
<!--ID: 1693659891906-->

---

DECK INFO

TARGET DECK: Javascript::Interview::ADSA - Master the coding interview data structures algorithms - andrei neagoie::Part I - Content::Chapter 1 - Content

FILE TAGS: #Javascript #Interview

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```


QUESTION STATUS: Safe to store