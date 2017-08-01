# Hash Table 

What if you hae a list of millions of names and you need to search it thousands of times a second and you want to know if it contains any particular search string?

**Hash tables** allow extremely fast lookups of arbitrary keys, like string, complex data types, etx. It is an array that is not indexed necessarily by integers, but by hash keys. Hash tables are often used to solve the dictionary problem. A dictionary is a data structure supporting efficient insert, delete, and search operations. 

-- example
Items may be instances of a student class, the **keys** are students’ names, and the returned values are the students’ ID numbers and grades in the course. We assume that keys are unique (different items have different keys).

**Hash functions** accept a key and return an output unique only to that specific key. This is known as **hashing**, which is the concept that an input and an output have a one-to-one correspondence to map information. Hash functions return a unique address in memory for that data.

**Hash collisions** are when a hash function returns the same output for two distinct inputs. It is common for hash functions to have this problem.

# Must know
+ Store data with key value pairs 
+ Designed to optimize searching, insertion, and deletion.

This is often accommodated for by having the hash tables be very large.
Hashes are important for associative arrays and database indexing.
