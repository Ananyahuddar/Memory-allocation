#  Dynamic Memory-allocation
# Introduction
This C program demonstrates the use of dynamic memory allocation in C using the malloc() and realloc() functions. The program allocates memory for two integer variables using malloc(), assigns values to them, and then uses realloc() to change the size of the memory block pointed to by one of the pointers.

![image](https://user-images.githubusercontent.com/125941580/234309635-75e2219a-c20d-4af7-adfa-a612e203979f.png)

# Algorithm
1.Allocate memory for two integer variables using malloc().
2.Assign a value to the first variable using the first pointer.
3.Increment the first pointer to point to the second variable.
4.Assign a value to the second variable using the first pointer.
5.Use realloc() to change the size of the memory block pointed to by the first pointer.
6.Assign a value to the newly allocated memory location using the new pointer returned by realloc().

Since C is a structured language, it has some fixed rules for programming. One of them includes changing the size of an array. An array is a collection of items stored at contiguous memory locations. 

![image](https://user-images.githubusercontent.com/125941580/230758947-f00e5080-56b0-45b5-b7bb-03c26d8cb25b.png)

As it can be seen that the length (size) of the array above made is 9. But what if there is a requirement to change this length (size). For Example, 

If there is a situation where only 5 elements are needed to be entered in this array. In this case, the remaining 4 indices are just wasting memory in this array. So there is a requirement to lessen the length (size) of the array from 9 to 5.
Take another situation. In this, there is an array of 9 elements with all 9 indices filled. But there is a need to enter 3 more elements in this array. In this case, 3 indices more are required. So the length (size) of the array needs to be changed from 9 to 12.
This procedure is referred to as Dynamic Memory Allocation in C.
Therefore, C Dynamic Memory Allocation can be defined as a procedure in which the size of a data structure (like Array) is changed during the runtime.
C provides some functions to achieve these tasks. There are 4 library functions provided by C defined under <stdlib.h> header file to facilitate dynamic memory allocation in C programming.

malloc()
calloc()
free()
realloc()
Let’s look at each of them in greater detail.

# C malloc() method
The “malloc” or “memory allocation” method in C is used to dynamically allocate a single large block of memory with the specified size. It returns a pointer of type void which can be cast into a pointer of any form. It doesn’t Initialize memory at execution time so that it has initialized each block with the default garbage value initially. 

Syntax: 

ptr = (cast-type*) malloc(byte-size)
For Example:

ptr = (int*) malloc(100 * sizeof(int));
Since the size of int is 4 bytes, this statement will allocate 400 bytes of memory. And, the pointer ptr holds the address of the first byte in the allocated memory.

![image](https://user-images.githubusercontent.com/125941580/230758996-17a4a996-8a3a-4977-a6b2-2501e4728f1a.png)


# C calloc() method
“calloc” or “contiguous allocation” method in C is used to dynamically allocate the specified number of blocks of memory of the specified type. it is very much similar to malloc() but has two different points and these are:
It initializes each block with a default value ‘0’.
It has two parameters or arguments as compare to malloc().

ptr = (cast-type*)calloc(n, element-size);
here, n is the no. of elements and element-size is the size of each element.
For Example: 

ptr = (float*) calloc(25, sizeof(float));
This statement allocates contiguous space in memory for 25 elements each with the size of the float.
 ![image](https://user-images.githubusercontent.com/125941580/230759042-e01705bd-7750-4bc0-8409-54af360f5345.png)
 
 # C realloc() method
 
 “realloc” or “re-allocation” method in C is used to dynamically change the memory allocation of a previously allocated memory. In other words, if the memory previously allocated with the help of malloc or calloc is insufficient, realloc can be used to dynamically re-allocate memory. re-allocation of memory maintains the already present value and new blocks will be initialized with the default garbage value.
 
 Syntax: 

ptr = realloc(ptr, newSize);

where ptr is reallocated with new size 'newSize'.

![image](https://user-images.githubusercontent.com/125941580/234309283-25a997fa-2b97-4a31-a998-664e9c0c3541.png)

If space is insufficient, allocation fails and returns a NULL pointer.

# Uses of Dynamic Memory Allocation

Dynamic memory allocation is useful in situations where we don't know the size of the data that needs to be stored in memory beforehand. It allows us to allocate memory for data at runtime and release it when it's no longer needed. The malloc() and realloc() functions provide a flexible way to manage memory dynamically.

# Applications

Dynamic memory allocation is used in a wide variety of applications, such as:

1.Implementing data structures like linked lists, stacks, and queues.
2.Allocating memory for variables and arrays in programs that need to handle varying amounts of data.
3.Implementing dynamic libraries and plugins that can be loaded and unloaded at runtime.


