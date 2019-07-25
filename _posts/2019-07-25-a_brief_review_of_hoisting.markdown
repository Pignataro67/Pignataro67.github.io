---
layout: post
title:      "A Brief Review of Hoisting"
date:       2019-07-25 18:12:44 +0000
permalink:  a_brief_review_of_hoisting
---

One of JavaScript's many quirks is something known as hoisting.
If you're new to coding in JavaScript, it’s likely you’re not writing your code perfectly just yet. Because of this, it’s highly likely that your hoisting isn’t perfect either.

When JavaScript is compiled, all variable declarations using the keyword 'var' are hoisted/lifted to the top of their functional/local scope (if declared inside a function) or to the top of their global scope (if declared outside of a function) regardless of where the actual declaration has been made. This is what is meant by “hoisting”.
Functions declarations are also hoisted, but these go to the very top and will sit above all of the variable declarations.
The following is a basic example of code to demonstrate the impact of hoisting.
If we were to write the following in our global scope:

console.log(myName);
var myName = ‘Pat’;

The console.log will output "undefined".

As we mentioned earlier, variables get moved to the top of their scope when your JavaScript compiles at run-time or when your web-page loads. However, an important thing to note is that the only thing that gets moved to the top is the variable declarations, not the value given to the variable.
Just to clarify, if we had a chunk of code and on line 10 we had var myName = 'Pat', when the JavaScript is compiled, var myName would get moved to the top of its scope, while myName = 'Pat' would stay on Line 10, maybe  Line 11 if var myName were hoisted up onto Line 1.
Again, looking at the same block of code, we see how the JavaScript compiler will output the code at run-time:
var myName;
console.log(myName);
myName = ‘Pat’;
This is why the console.log is able to output ‘undefined’, because it recognizes that the variable myName exists, but myName hasn’t been given a value until the third line.

We have named our variable myName instead of just name as the ‘window’ object in the browser already has a name property. If we were to test this in a browser, any variables created in the global scope actually end up being part of the ‘window’ object. Therefore, creating var name = 'Pat'; is the same as doing window.name = 'Pat'; and therefore, creating var name = ‘Pat'; can also be referenced by typing window.name.
Functions are also hoisted to the top, above where the variable declarations are hoisted.
If we look at the following example:
function hello() {
console.log('hello ' + myName);
};
hello();
var myName = 'Pat';
The hello() function call will return undefined because the JavaScript interpreter will compile to the following at run time:
function hello() {
console.log('hello ' + myName);
};
var myName;
hello();
myName = 'Pat';
When the function gets called, it knows that there is a variable called myName, but the variable has not been given a value.

The concept of hoisting is the reason why when you see other people’s code where variables are declared at the top, and then they are given values later. The idea here is to make their code closely resemble how the interpreter will compile it in order to help them limit errors.
But what about Let and Const?
They’re also hoisted — in fact, var, let, const, function and class declarations are hoisted.
The difference between var, let and const declarations is their initialization.
Instances of var and let can be initialized without a value, and if you try to call it, it will return undefined. On the flipside const will throw a reference error if you try to declare a variable without assigning it a value at the same time. So const myName = 'Pat' would work, but const myName; myName = 'Pat; would not.
So is there any difference between var, let and const in terms of hoisting?
Yes, if you create a var at the top, globally, it would create a property on the global object — in the case of the browser, this is likely to be the window object. So creating var myName = 'Pat'; can also be referenced by calling window.myName.
However, if you wrote let newName = 'patioFurniture'; this would not be accessible in the global window object.
Declarations made with var can be accessed from outside of their initial scope, whereas declarations made with let and const are not.
Declarations made with var return undefined where as those made with let or const return errors.
I hope this improved your understanding of hoisting.
