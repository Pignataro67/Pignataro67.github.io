---
layout: post
title:  "What I have not read in the curriculum"
date:   2017-09-11 17:46:35 +0000
---


  Upon reasearching on the internet, I have discovered the ".upto" and ".downto" methods, which I would like to discuss for this blog post. These methods work well with a range of numbers. If we know a range of numbers we'd like to use in a computer program, we can use ".upto" and ".downto". This is an alternative solution to using a for loop that stops when a counter variable reaches a certain value in a computer program.
  We can use ".upto" to print out a specific range of values, such as: 15.upto(20) { |num| print num, " " }. The ".upto" method can also be used on letters. An example of this would be, my_array = ["l", "m", "n", "o", "p"], "l".upto("p") { |char| puts char.upcase, " " }. The method ".downto" can also be used on letters or descending values. 
	I also read about Procs, which can be thought of as a "saved" block. Procs are great for keeping your code DRY, which stands for Don't Repeat Yourself, which I did read in the curriculum. With a block of code it must be written out each time you need it. Procs, on the other hand, can be written once and used many times.
	The last item I would like to discuss are lambdas. The following is an example of a lambda: #1 def titan_hunter_lambda #2 paul = lambda { return "Titan will win!" } #3 paul.call #4 "Hunter will win!" #5 end #6 puts titan_hunter_lambda. Procs and Lambdas are very similar. There are two differences, though. The first is a proc does not check the number of arguments passed to it while a lambda does. If the wrong number of arguments are passed to a lambda it will cause an error. With a proc, it will return "nil" for missing arguments. Secondly, a proc will return without going back to the caling method. The lambda will do the opposite, pass control back to the calling method.
	In Summation, I researched a lot on the internet and learned some new methods. The items I learned were a good complimentary to the robust curiculum on Learn.  I look forward to continuing supplementing my learning with reseaching online.
	
