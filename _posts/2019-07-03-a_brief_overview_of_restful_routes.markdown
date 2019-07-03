---
layout: post
title:      "A brief overview of RESTful Routes"
date:       2019-07-03 22:03:00 +0000
permalink:  a_brief_overview_of_restful_routes
---


I was first introduced to the term ‘RESTful routes’ when learning about building web applications. The term RESTful did not click at first so I decided to do some research. The ‘REST’ in restful stands for representational state transfer which describes the relationship between a client and a server.

A state transition occurs when you move from one page to another on a website as you click a link. You move it from the state you are in to the next state in the web app. Restful routes are used as a design pattern to follow when mapping between HTTP verbs, for example, get, post, put, delete, & patch, to your controller's CRUD actions- create, read, update, & delete, for these state transitions.

This mapping allows for both the HTTP verb and the URL together to pinpoint which web page to transition to, instead of just the URL. This arrangement allows the same URL, when used with another verb, to render a totally different page. 

The mapping between HTTP verbs and the CRUD actions of the controller are explained using roughly 7 route patterns. Many of these actions are implemented on the same resource. When you go to a website, the web application receives an HTTP request from your browser. The web app then examines the request and takes a look at the verb and URL. After that it identifies the matching controller action that has the same method and URL. Once this pattern is matched the web app executes any code in the controller and sends back the appropriate response.

Lets break down the possible patterns if we were building a website to share books:

1. HTTP verb: GET, ROUTE: ‘/books’, Action: index, Used for: An index page to display all books.
2. HTTP verb: GET, ROUTE: ‘/books/new’, Action: new action, Used for: Displaying a create book form.
3. HTTP verb: POST, ROUTE: ‘/books’, Action: create action, Used for: Creating one book.
4. HTTP verb: GET, ROUTE: ‘/books/:id’, Action: show, Used for: Displaying one book based on an id in a URL.
5. HTTP verb: GET, ROUTE: ‘/books/:id/edit’, Action: edit, Used for: Displaying an edit form based on an id in a URL.
6. HTTP verb: PATCH, ROUTE: ‘/books/:id’, Action: update, Used for: Modifying an existing book based on an id in a URL.
7. HTTP verb: PUT, ROUTE: ‘/books/:id/’, Action: update, Used for: Replacing an existing book based on an id in a URL.
Note: Using Patch or Put depends on architecture preference - either way, they provide a similar result. Patch uses the existing book and makes changes. Put will wipe out the old book and replace it with the updated material.
