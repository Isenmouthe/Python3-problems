# Python3-problems
to be done 

# **LEVEL 1**

#01: Write a program which will find all such numbers which are divisible by 7 but are not a multiple of 5,
between 2000 and 3200 (both included). The numbers obtained should be printed in a comma-separated sequence on a single line.

<details>
  <summary>Solution</summary>
  
```python3
l=[]
for num in range (2000,3200):
    if((num%7==0) and (num%5!=0)):
        l.append(num)
print(*l, sep=',')
```
</details>


#02: Write a program which can compute the factorial of a given numbers. The results should be printed in a comma-separated sequence on a single line.

<details>
  <summary>Solution</summary>
  
```python3
def factorial(x):
    if(x==0):
        return 1
    return factorial(x-1)*x

n=int(input())
print(factorial(n))
```
</details>

#03: With a given integral number n, write a program to generate a dictionary that contains (i, i*i) such that is an integral number between 1 and n (both included). and then the program should print the dictionary.

<details>
  <summary>Solution</summary>
  
```python3
d=dict()
n=int(input())
for i in range (1,n+1):
    d[i]=i*i
print(d)
```
</details>

#4 to be solved

#05: Define a class which has at least two methods:
getString: to get a string from console input
printString: to print the string in upper case.
Also please include simple test function to test the class methods.
<details>
  <summary>Solution</summary>
  
```python3
class inout:
    def __init__(self):
        self.s=""
    
    def gestring(self):
        self.s=input()

    def prinstring(self):
        print(self.s.upper())

strobj=inout()
strobj.gestring()
strobj.prinstring()
```
</details>
