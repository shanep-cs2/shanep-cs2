---
title: List ADT Part 1
tag: final project
layout: course
---

## Overview

Now that we have studied how to use built in data structures and algorithms it is time to write our
own! We are going to construct a doubly linked list that uses a sentinel node. 

It is sometimes helpful to draw out what your data structure will look like in memory before you
start coding anything up. Having a visual model to reference can aid in both development and
testing. The diagram below shows a list with 3 elements and a sentinel node. You can see that the
next pointer in node **n3** points back to the sentinel node and the prev pointer of **n1** points
back to the sentinel node. Each node has a data pointer that will hold a reference to the data that
is being stored in the list. There are many ways to implement a linked list. Two common ways are to
use a null terminated list or to use a sentinel node. A sentinel node allows us to write slightly
simpler algorithms when manipulating the list.

## Memory Layout

![Linked list visualization]({{site.url}}{% link /assets/images/list-sentinel.png %})
