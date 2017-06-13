# What is Python?

Python is a high-level, dynamically typed multiparadigm programming language. Python code is often said to be almost like pseudocode, since it allows you to express very powerful ideas in very few lines of code while being very readable

### Python versions
There are two different supported versions of Python, Python 2.7 and 3.6. Code written for 2.7 may not work under 3.5 and vice versa.

You can check your Python version at the command line by running ```python --version```

Python includes several built-in container types: lists, dictionaries, sets, and tuples.

**Lists**: Python equivalent of an array, but is resizeable and can contain elements of different types:
**Dictionaries**: stores (key, value) pairs, similar to a Map in Java or an object in Javascript. 
**Sets**: unordered collection of distinct elements.
**Tuples**: an (immutable) ordered list of values. A tuple is in many ways similar to a list; one of the most important differences is that tuples can be used as keys in dictionaries and as elements of sets, while lists cannot.

# What is numpy?

Numpy is the core library for scientific computing in Python. Numpy allows us to process large amount of numerical data. It provides a high-performance multidimensional array object, and tools for working with arrays. 
c
**Numpy Array**: *grid of values, all of the same type, and is indexed by a tuple of nonnegative integers.*

Numpy provides many built-in functions for many basic tasks you'll perform while doing statistical analysis. Examples include calcualting the mean, median, and standard deviation of an array.

--example: find the average of a simple array of numbers. 
```
>>> numbers = [1,2,3,4,5]
>>> numpy.mean(numbers)
3.0
```
Similarly you can find the median using 
```
>>> numpy.median(numbers)
3.0
```
And to find the standard deviation
```
>>> numpy.std(numbers)
1.4143235623730961
```

Numpy Library Documentation: https://docs.scipy.org/doc/numpy-dev/user/quickstart.html

# What is panda?

Panda series and dataframes allow us to store large datasets and extract information from them. It aims to be the fundamental high-level building block for doing practical, real world data analysis in Python.

Pandas Library Documentation: http://pandas.pydata.org/pandas-docs/version/0.17.0/

# What is Matplotlib?

Matplotlib is a plotting library. The most important function in matplotlib is ```plot```, which allows you to plot 2D data
