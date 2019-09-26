---
layout: post
title:      "A Brief Review of Iteration and Looping"
date:       2019-09-26 17:40:39 +0000
permalink:  a_brief_review_of_iteration_and_looping
---


You may be asking yourself what is the difference between iteration and looping and are there advantages to using one over the other.At first look it's easy to see that loops and iterators are used to repeat a chunk of code. One difference with iteration is that it lets you abstract away certain details of code. For example:

 loop             v.         iterator
 
 i = 0                         10.times do 
 while i < 7                puts "hello" 
   i += 1
   puts "hello"  
 end                          end
  
Both blocks of code do the same thing, but as you can see in this example the iteration is easier to write, read and understand, which makes it much "cleaner". Using a looping function there is always the possibility of an infinite loop if you fail to ensure that the termination condition is met. For example, trying to count from a number, that is inputted by a user, to 50 in steps of 5, may look like this:

number = gets.chomp.to_i 
while number != 50 
  puts number += 5
end

With a while loop you must remember to always make sure you are updating the condition on each loop so that the loop eventually ceases!  Additionally, if you accidentally left iteration out of a while loop it could result in a condition that always evaluated to true, which would cause an infinite loop.  An infinite loop would be impossible if we use just an iterator instead:

(number..50).step(5).each {|n| puts n}

Looping can be risky when creating Apps, programs, etc. When I create any piece of code that needs a looping block I may start with a loop, but when I review my code I will more than likely refactor the block of code to an iterator.

Thank you for reading my post, I hope you enjoyed it.
