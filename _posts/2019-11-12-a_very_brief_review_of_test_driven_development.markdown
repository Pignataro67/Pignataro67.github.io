---
layout: post
title:      "A Very Brief Review of Test Driven Development"
date:       2019-11-12 22:26:01 +0000
permalink:  a_very_brief_review_of_test_driven_development
---


Test Driven Development, or “TDD”, is a software development process that relies on a development cycle. This 'development cycle' is needed in order to implement new software features. The development cycle relies on 3 main phases, which are broken down below:
1) Write a test that when it passes, would accurately reflect the new software feature you are attempting to implement. When first written the test will fail because the code is not yet implemented. 2) Write the code to implement the new feature and then continue with development until the test passes. 3) As always, refactor the code once the tests are passing. 
The tests can be separated into three main categories:
1) Unit Testing which is testing a unit of code in isolation to make sure the code works. 2) Integration Testing which is building on unit tests. These tests combine units of code to ensure a larger combined functionality is working. 3)  Functional Testing which is sometimes referred to as ‘end to end’ testing. This builds off integration testing and tests the full functionality of a chunk of the system.
Pros and cons of Test Driven Development are:
Pros: When you develop with TDD you'll have a better idea of what your code should be doing. The specifications and requirements are clearly defined; the code either fails the test or passes, and it’s easy to pinpoint the failure.
Cons: The development takes time, and time is always of the essence. If you are coding at a client’s request, I would definitely make sure you and the client have the same idea on the project before you spend hours implementing a test suite.
The last thing I want to discuss is Capybara. When implementing end-to-end testing, we need a way to simulate the user interaction. Capybara is a web-based test automation software that allows you to mimic user interaction. With Capybara, we can simulate when a user “clicks” a button, “submits” a form, etc.
In summation, Test Driven Development is a great way to keep your code on track and prevent bugs. It will take time, but it’s absolutely worth the effort to ensure your code is correct. With advancements like Capybara, “TDD” has become an attainable and comprehensible way to write tests.
