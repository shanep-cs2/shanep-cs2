---
title: "Class coding Standards"
date: 2022-01-20
tags: coding standards
layout: course
---

## Overview

This document applies to all coding labs turned in during the semester. You are expected to follow
these standards for all the code that you submit. 

## Coding Standards

These standards are not optional, failure to adhere to the standards below will result in the 
grade penalty specified. In addition to passing all functional tests for your labs you
are expected to ensure the following:

- (-2 points) Code must be formatted consistently. I don't enforce any particular style, I expect
  your code to look consistent. Google has a pretty good [style
    guide](https://google.github.io/styleguide/javaguide.html) that you can follow. Choose a style
    and stick with it! [VSCode](https://code.visualstudio.com/docs/editor/codebasics#_formatting)
    will format your code for you, so there really is no excuse for turning in badly formatted code.
- (-2 points) `@Override` must be present on all methods that are overridden.
- The only part of the class that can be declared **public** are methods. All fields, properties, or
  variables must be declared **private**.
- (-2 points) [Javadoc](https://en.wikipedia.org/wiki/Javadoc) is required for all java files.
  - Any file that is marked with **DO NOT MODIFY** is exempt from this rule
- (-10 points) Writing Unit tests is not optional! You must have at least one unit test written for
  every class that you author. Be aware that most labs will require more than just one test!
  - Are all possible return values for methods
  - Passing null objects to method should not crash your program
  - Passing invalid method values should be handled as specified
- (-2 points) Code compiles without warnings, there are **NO** acceptable warnings. All warnings
  indicate a problem with your code.
- (-2 points) All TODO sections in the Retrospective.md must be completed

## Compiling code

Unless otherwise stated all code must compile and run on the department's computers in the [Kount
Computer Lab (CCP241)](https://cs481.boisestate.edu/ccp-tour/index.html). It doesn't matter if your
code compiles on your machine, it must compile on the computers provided in CCP241. If you program
fails to compile it will be awarded 0 points. Absolutely no partial credit will be given if your
program does not compile. 

You can access the lab computers remotely via ssh or you can go to the lab and use a work station
directly.

## Spelling and Grammar

I generally do not care about spelling or grammar mistakes. The only exception to this rule is if
your spelling and grammar are so bad I literally can't make heads or tails of what you are trying to
say. You can install a [spell
checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker)
that works with **camelCase** code!

## DO NOT MODIFY

Do not modify files that say **DO NOT MODIFY**. If you email and ask if you can modify files that
say "DO NOT MODIFY" the answer will be no. All files that say **DO NOT MODIFY** will be reset before
grading occurs, if this causes your program to not compile your grade will be a 0.

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

## Grading example

Your code will be graded on the command line. Your instructor or TA will not use an IDE to build
your code. Below is an example of how your code will be graded using gradle and the terminal.

{% include asciinema.html cast="grading.cast"%}

## Artistic License

Your programming labs and homework have been carefully crafted to ensure certain [learning
objectives]({{site.data.semester-info.learning-objectives}}) are satisfied. Thus you are required to
solve the problem as described in the lab write up. For example, if a lab asks you to solve a
problem using recursion and you think using iteration is the "better" solution you have defeated the
purpose of the lab and you will receive 0 points for your work regardless if you got the correct
output.
