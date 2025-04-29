# EX 1B Merge Sort
## DATE: 25/02/2025
## AIM: To write a python program to sort the first half of the list using merge sort.

## Algorithm:

1. **Input Reading**  
   - Read an integer `n` (number of elements).
   - Read `n` float elements into the list `arr`.

2. **Divide Step**  
   - In the `mergesort(arr, low, high)` function:
     - If `low < high`, compute the middle index `mid = (low + high) // 2`.
     - Recursively call `mergesort(arr, mid + 1, high)` to sort the right half.
     - Then call `merge(arr, low, mid, high)` to merge both halves.

3. **Merge Step**  
   - Use two pointers `left = low` and `right = mid + 1`.
   - Compare and copy the smaller element from `arr[left]` or `arr[right]` into a temporary list `temp`.
   - After either half is exhausted, copy the remaining elements.
   - Replace `arr[low]` to `arr[high]` with sorted `temp`.

4. **Repeat Recursively**  
   - Continue dividing and merging until each sub-array has one element.

5. **Output Result**  
   - Print the original array and the final sorted array.


## Program:
```
/*
Program to implement Merge Sort
Developed by: Nithilan S
Register Number: 212223240108
*/
```python
def merge(arr,low,mid,high):
    temp = []
    left = low 
    right = mid+1
    while (left<=mid and right<=high):
        if (arr[left] <=arr[right]):
            temp.append(arr[left])
            left +=1
        else:
            temp.append(arr[right])
            right +=1
    while (left<=mid):
        temp.append(arr[left])
        left +=1
    while (right<=high):
        temp.append(arr[right])
        right +=1
    
    for i in range (low ,high+1):
        arr[i] = temp[i-low]
    

def mergesort(arr,low,high):
    if (low<high):
        mid = (low+high)//2
        mergesort(arr,mid+1,high)
        merge(arr,low,mid,high)
    else :
        return 
n=int(input())
arr=[float(input()) for _ in range(n)]
print("Given array is")
for i in range(n):
    print(arr[i],end=' ')
print("\n")
mergesort(arr,0,n-1)

print("Sorted array is")
for i in range(n):
    print(arr[i],end=' ')
print()

```

## Output:
![image](https://github.com/user-attachments/assets/67b8d064-67e5-4d59-a415-31bb74d2cd10)



## Result:
The program successfully sorts the first half of the given array using merge sort. where only the first half is sorted, and the second half remains unchanged.
