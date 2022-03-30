---
title: "Class coding Standards"
date: 2022-01-20
tags: coding standards
layout: course
---

## Overview

This document applies to all coding labs turned in during the semester. You are expected to follow
these standards in for all the code that you submit.  You should imagine that you are trying to get
a job and the code that you submit will determine if you get offered the job or not!

## Coding Standards

These standards are not optional. Failure to follow these standards will impact your final grade.

- Code must be is formatted consistently. I don't enforce any particular style, I expect your code
  to look consistent. Google has a pretty good [style
    guide](https://google.github.io/styleguide/javaguide.html) that you can follow. Choose a style
    and stick with it! 
- `@Override` is present on all methods that are overridden.
- The only part of the class that can be declared **public** are methods. All fields, properties, or
  variables must be declared **private**.
- [Javadoc](https://en.wikipedia.org/wiki/Javadoc) is require for all files java files.
  - Any file that is marked with **DO NOT MODIFY** is exempt from this rule
- Writing Unit tests is not optional! You must have appropriate unit tests are written for every
  class that you author.
  - Are all possible return values for methods
  - Passing null objects to method should not crash your program
  - Passing invalid method values should be handled as specified
- Code compiles without warnings, there are **NO** acceptable warnings. All warnings indicate a
  problem with your code.


## Notes

- All TODO sections in the Retrospective.md must be completed
- If you program fails to compile it will be awarded 0 points. Absolutely no partial credit will be
  given if your program does not compile.
- Your code will be graded on the command line. Your instructor or TA will not use an IDE to build
  your code.
- Do not modify files that say **DO NOT MODIFY**. If you do you will be awarded 0 points!

```java
/**
* DO NOT MODIFY
*/
interface Foo {
  /**
   * Does some bar
   */
  public void bar();
}
```
