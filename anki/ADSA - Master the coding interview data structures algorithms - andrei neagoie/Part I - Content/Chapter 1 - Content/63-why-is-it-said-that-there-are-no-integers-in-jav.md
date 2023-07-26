Q: Why is it said that there are no integers in JavaScript?  
A: There is only the [Number](http://www.ecma-international.org/ecma-262/6.0/index.html#sec-ecmascript-language-types-number-type) data type in JS that represents numbers.  
**Internally it is implemented as [IEEE 754](http://www.ecma-international.org/ecma-262/6.0/index.html#sec-terms-and-definitions-number-value) double precision floating point number.**  
What it means is that - technically there is no dedicated data type that represents integer numbers.  
Practically it means that we can safely use only numbers that are safely representable by the aforementioned standard. And it includes integer values in the range: `[-9007199254740991; 9007199254740991]`. Both values are defined as constants: [`Number.MIN_SAFE_INTEGER`](http://www.ecma-international.org/ecma-262/6.0/index.html#sec-number.min_safe_integer) and [`Number.MAX_SAFE_INTEGER`](http://www.ecma-international.org/ecma-262/6.0/index.html#sec-number.max_safe_integer) correspondingly.  
[Is there or isn't there an integer type in JavaScript?](https://stackoverflow.com/questions/33773296/is-there-or-isnt-there-an-integer-type-in-javascript)
<!--ID: 1690376047131-->

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