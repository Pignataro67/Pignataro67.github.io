---
layout: post
title:      "A quick Overview of Nested Resources"
date:       2019-09-12 16:29:37 +0000
permalink:  a_quick_overview_of_nested_resources
---


Rails can be thought of as being “magical” at times, however, sometimes it can be difficult to capture that magic. Rails takes care of the "behind the scenes" code that is written for you. This can be very helpful, but can also lead to some confusion for individuals who are new to coding.Nested resources are used for when a route exists only for a specific view.  
For example, a review on a gym. The review does not exist for every gym because maybe a user has not visited all of the gyms in the database. (Additionally it probably wouldn’t make sense for a user to suggest a pilates class in their review of a gym.) In order for us to make this distinguishable to the application we are creating, we rely on nested resource routes.
To clarify, here are some code snippets of what this would look like in Ruby:GET /gyms/:gym_id/reviews <<<--- This would show all of the reviews for this specific gym based upon its given ID.POST /gyms/:gym_id/reviews <<<--- By changing the HTTP verb, we are now creating a review about that gymLet me give an example, let’s say we’re posting the review from our phone and accidentally hit "complete" before we are done writing our review.  
Our review will be given an ID which would then create a route like this: /gyms/:gym_id/reviews/:id A simple change of the http verb from “POST” to “PUT” will now create a route for us to update that review.  If we want to delete that comment all we would do is change the HTTP verb again to “DELETE”The reason these are called nested resources is because in this example, the reviews are “nested” within each gym resource.Rails "uses" convention over configuration, therefore, when you write resources :gyms rails assumes you will be using a gyms controller.  
This makes it a lot easier for the developer when it comes to configuring routes.With the aforementioned we can take it further by characterizing what we want our users to be able to access within our resources.
If a gym is created and we do not want our users to delete that gym, we could do it two ways by using :only or :except. In this case we would use the latter like this: resources :gyms, :except => [:delete]When we nest our resource within another, we write it like this: resources :gyms do resources :reviews endThis allows us to access all of the reviews through the routes listed above, as well as add new reviews.If we want to update or destroy a review the routes are reduced to only /reviews/:id because once you have the :id for the nested resources, we don’t need the first part. All we need is to specify our verb. 
In order to accomplish this and work on the idea of separating our concerns we could use :except=> [:update, :destroy].After doing that we could call a separate resources :reviews, :only => [:update, :destroy] . 

I hope you enjoyed my post on nested resources.
