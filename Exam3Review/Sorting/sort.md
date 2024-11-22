# Sorting Review

Sorting – Review the following sorting algorithms we covered in class 
and lab: <br>

*Each one of these has multiple iterations of a specific task (we can 
call this a subtask) in order to sort a list of values. Make sure you are 
able to explain what the subtask accomplishes given a list of values. 
For example, what does 1 iteration of selection sort achieve given a list
of values? <br>

a. bubble sort <br>

    Subtask: Compare adjacent elements and swap them if they are in wrong order
    1. In each iteration, traverse list from the start to the end of the unsorted portion.
    2. Compare each pair of adjacent elements (current and next element):
        - If the element is larger than the right element, swap them.
    3. At the end of each pass, the largest unsorted element is "bubbled" to its correct position at the end of the list.
    Purpose of Subtask: 
        - Gradually moves the largest elements to their correct position through repeated comparisons and swaps.
        
    Example: Sorting [4, 2, 7, 1] in ascending order:
        First pass: [4, 2, 7, 1] → [2, 4, 7, 1] → [2, 4, 1, 7] (7 is bubbled to the end).
        Second pass: [2, 4, 1, 7] → [2, 1, 4, 7] (4 is bubbled into its correct position).
        Third pass: [2, 1, 4, 7] → [1, 2, 4, 7] (2 is bubbled into its correct position).
        List is now sorted.

b. selection sort <br>

    Subtask: Find the smallest element in the unsorted portion of the list and move it to its correct position
    1. In each iteration:
        - Find the smallest element in the unsorted portion of the list
        - Swap it with the first element in the unsorted portion(placing it in the sorted portion)
    3. Repeat until the entire list is sorted

    Purpose of the Subtask:
     - Ensures that with each iteration, the smallest remaining element is placed in its correct position in the sorted portion

     Example: Sorting [4, 2, 7, 1]
        First iteration: Find the smallest element (1) and swap it with the first element: [1, 2, 7, 4].
        Second iteration: Find the next smallest element (2) and leave it in place: [1, 2, 7, 4].
        Third iteration: Find the next smallest element (4) and swap it with the third element: [1, 2, 4, 7].
        List is now sorted.

