**Stacks are LAST in, FIRST out (LIFO)**

They are used in almost all computer program to maintain return address for sub function calls. 

```stack.push``` places data onto a stack

```stack.pop``` removes the top element of a stack

``stack.peek`` 

-- example: JS

```
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
