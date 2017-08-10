**Stacks are LAST in, FIRST out (LIFO)**

They are used in almost all computer program to maintain return address for sub function calls. They have two primary functions - push and pop.

```stack.push``` places data onto a stack

```stack.pop``` removes the top element of a stack

It is often useful to have a peek method that allows for the object on the top to be previewed without popping.

``stack.peek`` 

Stacks can be used to implement an undo/redo tracking in a word processor. Also recording instructions to be completed in a certain order. 

-- example: JS

```js
var letters = []; // this is our stack

var word = "racecar"

var reverseWord = " ";

// put letters of word into stack 
for (var i = 0; i < word.length; i++) {
    letters.push(word[i]);
}

// pop off the stack in reverse order 
for (var i = 0; i < word.length; i++) {
    reverseWord += letters.pop();
}

if (reverseWord === word) {
    console.log(word + " is a palindrome.");
} else {
    console.log(word + " is not a palindrome.");
}
```
