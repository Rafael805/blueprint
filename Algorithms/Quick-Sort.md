# Quick Sort 

**A comparison based sorting algorithm**

+ Divides entire dataset in half by selecting the average element and putting all smaller elements to the left of the average.
+ It repeats this process on the left side until it is comparing only two elements at which point the left side is sorted.
+ When the left side is finished sorting it performs the same operation on the right side.

# Must know 
+ While it has the same Big O as (or worse in some cases) many other sorting algorithms it is often faster in practice than many other sorting algorithms, such as merge sort.
+ It halves the data set by the average continuously until all the information is sorted.

# Why is Quick Sort preferred over Merge Sort for sorting Arrays? 

**Quick Sort**
Worst-case runtime: ```O(n^2)``` 
Average case runtime: ```O(n log(n))```

**Merge Sort**
Worst-case runtime: ```O(n log(n))```
Average case runtime: ```O(n log(n))```

Quicksort in particular requires little additional space and exhibits good cache locality, and this makes it faster than merge sort in many cases. In other words, Quick Sort is space constant where Merge Sort depends on the structure you're sorting.

