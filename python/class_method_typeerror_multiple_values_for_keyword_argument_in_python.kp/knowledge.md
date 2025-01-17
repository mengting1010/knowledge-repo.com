---
title: The typeerror "got multiple values for keyword argument" is caused by a class method
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-16 00:00:00
updated_at: 2023-03-16 00:00:00
tldr: This error occurs when invoking a class method with both explicit and implicit arguments.
---

**Contents**

[TOC]

Section One: Introduction
In Python, it is common to use class methods to define methods that operate on the class as a whole, rather than on a specific instance of the class. However, there are certain scenarios where running a class method generates a TypeError.

Section Two: Multiple Values for Keyword Argument
One possible cause of the TypeError generated by a class method is when multiple values are provided for a keyword argument. This can happen if the class method is defined to take a specific number of arguments, and the caller provides too many arguments or provides them in the wrong order.

Section Three: Example of Multiple Values for Keyword Argument
For example, consider a class method defined as follows:

class MyClass:
    @classmethod
    def my_method(cls, arg1, arg2):
        print(arg1, arg2)

If we try to call this class method with three arguments instead of two, we will get a TypeError:

MyClass.my_method('hello', 'world', 'extra')

This will output the following error message:

TypeError: my_method() got multiple values for keyword argument 'arg2'

Section Four: Fixing the Error
To fix this TypeError, we need to make sure that we are calling the class method with the correct number of arguments, and that we are providing them in the correct order. We should also check the definition of the class method to make sure it is expecting the correct number of arguments.
