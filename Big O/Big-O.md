# Big O Notation 

BIg O Notation describes the fundamental scaling nature of an algorithm.

Note: Complexities are in order from worst to best. 

# O(N!)
Time to complete is the factorial of the input set. An example of this is the traveling salesman problem brute-force solution.

# O(2^n) - Exponential complexity

Given an input of size n, the number of steps it takes to accomplish a task is a constant to the n power (pretty large number). Does not scale. You have no hope of solving any non-trivially sized problem. Useful for knowing what to avoid, and for experts to find approximate algorithms which are in O(nk).

# O(N Log N) 
Time to complete increases by the number of items times the result of Log2(N). An example of this is heap sort and quick sort.

# O(n^2) - Quadratic complexity 
Given an input of size n, the number of steps it takes to accomplish a task is square of n. Nested for loops are quadratic time, because you’re running a linear operation within another linear operation (or n * n = n^2).

1 item: 1 second
10 items: 100 seconds
100 items: 10000 seconds

The number of items increases by a factor of 10, but the time increases by a factor of 102. Basically, n=10 and so O(n2) gives us the scaling factor n2 which is 102.

# O(n) - Linear complexity 

Given an input of size n, the number of of steps required is directly related (1 to 1) 

1 item: 1 second
10 items: 10 seconds
100 items: 100 second

The number of items increases by a factor of 10, and so does the time. n=10 and so O(n)'s scaling factor is 10.

# O(log n) - Logarithmic Complexity 

Given an input of size n, the number of steps it takes to accomplish the task are decreased by some factor with each step.  

1 item: 1 second
10 items: 2 seconds
100 items: 3 seconds
1000 items: 4 seconds
10000 items: 5 seconds

The number of computations is only increased by a log of the input value. So in this case, assuming each computation takes 1 second, the log of the input ```n``` is the time required, hence ```log n```.

# O(1) - Constant complexity 

Given an input of size n, it only takes a single step for the algorithm to accomplish the task.  

1 item: 1 second
10 items: 1 second
100 items: 1 second

The number of items is still increasing by a factor of 10, but the scaling factor of O(1) is always 1.
