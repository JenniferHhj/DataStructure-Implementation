# UcBerkeley-DataStructure
Introduction
In project 1A, we will build implementations of a “Double Ended Queue” using both lists and arrays. In project 1B, we will learn how to write our own tests for those data structures, and will use the Double Ended Queue to solve some small real world probelms.

In this part of the project you will create exactly two Java files: LinkedListDeque.java and ArrayDeque.java, with public methods listed below.

Project Tasks
1. Linked List Deque
Note: We covered everything needed in lecture to do this part in Lectures 4 and 5 (1/30 and 2/1).

Create a file called LinkedListDeque.java in your project directory.

As your first deque implementation, you’ll build the LinkedListDeque class, which will be linked list based.

Your operations are subject to the following rules:

add and remove operations must not involve any looping or recursion. A single such operation must take “constant time”, i.e. execution time should not depend on the size of the deque.
get must use iteration, not recursion.
size must take constant time.
The amount of memory that your program uses at any given time must be proportional to the number of items. For example, if you add 10,000 items to the deque, and then remove 9,999 items, the resulting size should be more like a deque with 1 item than 10,000. Do not maintain references to items that are no longer in the deque.
Implement all the methods listed above in “The Deque API” section.

In addition, you also need to implement:

public LinkedListDeque(): Creates an empty linked list deque.
public LinkedListDeque(LinkedListDeque other): Creates a deep copy of other.
Creating a deep copy means that you create an entirely new LinkedListDeque, with the exact same items as other. However, they should be different objects, i.e. if you change other, the new LinkedListDeque you created should not change as well. (Edit 2/6/2018: A walkthrough that provides a solution for this copy constructor is available at https://www.youtube.com/watch?v=JNroRiEG7U4)
public T getRecursive(int index): Same as get, but uses recursion.
You may add any private helper classes or methods in LinkedListDeque.java if you deem it necessary.

While this may sound simple, there are many design issues to consider, and you may find the implementation more challenging than you’d expect. Make sure to consult the lecture on doubly linked lists, particularly the slides on sentinel nodes: two sentinel topology, and circular sentinel topology. I prefer the circular approach. You are not allowed to use Java’s built in LinkedList data structure (or any data structure from java.util.*) in your implementation.

2. Array Deque
Note: We’ll have covered everything needed in lecture to do this part by Feb 4th (lecture 6).

Create a file called ArrayDeque.java in your project directory.

As your second deque implementation, you’ll build the ArrayDeque class. This deque must use arrays as the core data structure.

For this implementation, your operations are subject to the following rules:

add and remove must take constant time, except during resizing operations.
get and size must take constant time.
The starting size of your array should be 8.
The amount of memory that your program uses at any given time must be proportional to the number of items. For example, if you add 10,000 items to the deque, and then remove 9,999 items, you shouldn’t still be using an array of length 10,000ish. For arrays of length 16 or more, your usage factor should always be at least 25%. For smaller arrays, your usage factor can be arbitrarily low.
Implement all the methods listed above in “The Deque API” section.

In addition, you also need to implement:

public ArrayDeque(): Creates an empty array deque.
public ArrayDeque(ArrayDeque other): Creates a deep copy of other.
Creating a deep copy means that you create an entirely new ArrayDeque, with the exact same items as other. However, they should be different objects, i.e. if you change other, the new ArrayDeque you created should not change as well.
You may add any private helper classes or methods in ArrayDeque.java if you deem it necessary.

We strongly recommend that you treat your array as circular for this exercise. In other words, if your front pointer is at position zero, and you addFirst, the front pointer should loop back around to the end of the array (so the new front item in the deque will be the last item in the underlying array). This will result in far fewer headaches than non-circular approaches. See the project 1 demo slides for more details.


Applying and Testing Data Structure

Introduction
In most of your prior programming assignments, you’ve relied on some external source of truth to tell you that your code was correct.
In this project, you’ll use your one of your deques from project 1A to solve a real world problem. Along the way, you’ll also write tests of your application to convince yourself that everything works correctly.

Project Description link:https://sp19.datastructur.es/materials/proj/proj1a/proj1a
Project Test Link:https://sp19.datastructur.es/materials/proj/proj1b/proj1b
