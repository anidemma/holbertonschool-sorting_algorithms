# Sorting Algorithms Project

This project demonstrates the implementation of various sorting algorithms in C. It includes Bubble Sort, Insertion Sort, Selection Sort, and Quick Sort. Each algorithm is implemented with the goal of understanding how they work and their efficiency in sorting data.

## Project Structure

- `0-bubble_sort.c`: Implementation of the Bubble Sort algorithm.
- `1-insertion_sort_list.c`: Implementation of the Insertion Sort algorithm for doubly linked lists.
- `2-selection_sort.c`: Implementation of the Selection Sort algorithm.
- `3-quick_sort.c`: Implementation of the Quick Sort algorithm using the Lomuto partition scheme.
- `print_array.c`: Helper function to print arrays.
- `print_list.c`: Helper function to print doubly linked lists.
- `sort.h`: Header file containing function prototypes and type definitions.

## Compilation

To compile the project, use the following command:

```bash
gcc -Wall -Wextra -Werror -pedantic *.c -o sort

Usage
After compiling, you can run the program to see the sorting algorithms in action. The program will print the array or list at each step where elements are swapped.

Big O Notations
Bubble Sort:

Best: O(n)
Average: O(n^2)
Worst: O(n^2)
Insertion Sort:

Best: O(n)
Average: O(n^2)
Worst: O(n^2)
Selection Sort:

Best: O(n^2)
Average: O(n^2)
Worst: O(n^2)
Quick Sort:

Best: O(n log n)
Average: O(n log n)
Worst: O(n^2)
Description
Bubble Sort: A simple comparison-based algorithm where adjacent elements are swapped if they are in the wrong order. This process is repeated until the list is sorted.

Insertion Sort: Builds a sorted section of the array one element at a time, inserting each new element into its proper position within the sorted section.

Selection Sort: Divides the array into a sorted and unsorted region, repeatedly selecting the smallest element from the unsorted region and moving it to the end of the sorted region.

Quick Sort: Uses a pivot element to partition the array into two sub-arrays, recursively sorting the sub-arrays. The Lomuto partition scheme is used in this implementation.

This project utilizes print_array and print_list helper functions to visualize each step of the sorting process, aiding in understanding how each algorithm works.
