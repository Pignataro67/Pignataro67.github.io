---
layout: post
title:      "A Brief Review of the MVC Design Pattern"
date:       2019-08-22 17:07:23 +0000
permalink:  a_brief_review_of_the_mvc_design_pattern
---


Many of my projects follow a design pattern known as MVC, or Model-View-Controller. I know it's an important topic, a topic that can come up in interviews, so I decided to write a post about it to better my understanding.

The idea behind using a MVC pattern is to seperate an application's concerns. Each component, for lack of a better word, Model, View and Controller, has a different purpose and the code is organized into three parts to separate the different functions.

Model - In my rails with a JS frontend app, for example, the model is a Ruby class. It inherits methods from ActiveRecord::Base that work with the database. The model contains methods and most of the logic related to the class that can be used throughout the application. Best practice is to keep the logic in your model. This can be thought of as the chef in a restaurant.

Controller - The controller, or the waiter in a restaurant, connects the models and views, similar to how the waiter would bring food to the table. Methods are defined that take the user’s input and decides what to do with it, the way a waiter would communicate meal requests.

Views - The views are what the user interacts with, or the customer having a meal at a restaurant. They should never contain logic and should only render what is received from the database or chef.

Putting everything together, a user will click a button on your app, such as “delete”. The request is sent to the controller, processes it and requests the information from the Model. The model then sends it back to the controller, and from there the information is sent to the view, in/on the user’s browser and the process begins again.

Thank you for reading my post, I hope it helped explain the MVC pattern.
