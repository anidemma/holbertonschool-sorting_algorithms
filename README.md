```markdown
# Sorting Algorithms Project

This project demonstrates the implementation of various sorting algorithms in C, including Bubble Sort, Insertion Sort, Selection Sort, and Quick Sort.

## Project Structure

- `0-bubble_sort.c`: Implementation of Bubble Sort.
- `1-insertion_sort_list.c`: Implementation of Insertion Sort for doubly linked lists.
- `2-selection_sort.c`: Implementation of Selection Sort.
- `3-quick_sort.c`:

 Implementation of Quick Sort.
- `print_array.c`: Helper function to print arrays.
- `print_list.c`: Helper function to print doubly linked lists.
- `sort.h`: Header file containing function prototypes and type definitions.

## Compilation

To compile the project, use the following command:

```bash
gcc -Wall -Wextra -Werror -pedantic *.c -o sort
```

## Usage

Run the compiled executable and provide the array or list to be sorted.

## Big O Notations

- **Bubble Sort:**
  - Best: O(n)
  - Average: O(n^2)
  - Worst: O(n^2)

- **Insertion Sort:**
  - Best: O(n)
  - Average: O(n^2)
  - Worst: O(n^2)

- **Selection Sort:**
  - Best: O(n^2)
  - Average: O(n^2)
  - Worst: O(n^2)

- **Quick Sort:**
  - Best: O(n log n)
  - Average: O(n log n)
  - Worst: O(n^2)
```

## Explanation:

- **Bubble Sort:** We repeatedly swap adjacent elements if they are in the wrong order.
- **Insertion Sort:** We build the sorted list one element at a time by shifting larger elements.
- **Selection Sort:** We repeatedly select the smallest element and swap it to its correct position.
- **Quick Sort:** We use a pivot to partition the array and recursively sort the subarrays.

These implementations include printing steps for educational purposes, using `print_array` and `print_list` helper functions provided in your project.

### Helper Files

Here's a minimal example of how `print_array.c`, `print_list.c`, and `sort.h` might look:

**`print_array.c`**

```c
#include <stdio.h>
#include "sort.h"

/**
 * print_array - Prints an array of integers.
 * @array: The array to be printed.
 * @size: The size of the array.
 */
void print_array(const int *array, size_t size)
{
    size_t i;

    for (i = 0; i < size; i++)
    {
        if (i > 0)
            printf(", ");
        printf("%d", array[i]);
    }
    printf("\n");
}
```

**`print_list.c`**

```c
#include <stdio.h>
#include "sort.h"

/**
 * print_list - Prints a list of integers.
 * @list: The list to be printed.
 */
void print_list(const listint_t *list)
{
    while (list)
    {
        if (list->prev)
            printf(", ");
        printf("%d", list->n);
        list = list->next;
    }
    printf("\n");
}
```

**`sort.h`**

```c
#ifndef SORT_H
#define SORT_H

#include <stddef.h>

/**
 * struct listint_s - Doubly linked list node
 *
 * @n: Integer stored in the node
 * @prev: Pointer to the previous element of the list
 * @next: Pointer to the next element of the list
 */
typedef struct listint_s
{
    const int n;
    struct listint_s *prev;
    struct listint_s *next;
} listint_t;

void print_array(const int *array, size_t size);
void print_list(const listint_t *list);

void bubble_sort(int *array, size_t size);
void insertion_sort_list(listint_t **list);
void selection_sort(int *array, size_t size);
void quick_sort(int *array, size_t size);

#endif /* SORT_H */
```
