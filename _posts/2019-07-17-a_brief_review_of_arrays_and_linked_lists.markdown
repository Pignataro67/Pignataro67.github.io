---
layout: post
title:      "A Brief Review of Arrays and Linked Lists"
date:       2019-07-17 21:10:54 +0000
permalink:  a_brief_review_of_arrays_and_linked_lists
---


I recently learned of a new data structure I was unfamiliar with, a linked list. I have never worked with linked lists before, except for the lab in the Flatiron Computer Science section, and wanted to tighten up my understanding of the term.

Let’s start by discussing what a linked list is. A linked list is a linear data structure which stores elements in the non-contiguous location. The elements in a linked list are linked with each other using pointers, or nodes, where each node contains a data field and a reference(link) to the next node in the list.

This varies from an ordered list of elements, such as an array. In order to access an element of a linked list, you need to access each element that comes before it (or all of the elements that it is linked to). You could say a linked list relies on references or pointers to traverse the referential tree. In order to access an element in an array, you can simply use their integer indexes.

Turning to an example to help our understanding:

birds = [Robin, Blue Jay, Cardinal, Stellar Eagle, Vulture] If I want to access the fourth element of this array “birds”, I simply use birds[3].

linkedbirds = Head –> [Robin] –> [Blue Jay] –> [Cardinal] –> [Stellar Eagle] –> [Vulture]. If I want to access the fourth element of this linked list, I need to read through the linked list, starting with “Robin” which points to “Blue Jay” which points to “Cardinal” which points to "Stellar Eagle". In the code below, notice the “next” keyword. Each item in a linked list is equipped with a pointer, and the next keyword let’s us call on that pointed direction.

public void printAllBirds() {
    Node bird = head;
    while (bird != null) 
    {
        Console.WriteLine(bird.data);
        bird = bird.next;
    }
}

Thank you for reading my short explanation of Arrays and Linked Lists.
