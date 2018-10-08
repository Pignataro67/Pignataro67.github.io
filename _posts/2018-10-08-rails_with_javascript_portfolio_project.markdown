---
layout: post
title:      "Rails with JavaScript Portfolio Project"
date:       2018-10-08 14:35:30 -0400
permalink:  rails_with_javascript_portfolio_project
---

  The Journey continues and what an experience it has been so far! There are so many ups and downs with programming and this project did not disappoint. Even after finishing the project, or thinking I did, because everything was working...  BOOM, an error. Luckily it wasn't one of those errors that makes you question everything, but it was not an easy error either. No, this one takes the better part of an hour, mostly because you can't see straight from staring at a computer screen for hours. Then you find it, and it was something you checked at least 3 times and know it was right, but it ends up being a simple spelling/misplaced punctuation mark; extra whitespace, a misplaced “space”, in this case. I watched a lot of the videos, most multiple times, to get ideas for this project. One piece of code I saw, which excited me to incorporate in my project was “remote: true”. Unfortunately, we could not use that, but it was fun finding a way to get the app running without it.
  This app was built on my Rails project Gym Finder. Gym Finder is a gym, user and review domain model. Users can sign up as an admin or non-admin user. Admin users can create, update and delete their own gym. Non-admin users have the ability to write, edit and delete their own reviews.  
  In this project, I have created a JQuery front end for Gym Finder. The JQuery front end makes AJAX requests to actions in the rails controller and then renders the response by appending the returned JSON to the dom.  AJAX is short for Asynchronous JavaScript and XML and it is a technique that is used in web applications. AJAX retrieves content from a server and displays it without having to refresh the entire page.
  I started out by changing my rails controllers to serve as an API. Changes I made were how I render the data, using Json or JavaScript Object Notation . Then I wrote some jQuery/Javascript functions that are being required in the application.js file via the gym.js declaration, which is where the functions reside, in the gym.js file. The first function I wrote was a document.ready function that is calling the bindClickHandlers() and userClickHandlers(). These functions are making the JQuery calls to the rails API, running them once, and ensuring the dom is loaded in the browser. 
  In Summation, This project has been my favorite to build so far. I look forward to continuing with the curriculum and my next project!


