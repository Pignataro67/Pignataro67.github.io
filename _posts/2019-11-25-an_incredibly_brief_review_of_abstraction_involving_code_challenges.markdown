---
layout: post
title:      "An Incredibly Brief Review of Abstraction involving Code Challenges"
date:       2019-11-25 18:32:24 +0000
permalink:  an_incredibly_brief_review_of_abstraction_involving_code_challenges
---


As I’ve gone on my coding journey, I’ve definitely appreciated allowing code to “do the work” for me. However, I’ve also been going back to some of the code challenges I’ve done and breaking them down into less abstract solutions to better understand the basics.
The Challenge: Given an array of strings, pluralize each string and return a new array.
The more abstract, streamline solution woud involve invoking the .map() to iterate over the given array and return a new, updated array.


``` const array = [‘dog’, ‘cat’, ‘snake’]const pluralize = (array) => { let newArray = array.map(el => el + “s”) console.log(newArray) }```


The .map() method creates a new array, saved as the variable ‘newArray’, and calls the provided function once for each string in the array (in this instance, it is appending the “s” to the string). This method does not alter the original array, but creates a new array the same length as the original array. Looking at this function in a more verbose way, using a for... loop allows the full effectiveness of .map() to be appreciated.
Given the same array as the example above, ` const array = [‘dog’, ‘cat’, ‘snake’]`, the code quicly becomes much longer. Like the above example, the original array remains untouched, and each element is added to the new array in the original order. However, the new array must be initialized as an empty array first. As each element is iterated over, it is saved into a new constant “string” to which the plural “s” is appended. This pluralized string is then pushed into the new, empty array.

```const pluralize = (array) => { const pluralArray = [] for (var i = 0; i < array.length; i++) { const string = array[i] const plural = (string + "s") pluralArray.push(plural) } console.log(pluralArray) }```

While the above example is longer and less abstract, it extrapolates the logic of the .map method and allows one to appreciate and understand the more abstract syntax.
Thanks for reading my blog, I  hope you enjoyed it.
