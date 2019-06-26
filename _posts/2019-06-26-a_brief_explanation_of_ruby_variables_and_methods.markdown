---
layout: post
title:      "A Brief Explanation of Ruby Variables and Methods"
date:       2019-06-26 17:14:44 +0000
permalink:  a_brief_explanation_of_ruby_variables_and_methods
---


**Ruby Variables**
Local Variables: Variables that are defined in a method. Local variables are not available outside of the method. Local variables begin with a lowercase letter or underscore(_).

Instance Variables: Variables which are available across methods for any particular instance or object. What this means is that instance variables change from object to object. Instance variables are preceded by the at sign (@) followed by the variable name.

Class Variables: Variables that are available across different objects. A class variable belongs to the class and is a characteristic of a class. They are preceded with 2 at signs (@@) and are followed by the variable name.

Global Variables: Class variables are not available across classes. If you want to have a single variable, which is available across classes, you need to define a global variable. Global variables are always preceded by the dollar sign ($). There are very few, if any, cases when global variables should be used.


**Ruby Methods**
Ruby methods are very similar to functions in any other programming language. Ruby methods are used to bundle one or more repeatable statement into a single unit. Method names should begin with a lowercase letter. If you begin a method name with an uppercase letter, Ruby may interpret it as a constant and parse the call incorrectly. Methods should be defined before calling them, otherwise Ruby will raise an exception for an undefined method being invoked. Methods can also accept parameters, or arguments, which are used in JavaScript, but you must remember the number of parameters when you call a method. You can set default values for the parameters, which will be used if a method is called without passing parameters. Every method in Ruby returns a value by default. This returned value will be the value of the last statement. The return statement in ruby is used to return one or more values from a Ruby method. If more than two expressions are given, the array containing these values will be the return value. If no expression is given, the return value will be nil.
