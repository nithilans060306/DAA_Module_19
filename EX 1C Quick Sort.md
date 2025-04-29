# EX 1C Quick Sort
## DATE: 27/02/2025
## AIM: To write a python program to implement quick sort using tha last element as pivot on the list of float values.

## Algorithm:

1. **Input Reading**  
   - Read an integer `n` (number of elements).
   - Read `n` float elements into the list `arr`.

2. **QuickSort Function**  
   - If `left < right`, choose a pivot using the `partition` function.
   - Recursively sort elements before and after the pivot.

3. **Partitioning**  
   - Select the last element as pivot (`arr[right]`).
   - Initialize pointer `i` to `left - 1`.
   - Iterate from `left` to `right - 1`:
     - If `arr[j] < pivot`, increment `i` and swap `arr[i]` with `arr[j]`.
   - After loop, swap pivot with `arr[i+1]` to place it at correct position.
   - Return new pivot index (`i + 1`).

4. **Recursive Sorting**  
   - Apply the same logic to the subarrays on left and right of the pivot.

5. **Output Result**  
   - Print the sorted float array.

## Program:
```
/*
Program to implement implement quick sort using the last element as pivot on the list of float values.
Developed by: Nithilan S
Register Number: 212223240108
*/
```python
def quickSort(arr, left, right):
    if left < right:
        pivot = partition(arr, left, right)
        quickSort(arr, left, pivot - 1)
        quickSort(arr, pivot + 1, right)

def partition(arr, left, right):
    pivot = arr[right]
    i = left - 1

    for j in range(left, right):
        if arr[j] < pivot:
            i += 1
            arr[i], arr[j] = arr[j], arr[i]

    arr[i + 1], arr[right] = arr[right], arr[i + 1]
    return i + 1

n = int(input())
arr = [float(input()) for _ in range(n)]
quickSort(arr, 0, len(arr) - 1)
print("Sorted array is:")
for i in range(len(arr)):
    print(arr[i])

```

## Output:
![image](https://github.com/user-attachments/assets/30f9e2d9-d0e1-4dde-ba39-b8e76c584054)



## Result:
The program successfully sorts the input array using the QuickSort algorithm, arranging the elements in ascending order.
