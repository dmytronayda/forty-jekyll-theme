---
layout: post
title: Functions
description: Explaning how passing an argument into a function may or may not permanently change the object
---

## Understand the function terminology

Image comes from my Google Drawing [here](https://docs.google.com/drawings/d/1jNT5QHoScWI7AHfDCqGx50cs-ufsXr-C_xWWT-c6fQs/edit?usp=sharing).

![octopus](/assets/images/parameter-vs-argument-distinction.png)
![](@attachment/Clipboard_2020-04-16-07-36-08.png)

## Return values

All JS function calls evaluate to a value. Default value is ``undefined``. But, when we use the ``return`` statement, we can return a specific value from a function.

<div class="row">
  <div class="6u 12u$(small)">
    <h3>Returns default `undefined` value</h3>
      <pre><code>
function sum(a, b) {
  a + b;
}

console.log(sum(3,4)); // prints undefined
      </code></pre>
  </div>
  <div class="6u$ 12u$(small)">
    <h3>Returns specific value</h3>
      <pre><code>
function sum(a, b) {
  return a + b;
}

console.log(sum(3,4)); // prints 7
      </code></pre>
  </div>  
</div>

