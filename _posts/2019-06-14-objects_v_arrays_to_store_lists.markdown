---
layout: post
title:      "Objects v. Arrays to Store Lists"
date:       2019-06-14 14:49:09 +0000
permalink:  objects_v_arrays_to_store_lists
---


Developng applications, wether for fun or work, generally involve a list of items such as users, comments, posts, movies, books etc. The most common data structure to store lists in JavaScript is an array. However, I would like to discuss why that might not be the best choice when storing lists in a state management tool like React or Redux.

First, when using the CRUD operations on a single item you always need to iterate with the Read, Update or Delete operations on a single item. With Create you need to add the item to the list. When Read-ing from an array you have to find the item by filtering. With an Object you need the identifier that was used as a key. When Update-ing using an array the best way is to map and change the item you want to change. On the other hand with an object, all you have to do is set the property, or key, pointing to the updated item. Lastly, when Delete-ing an item you will filter with an array and with an object you will delete the key.

Objects are also better to use when fetching from an API. When fetching items from the backend there is a chance you can fetch the same item or list twice OR a list with duplicated AND new items. If an array was used you have to make sure to not duplicate the items, which can add more complexity. When you add the same item to an object twice, because the items are stored by a key and you can't have the same key, you will substitute the fetched item with the one already in state.  Conversely, If you do not have a unique identifier for each item or you want to keep an order without using an extra property, or key, you should not use an object.

There are times you may find it easier to use an array for a list of items. For example, when rendering a list it's easier to have an array, use map and create the element in each iteration or you could try to access the state directly and use a function, known as a selector. A selector is a function that takes a piece of state and returns the data you need. 

In conclusion, using an object will save some time and bugs. You should do yourself a favor and use an object, with key-value pairs, to store a list of items. Even as a beginner, I would recommend using an object instead of an array when storing lists in a state management tool like React or Redux. The struggle will pay off in the end.
