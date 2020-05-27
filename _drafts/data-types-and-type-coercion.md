---
layout: post
title: Primitive values, types and type conversions
description: Explaning variables, scope and a variable scope topic.
---

- [ ] primitive values, types and type conversions
  - [x] a. Start w/ different JS data types in the [book](https://launchschool.com/books/javascript/read/basics#datatypes)
  - [x] b. add some rigor with [Explicit Type Coercion](https://launchschool.com/lessons/64655364/assignments/d25ab156) from JS101
  - [x] c. then, add some more with [Implicit Type Coercion](https://launchschool.com/lessons/64655364/assignments/63b6e5e4) from JS101

- [ ] learn by heart at least the coercing methods below: 

<iframe height="500" width="1450" src="https://docs.google.com/spreadsheets/d/e/2PACX-1vQSm2bAouxjR4WHv3p3nOmSqNOiDWem_cnoS6FpM3CqdAPM2XttoF_y1l3_DqAAO9FJHbmH3IBCDlYD/pubhtml?gid=1234610985&amp;single=true&amp;widget=true&amp;headers=false"></iframe>

## Primitive values

| Data Type | Group | Example | Explanation| Details |
| ------ | --- | ----- |-------| ---------| 
| String | primitive | 'hello' |A list of characters in a specific sequence.| (\\) backslash is an escape character; backticks(`) allow template literals to enable an operation called string interpolation.|
| Number | primitive | 3, 1.14, 5.15 |All kind of numbers in JS.| |
| Undefined | primitive | ----- |A way to represent an absence of a value.| The console.log function is an example of a function that returns undefined. Check example 1 below. | 
| Null | primitive | ----- |Used to represent an intential absence of a value; often used to represent emptiness or "nothing".| Main different from `undefined` is that you need to use `null` explicitly. `undefined` can arise implicitly.|
| Boolean | primitive | true, false |-------| |
| Array | complex | [1, 'Dima', 14, 2] || 1) The order of the elements is significant. 2) Use index numbers  to retrieve elements from the array. 3) Index numbers are non-negative integers starting from `0`|
| Object | complex | {'firstName' : 'Dmytro', 'lastName' : 'Naida', 'nationality' : 'Ukraine'} |A dictionary-like data structure that matches keys with specific values| |

### Examples

#### `undefined` 
1. Function `console.log` writes a value to the console but it does not have a concrete return value. Thus, it returns `undefined`.
   
```javascript
> console.log("Hello, World!")
Hello, World!
= undefined
```

2. `undefined` also arises when declaring variables w/o an explicit value: 
   
```javascript
> let foo
= undefined 

> foo
undefined

> let bar = 3
= undefined

> bar
= 3
```

Here we declare the foo variable w/o givin it a value. That's why it returns undefined. On the other hand, we declare `bar` with an initial value of `3`. Thus, using `bar` in an expression returns `3`. 

#### The typeof Operator
To see what type a particular value has, you can use the `typeof` operator. It returns a string that contains the type of its operand's value. For example: 
```javascript
> typeof 1
= 'number'

> typeof 'foo'
= 'string'

> typeof true
= 'boolean'

> typeof undefined
= 'undefined'

> typeof null
= 'object'

```
## Type Coercion

__Type coercion__ is the conversion of one type of value into another.

## Explicit Type Coercion
Explicit type coercion happens when the programmer **intentionally** uses one of the many built-in functions and operators to coerce one type of value to another.

## Implicit Type Coercion

__Implicit__ type coercion happens when you perform an operation involving values of two diffeerent types and JavaScript coerces one of them to match the other.

### Implicit Coercion with `==` Operator
1. When a number is compared with a string using ==, the string is coerced into a number.
2. When a boolean is compared with any other value, it is coerced into a number and compared again using the == operator.
3. When an object is compared with a primitive value, the object is coerced into a primitive value and compared again using the == operator.
4. A == comparison of undefined with null evaluates to true.

























