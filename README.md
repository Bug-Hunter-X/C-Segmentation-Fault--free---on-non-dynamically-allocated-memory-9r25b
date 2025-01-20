# C Segmentation Fault: Incorrect Use of free()

This repository demonstrates a common C programming error: attempting to free memory that was not allocated dynamically using `malloc`, `calloc`, or `realloc`.  This leads to undefined behavior, most often a segmentation fault.

The `bug.c` file contains the erroneous code.  The `bugSolution.c` file provides a corrected version.

**Understanding the Problem**

In C, `malloc`, `calloc`, and `realloc` allocate memory from the heap.  The `free` function releases this memory back to the heap.  However, attempting to `free` memory that was not allocated with one of these functions results in undefined behavior.

**Solution**

The solution involves only freeing memory that was previously allocated using `malloc`, `calloc`, or `realloc`.