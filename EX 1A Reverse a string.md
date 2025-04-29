# EX 1A Power of a Number
## DATE: 25/02/2025
## AIM: To write python Program Using Recursive Function which calculates the value of a number multiplied by itself a certain number of times.

## Algorithm:

1. **Input Reading**  
   Read two integers from the user:  
   - `n` (base)  
   - `x` (exponent)

2. **Base Case**  
   If `x == 0`, return `1`.

3. **Recursive Case**  
   Return `n * power(n, x - 1)`.

4. **Recursive Unwinding**  
   Continue until the base case is reached and start returning values.

5. **Output Result**  
   Print the result in the format:  
   `n to the power of x is result`

## Program:
```
/*
Program to implement power of a number
Developed by: Nithilan S
Register Number: 212223240108
*/
```python
def power(num, topwr):
    #Add your code here
    if topwr == 0:
        return 1
    return num * power(num, topwr - 1)

n=int(input())
x=int(input())

print('{} to the power of {} is {}'.format(n, x, power(n, x)))
```

## Output:
![image](https://github.com/user-attachments/assets/4e276a38-fb31-49f2-b27a-0305e2c1718a)



## Result:
The program successfully reverses the input string using recursion. When the user provides an input string, the output displays the reversed version of the string
