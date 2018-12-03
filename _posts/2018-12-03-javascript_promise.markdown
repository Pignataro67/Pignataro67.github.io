---
layout: post
title:      "JavaScript Promise"
date:       2018-12-03 09:16:45 -0500
permalink:  javascript_promise
---

  JavaScript promises can be somewhat difficult to understand.  Keeping it simple, a promise can only fail or succeed once. It can't fail or succeed twice, nor can it switch from a failure to a success or a success to a failure. Also, if a promise has failed or succeeded and a failure/success callback is added later, the correct callback will be called, even though the event took place earlier.  
	
	Generally you're more interested in reacting to an event/outcome and less interested in the precise time something can be available. This concept is extremely useful for asynchronous failures and successes.
	
	  A Javascript promise can have four results: fulfilled, rejected, pending, and settled. A fulfilled promise is when the action relating to the promise succeeds. A rejected promise is when the action relating to the promise fails. A pending promise is when the action does not fulfill or reject. A settled promise is when the action fulfills or rejects.
   
	
   
	 A promise takes one argument, a callback with two parameters, resolve and reject. It will do something within the callback, maybe something asynchronous, and resolve will be called if everything works. If reject is called it is commonplace to reject with an error object because they capture a stack trace, which make the debugging tools more useful. You can also use .then with a promise. You can give then() two arguments, a callback for a success case and a callback for a failure case. They, then(), can also be chained together to run additional asynchronous actions or transform values. If you return something like a promise, the next then() will wait, and is only called when that promise settles either in success or failure. An example is below:
   

	 
	 
var promise = new Promise(function(resolve, reject) {
  resolve(2);
});

promise.then(function(val) {
  console.log(val); // 2
  return val + 2;
}).then(function(val) {
  console.log(val); // 4
})
	
Rejections occur when a promise is explicitly rejected, but can also happen implicitly if an error is thrown in the constructor callback. A good rule of thumb is to do all your promise-related work inside the promise constructor callback, this way errors are caught and rejected.

Lastly, I would like to discuss Promise.resolve(). Promise.resolve() will create a promise that resolves to any value it is given. If you pass it an instance of Promise, it will be returned. If you pass it something promise-like, for example, with a then(), it creates a Promise that will fulfill or reject the same way.
