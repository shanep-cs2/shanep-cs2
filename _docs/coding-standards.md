---
title: "Class Coding Standards"
date: 2022-01-20
tags: coding standards
layout: course
---

## Overview

This document applies to all coding labs turned in during the semester. You are expected to follow these standards for all
the code that you submit. Writing code is similar to writing an essay in English, part of writing a good paper is proper
paragraph breaks and document structure. You wouldn't turn in an English 101 paper with 0 paragraph breaks, or proper
punctuation and expect to receive a 100% and the same exists for writing code. So take some time to make sure your code
**looks** nice as well as the functional requirements.

## Compiling code

Unless otherwise stated all code must compile and run on the department's computers in the [Kount Computer Lab
(CCP241)](https://cs481.boisestate.edu/ccp-tour/index.html). It doesn't matter if your code compiles on your machine, it must
compile on the computers provided in CCP241. **If your program fails to compile it will be awarded 0 points**. Absolutely no
partial credit will be given if your program does not compile.

You can access the lab computers remotely via ssh or you can go to the lab and use a workstation
directly.

## Functional Requirements

Your code must meet all the functional requirements that are listed in the specification document (located in your GitHub
repository). Functional requirements are worth 65% of the lab grade. Partial credit will be given for functional requirements
if applicable.

Your code will be graded on the command line using the provided gradle build scripts. Your instructor or TA will not use an
IDE to build your code. Below is an example of how your code will be graded using gradle and the terminal.

{% include asciinema.html cast="grading.cast"%}

## Coding Standards

These standards are not optional, failure to adhere to the standards below will result in the grade penalty specified. In
total these standards are worth 35% of the lab grade (5% each). In addition to passing all functional tests for your labs you
are expected to ensure the following criteria are met. Each criteria listed below is **pass/fail**, failing a criteria (no
matter how small) will result in a deduction.

### Criteria 1

Code must be formatted consistently. I don't enforce any particular style, however I expect your code to look consistent.
Google has a pretty good [style guide](https://google.github.io/styleguide/javaguide.html) that you can follow. Choose a
style and stick with it! [VSCode](https://code.visualstudio.com/docs/editor/codebasics#_formatting) will format your code for
you, so there really is no excuse for turning in badly formatted code.

In the example below you would receive a deduction because the method `second()` is not at the correct indentation level.

```java
public class Foo{

  public void first(){

  }

        //this is not indented correctly
        public void second(){

        }
}
```

### Criteria 2

`@Override` must be present on all methods that are overridden.

In the example below you would receive a deduction because the method `show()` in the Child class does not have the
`@Override` annotation. It doesn't matter if this code compiles and works perfectly! You **MUST** have the correct
annotations.

```java
public class Parent {
    void show(){
        System.out.println("Parent method");
    }
}
  
public class Child extends Parent {
    //Missing override!!
    void show(){
        System.out.println("Child method");
    }
}
```

### Criteria 3

The only part of the class that can be declared **public** are methods. All fields, properties, or variables must be declared
**private**.

In the example below you would receive a deduction because the field `bar` is declared public when it should be private.

```java
public class Foo{

  //This should be declared private!
  public int bar;

  public int getBar(){
    return this.bar;
  }

  public int setBar(int bar){
    this.bar = bar;
  }

}
```

### Criteria 4

[Javadoc](https://en.wikipedia.org/wiki/Javadoc) is required for all java files. Any file that is marked with **DO NOT
MODIFY** is exempt from this rule

In the example below you would receive a deduction because the method `first()` does not have a Javadoc comment.

```java
/**
 * This is the Foo class and makes lots of Foo!
 */
public class Foo{

  public void first(){

  }
}
```

### Criteria 5

Writing Unit tests is not optional! You must have at least one unit test written for every class that you author. Be aware
that most labs will require more than just one test! Every project has a small set of example tests to help guide you. The
tests are not complete and you must author your own tests.

Here are some guidelines for writing unit tests.

- Are all possible return values for methods accounted for and checked?
- Passing null objects to a method should not crash your program
- Passing invalid method values should be handled as specified

### Criteria 6

Code compiles without warnings, there are **NO** acceptable warnings. All warnings indicate a problem with your code. You
are not allowed to suppress any warnings you must fix the issue in your code.

### Criteria 7

All TODO sections in the Retrospective.md must be completed

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

## Artistic License

Your programming labs and homework have been carefully crafted to ensure certain [learning
objectives]({{site.data.semester-info.learning-objectives}}) are satisfied. Thus you are required to
solve the problem as described in the lab write up. For example, if a lab asks you to solve a
problem using recursion and you think using iteration is the "better" solution you have defeated the
purpose of the lab and you will receive 0 points for your work regardless if you got the correct
output.
