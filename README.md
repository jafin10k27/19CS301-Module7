# 19CS301-Module7

## EX: 7.1 RECURSION

### Aim: To write a Python program to find whether the given number is prime or not using recursive function

### Algorithm:
1.Define a recursive function prime(n, i=2).

2.If n <= 2, return result based on whether n == 2.

3.If n % i == 0, return "not a prime number".

4.If i * i > n, return "prime number".

5.Else, call prime(n, i + 1).

6.Take user input and call the function.

7.Display the result.

### Program:
```
## Reg no:212223020018
## Name: Mohamed Jafin S
def prime(n,i=2):
    if n<=2:
        return (f'{a} is a Prime number') if n==2 else(f'{a} is not a Prime number')
    if n%i==0:
        return (f'{a} is not a Prime number')
    if i*i>n:
        return (f'{a} is a Prime number')
    return prime(n,i+1)
a=int(input())
print(prime(a))

```
### Output:
![image](https://github.com/user-attachments/assets/25da5d96-64b4-405e-a225-a88c49b59b5f)

### Result:
Thus, the given program is implemented and executed successfully .
 

## EX: 7.2 TYPES OF RECURSIONS

### Aim: Write a Python program to find an element in a sorted list using tree recursion. If found print the position in the list otherwise print 0  (Hint: Binary search )

### Algorithm:
1.Define a recursive function binary_search(l, low, high, elem).

2.Calculate mid index.

3.If l[mid] == elem, return mid.

4.If l[mid] > elem, search in the left half.

5.Else, search in the right half.

6.If element not found, return -1.

7.Take input list, sort it, and search using binary search.

8.If result is -1, print 0; else, print position (index + 1).

### Program:
```
## Reg no:212223020018
## Name:Mohamed Jafin S
def binary_search(l, low, high, elem):
   if high >= low:
      mid = (high + low) // 2
      if l[mid] == elem:
         return mid
      elif l[mid] > elem:
         return binary_search(l, low, mid - 1, elem)
      else:
         return binary_search(l, mid + 1, high, elem)
   else:
      return -1

l = [ ]
n=int(input())
for i in range(n):
    x=int(input())
    l.append(x)
num = int(input())
l.sort()
print("The sorted list is")
print(l)
print(binary_search(l,0,len(l)-1,num)+1)
```
### Output:
![image](https://github.com/user-attachments/assets/5b25e57c-5395-4bba-84b7-5ad278c16030)

### Result:
Thus, the given program is implemented and executed successfully.
 


## EX: 7.3 TAYLOR SERIES

### Aim: To  write a python program to evaluate the series using recursion: 1+x+x^2+x^3+.....+x^n    by collecting the x and n values from the user.

### ALGORITHM:
1.Read values of x and n from user.

2.Define a recursive function fun(n, x):

3.If n == 0, return 1.

4.Else, return xⁿ + fun(n-1, x).

5.Call the function and print the result.


### Program:
```
## Reg no:212223020018
## Name:Mohamed Jafin S
x=int(input())
n=int(input())
def fun(n,x):
    if n==0:
       return 1
    else:
       return x**n + fun(n-1,x)
print(fun(n,x))
```
### Output:
![image](https://github.com/user-attachments/assets/41bc545f-276f-4247-88f5-d5460a75a886)

### Result: 
Thus, the given program is implemented and executed successfully .
 

## EX: 7.4 Solve by recursion relation

### Aim: Write a program to determine the sum of all elements in the list using recursion

### Algorithm:
1.Take input for list size and elements.

2.Define recursive function sum_list(l, length):

3.If length == 0, return l[0].

4.Else, return l[length] + sum_list(l, length - 1).

5.Call the function with length = n - 1 and print result.

### Program:
```
## Reg no:212223020018
## Name:Mohamed Jafin S
def sum_list(l,length):
    if length==0:
       return l[0]
    else:
       return l[length]+sum_list(l,length-1) 
l=[]
n=int(input())
for i in range(n):
    x=int(input())
    l.append(x)

```
### Output:
![image](https://github.com/user-attachments/assets/b874df87-2b83-4f62-ba62-ad78990c5dbe)

### Result: 
Thus, the given program is implemented and executed successfully .

 ## EX: 7.5 SEB

### Aim: To Write a Python Program to convert a decimal number to a binary number using tail recursion.

### Algorithm:
1.Define a function decimal_to_binary_tail(n, result):

2.If n == 0, return result (or "0" if empty).

3.Else, prepend n % 2 to result and call function recursively with n // 2.

4.Call the function with user input and initial result="".

5.Print the binary result.

### Program:
```
## Reg no:212223020018
## Name: Mohamed Jafin S
def decimal_binary(n):
    if n==0:
        return 0
    else:
        return (n%2)+10*decimal_binary(int(n/2))
n=int(input())
print(decimal_binary(n))

```
### Output:
![image](https://github.com/user-attachments/assets/1fb44485-5a06-472f-9069-efe1447b86a1)

### Result: 
Thus, the given program is implemented and executed successfully .
