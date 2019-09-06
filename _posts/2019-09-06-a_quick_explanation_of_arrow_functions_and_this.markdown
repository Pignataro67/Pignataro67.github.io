---
layout: post
title:      "A Quick Explanation of Arrow Functions and *this*"
date:       2019-09-06 19:39:48 +0000
permalink:  a_quick_explanation_of_arrow_functions_and_this
---

When written in JavaScript, the arrow function implicitly returns the result of the final line of code, which can help DRY(Don't Repeat Yourself) up our functions. Something else to keep in mind, the arrow function does not bind its own ‘this’ value on instantiation; rather it "will take" ‘this’ from the context of wherever it was instantiated. In arrow functions, this is always delegated to the lexical context. This behavior makes the arrow function more... functional, for lack of a better word, when used in React than a normal function declaration or expression because of the  structure of React components. When a function is passed down the component tree, there is a danger that the function declaration or expression will redefine ‘this’ in their new context of the nested component, which can alter the behavior of the application in ways that are unpredictable and difficult to debug. Because the arrow function will always take ‘this’ from its original context, we can pass it to any of the children of the component containing the arrow function. By doing the aforementioned, we will get a response using the parent component as the reference point for ‘this’.

When passing a function to an event handler in React, for example a click event, we do not need to provide parentheses at the end of the function because we do not want to call the function. If we did this, the app would invoke the function and call it every time the page was rendered, rather than only calling it when the element was clicked. There are, however, instances when we need to pass an argument into a function, that will create the same invocation issue as an empty set of parentheses. In this situation, it is ideal to wrap the function call with an arrow function in order to make it a callback. This will then assign the arrow function to the onClick event listener without invoking it.

I hope you enjoyed my brief explanation of arrow functions.


