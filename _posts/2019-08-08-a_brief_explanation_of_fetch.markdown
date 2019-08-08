---
layout: post
title:      "A Brief Explanation of Fetch"
date:       2019-08-08 18:02:28 +0000
permalink:  a_brief_explanation_of_fetch
---


Fun fact of the day-- the fetch method is not included in the base Node.JS library. Therefore, you can’t just fetch(api/url)in node. It’s an external library (the node-fetch library) that needs to be installed and included in your codebase. It’s actually allowing you to use the browser’s fetch ability in your node environment.

You may be wondering, "How do we use fetch?" Anyone who was worked in web development has probably seen a fetch request similar to the following:

const fetch = require('node-fetch');

fetch('https://jsonplaceholder.typicode.com/todos/1')
    .then(res => res.json()) // expecting a json response
    .then(json => {
        console.log(json.id);
        console.log(json.title);
    })
    .catch(err => {
        console.log(err);
    });

Let’s go line by line and explain what is going on.

In the first line, the fetch method calls itself: fetch('some/url/here') That is all there is to the actual fetching itself. We're telling the program to fetch data from a specific url. Everything else you see in the code block at the top of the post is handling the response you get back. That is where all the confusion begins.

Since fetch is a method call, it returns a value called a promise object. Promise objects are like boxes. They contain other data types inside of them. You can think of the .then() methods as opening those boxes to get what is inside. We are getting 2 promises here. The first contains our response and the second is inside the response which contains the json.

Next, is the second line of our block: .then(res => res.json()) The ‘.then’ method is waiting until it gets a response from the server, THEN do this next block of code with it. We are then using an arrow function that takes the response you just got, and makes it a json object.

The next line is .then(json => {some other code here}. Next, we are converting our response into json format, THEN run this block of code. 

Now we can console.log out the data.  It’s inside these functions, but not always accessible to our code outside of the fetch itself. We can save our json to a variable, but the json we want is enclosed within the fetch method and we can't access it outside of there.  However, we can save the response of the fetch call to a value. If we change our first block of code to look like the following, we can manipulate the value because we have scope access to it.

const fetch = require('node-fetch'); const response = fetch('https://jsonplaceholder.typicode.com/gyms/1') .then(res => res.json()) // expecting a json response .then(json => { console.log(json.id); console.log(json.name); }) .catch(err => { console.log(err); });

Now we can say things like let gym_name = response.body[gym] and begin extracting the data we want out of the response.

Thanks for reading my explanation on fetch-ing!
