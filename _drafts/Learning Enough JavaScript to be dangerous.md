---
title: Learning Enough JavaScript to be dangerous
layout: post
description: 'Course Overview - Learning Enough JavaScript to be dangerous'
image: /assets/images/resume.jpg
nav-menu: true
---

This is a documentation I do to keep myself organized in my stydies.

Here I am going to write only things that were especially useful to me, when I was going through the tutorial and showcase completed exercises.

Find full tutorial by following this [LINK](https://www.learnenough.com/command-line-tutorial/basics).


<div class="table-wrapper">
    <table class="alt">
        <thead>
            <tr>
                <th>Tutorial</th>
                <th>Time to complete / hrs</th>
                <th>Price</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>Learn Enough Command Line to Be Dangerous</td>
                <td>3</td>
                <td>15$/month <br>
                (1 month subscription was enough for me)</td>
            </tr>
        </tbody>
    </table>
</div>

It took me X hours total within 2 days to complete this tutorial:
![time to complete](image)

-------------------------
## Chapter 1: Hello, World!

This tutorial goes beyond standard of writing "Hello, World" program in your browser.

Author assumes you have no prior experience with JavaScript and showcases the language as a general purpose language,
instead of the standard representation as "browser language" only.

That is, you learn how to execute "Hello, World" program in 4 different ways:
1. JS in a web browser - [here's my result on Git Hub Pages ](https://dmytronayda.github.io/js_tutorial/)
2. JS in a REPL. REPL is a program that reads input, evaluates it, prints out the result (if any), and then loops back
to the read step. This is basically the way to test JS usability right from your browser (e.g. using Chrome Dev Tools =>
Console).
3. JS in a file
4. and, JS in a shell script

## Chapter 2: Strings

JavaScript uses double and single quotes interchangeably for almost all practical purposes. The main exception is that
apostrophes have to be escaped out with a backslash when included inside single-quoted strings:

```js
> "It's not easy being green"
'It\'s not easy being green'
```
Same thing for literal double quotes:
```js
> "Let's write a \"hello, world\" program!"
'Let\'s write a "hello, world" program!'
```

Also, just a reminder: `\n` - is a new line special character and `\t` - is a tab special character for JS.


### 2.2 Concatenation and interpolation

* Concatenation - joining strings together
* Interpolation - putting variable content into string

[Exercises for this
section](https://www.learnenough.com/javascript-tutorial/strings#sec-exercises_concatenation_and_interpolation):
1. `var` with the same name can be changed and defining `let` with the same name would result in `SyntaxError:
Identifier 'name' has already been declared`.
2. Assign variables city and state to your current city and state of residence using interpolation.

```sh
> let city = "Salzburg";
undefined
> let state = "Austria";
undefined
> console.log(`I live in ${}, ${state}`);
console.log(`I live in ${}, ${state}`);
^

SyntaxError: Unexpected token }

> console.log(`I live in ${city}, ${state}`);
I live in Salzburg, Austria
undefined
>
```
3. Repeat the previous exercise but with the city and state separated by a tab character.

```sh
> console.log(`I live in ${city}\t ${state}`);
I live in Salzburg Austria
undefined
>
```

### 2.3 Printing

2.3.1 Exercises
Define `firstName` and `lastName` variables inside `index.html`, and output them in the browser console using
`console.log`.

Solution:

![solution](/assets/images/solution_2.3.1.png)

and proof from browser console:

![solution](/assets/images/solution_2.3.1_proof.png)


### 2.4 Properties, booleans, and control flow

Here author also introduces some formatting practices. One which was particularly interesting to me is:

<div class="box">
    <p> <strong>Limit lines to 80 characters (also called “columns”).</strong>
        This is an old constraint, one that dates back to the early days of 80-character-width terminals. Many modern
        developers routinely violate this constraint, considering it outdated, but in my experience the 80-character
        limit is a good source of discipline, and will save your neck when using command-line programs like `less` (or
        when using your code in a document with more stringent width requirements). A line that breaks 80 characters is
        a hint that you should introduce a new variable name, break an operation into multiple steps, etc., to make the
        code clearer for anyone reading it.</p>
</div>

#### 2.4.1 Combining and inverting booleans

1. If `x` is `"foo"` and `y` is `""` (the empty string), what is the value of `x && y`? Verify using the “bang bang”
notation that `x && y` is `false` in a boolean context. Hint: When applying `!!` to a compound expression, wrap the
whole thing in parentheses.

![solution](/assets/images/solution_2.4.3.png)
1. What is `x || y`? What is it in a boolean context?

![solution](/assets/images/solution_2.4.3_2.png)


### 2.5 Methods

#### 2.5.1 Exercises

1. Write the JavaScript code to test whether the string “hoNeY BaDGer” includes the string “badger” without regard to
case.

![solution](/assets/images/solution_2.5.1_1.png)
2. What does `includes(string, i)` do for any integer `i`? Hint: Counting in JavaScript starts at `0` rather than `1`.
Answer: The position within the string at which to begin searching for searchString. (defaults to 0).

![solution](/assets/images/solution_2.5.1_2.png)


### 2.6 String iteration

I knew about `for` loop for quite long by now, but I get some fun this time. I made my machine count till `1,000,000`
for time. It took around 8 seconds to do that. Check out the short video on [YouTube](https://youtu.be/RBBXK_Ppj8Q) or the image below 😀:

<!-- video -->
![counting to 1 million on Mac](/assets/images/video_poster.png)
#### 2.6.1 Exercises
1. Use `let` to define a variable `N` that’s equal to the `length` of `soliloquy`, and show that the code in Mike Vanier’s for loop actually works in JavaScript exactly as written. (In particular, you can sometimes get away with omitting `let`, though this isn’t a good practice.)
![solution](/assets/images/solution2.6.1_1.png)

2. Show that you can replace the `charAt` method in Listing 2.18 with a literal bracket notation, like this: soliloquy[i].
![solution](/assets/images/solution2.6.1_2.png)

## Chapter 3: Arrays

### 3.1 Splitting

There’s a natural way to get from strings to arrays via the split method:

```
    > "ant bat cat".split(" ");     // Split a string into a three-element array.
    [ 'ant', 'bat', 'cat' ]
```
We can even split a string into its component characters by splitting on the empty string:

```
    > "badger".split("")
    [ 'b', 'a', 'd', 'g', 'e', 'r' ]
```
#### 3.1.1 Exercises

1. Assign `a` to the result of splitting the string `“A man, a plan, a canal, Panama”` on comma-space. How many elements does the resulting array have?
2. Can you guess the method to reverse a in place? Google for the answer if necessary. 
![solution](/assets/images/solution3.1.1.png)

### 3.2 Array access
#### 3.2.1 Exercises

1. Write a `for` loop to print out the characters obtained from splitting “honey badger” on the empty string.

![solution](/assets/images/solution3.2.1.png)

2. See if you can guess the value of `undefined` in a boolean context. Use `!!` to confirm.

![solution](/assets/images/solution3.2.1_2.png)

### 3.3 Array slicing

The simplest way to slice an array is to provide only one argument, which returns all the elements in the array from that index on.

#### 3.3.1 Exercises
1. Define an array with the numbers 1 through 10. Use slicing and `length` to select the third element through the third-to-last. Accomplish the same task using a negative index.
2. Show that strings also support the `slice` method by selecting just `bat` from the string  `"ant bat cat"`. (You might have to experiment a little to get the indices just right.)

![solution](/assets/images/solution3.3.1.png)

### 3.4 More array methods

#### 3.4.4 Exercises
1. The split and join methods are almost inverse operations, but not quite. In particular, confirm using == (not ===) that a.join(" ").split(" ") in Listing 3.2 is not the same as a. Why not?

Because arr.join() converts all data types included in the array to strings. 

2. Using the array documentation, figure out how to push onto or pop off the front of an array. Hint: The names aren’t intuitive at all, so you might have to work a bit.

![solution](/assets/images/solution3.4.4.png)

### 3.5 Array Iteration 

#### 3.5.1 Exercises

1. Show that the identifier i is undefined both before and after a for loop executes. (You might have to exit and re-enter the Node console.)
   
   ![solution](/assets/images/solution3.5.1.png)
2. Define an accumulator variable total and combine it with a loop to add all the elements of Listing 3.4. You can use the code in Listing 3.5 to get started (just replace the comment with the proper code). How does the value of total compare to a.join("")?

    It appears to have the same result. 
   ![solution](/assets/images/solution3.5.1_2.png)

## Chapter 4: Other native objects

### 4.1 Math and Number
```
> 1 + 1;
2
> 2 - 3;
-1
> 2 * 3;
6
> 10/5;
2
> 2/3;
0.6666666666666666
```
Note that the final example here isn’t exact; it’s a floating point number (also called a float), which can’t be represented exactly by the computer. **But in fact JavaScript has only one numerical type, and even something like 1 or 2 is treated as floating point under the hood.** This is convenient for us as programmers, since it means we never have to make distinctions between different kinds of numbers.1

#### 4.1.1 More advanced operations

JavaScript supports more advanced mathematical operations via a global object called `Math`, which has properties and methods for things like mathematical constants, exponentiation (powers),2 roots, and trigonometric functions:

```
> Math.PI
3.141592653589793
> Math.pow(2, 3);
8
> Math.sqrt(3)
1.7320508075688772
> Math.cos(2*Math.PI)
1
```

#### 4.1.3 Exercises
1. See if you can guess the return value of String(Number('1.24e6')). Confirm using the Node REPL.

2. Like most programming languages, JavaScript lacks support for imaginary numbers, i.e., numbers that are a real multiple of the imaginary unit i (satisfying the equation i2=−1, sometimes written as i=−1−−−√). What is the JavaScript value of the square root of −1? By guessing or Googling, figure out what this value stands for. What is its boolean value?

The value is `NaN` which stands for 'Not a Number'. More documentation [here](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/NaN).  

![solution](/assets/images/solution4.1.3.png)

#### 4.3.1 Regex methods

#### 4.3.3 Exercises
1. Write a regex that matches the extended-format ZIP code consisting of five digits, a hyphen, and a four-digit extension (such as 10118-0110). Confirm that it works using String#match and caption in Figure 4.8.9

![solution](/assets/images/solution4.3.3.1.png)

2. Write a regex that splits only on newlines. Such regexes are useful for splitting a block of text into separate lines. In particular, test your regex by pasting the poem in Listing 4.2 into the console and using sonnet.split(/your regex/). What is the length of the resulting array?

![solution](/assets/images/solution4.3.3.2.png)


### 4.4 Plain objects
The word object is used in [various contexts](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Working_with_Objects) in JavaScript, usually referring to the abstract idea of a collection of data (properties) and functions (methods). As noted in Section 2.4, (almost) everything in JavaScript is an object, and we’ll see in Chapter 7 how to define objects that parallel built-in objects like String, Array, and RegExp. In this section, we’ll focus on plain objects, which are simpler to define than the more general objects we’ve encountered so far.


#### 4.4.1 Exercises
1. Show that `new Object()` also works to create a new empty object. What happens if you give the object constructor an argument equal to the output of Listing 4.3?

![solution](/assets/images/solution4.4.1.png)

#### 4.5.1

```js
const sonnet = `Let me not to the marriage of true minds
Admit impediments. Love is not love
Which alters when it alteration finds,
Or bends with the remover to remove.
O no, it is an ever-fixed mark
That looks on tempests and is never shaken;
It is the star to every wand'ring bark,
Whose worth's unknown, although his height be taken.
Love's not time's fool, though rosy lips and cheeks
Within his bending sickle's compass come:
Love alters not with his brief hours and weeks,
But bears it out even to the edge of doom.
  If this be error and upon me proved,
  I never writ, nor no man ever loved.`;


let uniques = new Map();
let words = sonnet.match(/[\w']+/g);

for (let i = 0; i < sonnet.length; i++) {
    let word = words[i]; 
    if (uniques[word]) {
        uniques[word] += 1; 
    } else {
        uniques[word] = 1; 
    }
}

console.log(uniques); 
```


## Chapter 5: Functions
1.  Using function, define a square function that returns the square of a number. Do the same with an analogous altSquare function using the fat arrow notation.

![solution](/assets/images/exercise1.png)

2. My code for the rest of the exercises in chapter 5 provided below: 

![solution](/assets/images/exercise2.png)


## Chapter 6: Functional programming 

Solution to exercise 6.1.1  

![solution](/assets/images/solution6.1.1.png)


Solution to exercise 6.2.1  

![solution](/assets/images/solution6.2.1.png)


Solution to exercise 6.3.4 

![solution](/assets/images/solution6.3.4.png)



Solution to exercise 7.1.1

![solution](/assets/images/solution7.1.1.png)


Solution to exercise 7.2.1

![solution](/assets/images/solution7.2.1.png)

Solution to exercise 7.3.1

![solution](/assets/images/solution7.3.1.png)

Solution to exercise 7.3.2

![solution](/assets/images/solution7.3.2.png)

Stopped [here](https://www.learnenough.com/javascript-tutorial/functional_programming)
------------------------
Make sure to add Num of hrs needed for the completion of the tutorial in the end.


