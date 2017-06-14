# What is Numpy (Numerical Python) ?

Numpy is the core library for scientific computing in Python. It is a library that provides functions that are especially useful when you have to work with large arrays and matrices of numeric data, like doing matrix matrix multiplications. Numpy allows us to process large amount of numerical data. The array object class is the foundation of Numpy, and Numpy arrays are like lists in Python, except that every thing inside an array must be of the same type, like int or float.

Numpy Array: grid of values, all of the same type, and is indexed by a tuple of nonnegative integers.

Numpy provides many built-in functions for many basic tasks you'll perform while doing statistical analysis. Examples include calcualting the mean, median, and standard deviation of an array.

Import the numpy library using ```import numpy as np```

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

These are just a few of the functions that make it easier to analyze data when using Numpy

Numpy Library Documentation: https://docs.scipy.org/doc/numpy-dev/user/quickstart.html
