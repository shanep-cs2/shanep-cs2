---
title: List ADT Part 2
tag: final project
layout: course
---

## Overview

Now that we have studied and built a linked list using nodes as the backing data structure we are
going to implement the same interface except we are going to use an array as the backing data
structure. This should help demonstrate the power of interfaces and how different implementations
can give you different performance characteristics.

When you use an array as the backing data structure you will have to resize the array if you run out
of room and then copy all the elements from the old array to the new array. As you can imagine this
could be a serious performance hit if you are doing this too often. 

## Additional Videos

- [Mason Vail - ArrayList](https://www.youtube.com/watch?v=Pb-z1fC3JBQ)