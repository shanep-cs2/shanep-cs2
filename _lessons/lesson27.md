---
title: List Part 2
tag: linked list
layout: course
---

## Overview

Now that we have studied and built a linked list using nodes as the backing data structure we are
going to implement the same interface except we are going to use an array as the backing data
structure. This should help demonstrate the power of interfaces and how different implementations
can give you different performance characteristics.

It is sometimes helpful to draw out what your data structure will look like in memory before you
start coding anything up. Having a visual model to reference can aid in both development and
testing. The diagram below shows a list with 3 elements and a backing array of size 10. When you
use an array as the backing data structure you will have to resize the array if you run out of
room and then copy all the elements from the old array to the new array. As you can imagine this
could be a serious performance hit if you are doing this too often. 