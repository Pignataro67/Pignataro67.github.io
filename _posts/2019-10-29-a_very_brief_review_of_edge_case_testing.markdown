---
layout: post
title:      "A Very Brief Review of Edge Case testing"
date:       2019-10-29 19:11:57 -0400
permalink:  a_very_brief_review_of_edge_case_testing
---


Edge case testing can be a very crucial step if you want to consider your code fully vetted. You may be asking yourself, "What are edge cases, and why are they important to test?"
Edge cases are sets of data that code will analyze that are *a-typical* to data that **typically** passes through. For example, let's say you have a method computing the sum of two numbers, if one or both of those numbers are negative, that could be an edge case. If you have another method measuring the length of a string, and a string is ‘undefined’, that is an edge case.
Edge cases are important to test. Although they may be very rare, the possibility of them executing does exist. This means there is a possibility for code to break, which you never want.
There are common edge cases you can test for. While there is no rule of thumb, here are some common edge cases to watch out for:

1. Testing a string: 
a. Empty string 
b. Excessively long string 
c. Null as an argument

2. Testing an integer: 
a. 0 
b. Negative numbers 
c. Excessively high numbers 
d. Null as an argument

The edge cases above are intuitive and obvious for two basic data types. As we know, however, methods can take more than one argument, so combining the edge cases above can exponentially elevate the number of edge cases. For example - if a method takes one integer and one string, I can test for the following edge cases:

1. Empty string and 0
2. Empty string and a negative number
3. Empty string and an excessively high number
4. Empty string and null
5. Excessively long string and a negative number
6. Excessively long string and 0
7. Excessively long string and null
8. Excessively long string and an excessively high number
9. Null argument and a negative number
10. Null argument and 0
11. Null argument and a null argument
12. Null argument and a excessively high number

By analyzing only two simple arguments, edge case testing can get very... involved. Thanks for reading my post, I hope you enjoyed it. 
