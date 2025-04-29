# EX 1D Linear search
## DATE: 27/02/2025
## AIM: To write a python program for a search function with parameter list name and the value to be searched using string values.



## Algorithm:

1. **Input Reading**  
   - Read an integer `n` (number of elements).
   - Read `n` values into a list `arr` and sort it.

2. **Binary Search Logic**  
   - Initialize two pointers: `low = 0`, `high = n - 1`.
   - While `low <= high`:
     - Compute `mid = (low + high) // 2`.
     - If `arr[mid] == val`, print the index and return.
     - If `arr[mid] < val`, search the right half (`low = mid + 1`).
     - Else, search the left half (`high = mid - 1`).

3. **Not Found Case**  
   - If no match is found after the loop ends, print "Element is not present in array".
 

## Program:
```
/*
Program to implement a search function with parameter list name and the value to be searched using string values.
Developed by: Nithilan S
Register Number: 212223240108
*/
```python
def binarySearchAppr(arr, low, high, val):
    while low <= high:
        mid = (low + high) // 2
        if arr[mid] == val:
            print("Element is present at index", mid)
            return
        
        elif arr[mid] < val:
            low = mid + 1
            
        else:
            high = mid - 1
            
    print("Element is not present in array")

arr = sorted([input() for _ in range(int(input()))])
x = input()
```

## Output:
![image](https://github.com/user-attachments/assets/9769acad-8946-4af5-ba27-0b1a01fe2249)



## Result:
The program was executed successfully, and it correctly checks if the input element is present in the list, printing "Found" if the element exists or "Not Found" if it does not.
