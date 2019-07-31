---
layout: post
title:      "A Brief Explanation of Big O"
date:       2019-07-31 20:30:04 +0000
permalink:  a_brief_explanation_of_big_o
---


A major topic that you don’t seem to hear much about during your time in coding bootcamp(s) seems to be more prevalent the moment you start your job search and interviewing. It is The Big O. You may be asking yourself what do you need to know about it when you’re looking for your first development job.

In a simplified technical sense Big O is a way of measuring how efficient your code is. It has become the way developers talk about size and speed of code so that possible solutions to a problem can be compared against each other in a productive manner. By using Big O developers can compare algorithm's efficiency.

It’s important to understand that when you are discussing the efficiency of an algorithm, you consider how that algorithm performs on multiple inputs. For example, if your algorithm is searching an array for a specific value, the efficiency of method X might be good for short arrays, but inefficient for larger arrays. It’s because of this variable input that Big O notation is often a discussion about the worst case scenario, usually the scenario with big datasets. Writing an algorithm to find an element in an array that has a length of 10 is great, but not practical if it's not efficient for longer arrays.

Depending on your algorithm, different operations have different time and space attributes. Assigning a value to a variable, for example, is a constant time operation. You are setting a piece of physical memory to a value. In Big O notation this is an O(1) operation. It is about as fast of an operation that a computer can perform. Now consider iterating through an array. Even if you do nothing with the values you iterate through, the number of times the computer is looking at that array is dependent on the size of the array. The size of an array is represented by n.

Let's see what happens when we add a comparison to our iteration loop. We'll make it easy and see if the value in the array is equal to another specific value, for example, if an element in the array is equal to 5. You might expect this new looping operation to be worse than just iterating over each element and doing nothing with it and that would be mostly right, as the new loop would be O(n +1), and that’s bigger than O(n), which is less efficient, but in Big O notation you are often looking at the efficiency of these operations in respect to infinity. Many developers would ignore the constant of 1 and say the two loops are equal because O(infinity) and O(infinity +1) are equivalent on a functional level.

What happens when you nest a loop inside another loop? Well we know if we iterate through a loop once, our Big O is O(n). If we add a loop inside the first loop we would get O(n^2). There are plenty of other common forms we see in programming that have O notation shortcuts, but more importantly is knowing how to piece them together. If you have two loops-- one after another you would add the n together O(n) + O(n), rather than multiply them.

I hope this has made Big O a little easier to understand.
