# Python3-problems
https://github.com/zhiwehu/Python-programming-exercises/blob/master/100%2B%20Python%20challenging%20programming%20exercises.txt
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

# **LEVEL 2**
#06: Write a program that calculates and prints the value according to the given formula:
Q = Square root of [(2 * C * D)/H]
Following are the fixed values of C and H:
C is 50. H is 30.
D is the variable whose values should be input to your program in a comma-separated sequence.
Example
Let us assume the following comma separated input sequence is given to the program:
100,150,180
The output of the program should be:
18,22,24
<details>
  <summary>Solution</summary>
  
```python3
import math
c=50
h=30
value=[]
items=[x for x in input().split(',')]
for d in items:
    value.append(str(int(round(math.sqrt(2*c*float(d)/h)))))
print(','.join(value))
```
</details>

#08: Write a program that accepts a comma separated sequence of words as input and prints the words in a comma-separated sequence after sorting them alphabetically.
Suppose the following input is supplied to the program:
without,hello,bag,world
Then, the output should be:
bag,hello,without,world
<details>
  <summary>Solution</summary>
  
```python3
items=[x for x in input().split(',')]
items.sort()
print(','.join(items))
```
</details>

#09: Write a program that accepts sequence of lines as input and prints the lines after making all characters in the sentence capitalized.
Suppose the following input is supplied to the program:
Hello world
Practice makes perfect
Then, the output should be:
HELLO WORLD
PRACTICE MAKES PERFECT
<details>
  <summary>Solution</summary>
  
```python3
lines=[]
while True:
    s=input()
    if s:
        lines.append(s.upper())
    else:
        break
for sentence in lines:
    print(sentence)
```
</details>

#10: Write a program that accepts a sequence of whitespace separated words as input and prints the words after removing all duplicate words and sorting them alphanumerically.
Suppose the following input is supplied to the program:
hello world and practice makes perfect and hello world again
Then, the output should be:
again and hello makes perfect practice world
<details>
  <summary>Solution</summary>
  
```python3
s=input()
words=[word for word in s.split(' ')]
print(' '.join(sorted(list(set(words)))))
```
</details>

#11: Write a program which accepts a sequence of comma separated 4 digit binary numbers as its input and then check whether they are divisible by 5 or not. The numbers that are divisible by 5 are to be printed in a comma separated sequence.
Example:
0100,0011,1010,1001
Then the output should be:
1010
Notes: Assume the data is input by console.

<details>
  <summary>Solution</summary>
  
```python3
value = []
items=[x for x in input().split(',')]
for p in items:
    intp=int(p,2)
    if not intp%5:
        value.append(p)
print(','.join(value))
```
</details>


#12: Write a program, which will find all such numbers between 1000 and 3000 (both included) such that each digit of the number is an even number.
The numbers obtained should be printed in a comma-separated sequence on a single line.
Hints:
In case of input data being supplied to the question, it should be assumed to be a console input.

<details>
  <summary>Solution</summary>
  
```python3
values = []
for i in range(1000,3001):
    s=str(i)
    if(int(s[0])%2==0) and (int(s[1])%2==0) and (int(s[2])%2==0) and (int(s[3])%2==0):
        values.append(s)
print(",".join(values))
```
</details>

#13: Write a program that accepts a sentence and calculate the number of letters and digits.
Suppose the following input is supplied to the program:
hello world! 123
Then, the output should be:
LETTERS 10
DIGITS 3

Hints:
In case of input data being supplied to the question, it should be assumed to be a console input.

<details>
  <summary>Solution</summary>
  
```python3
s=input()
d={"LETTERS":0, "DIGITS":0}
for i in s:
    if i.isdigit():
        d["DIGITS"]+=1
    elif i.isalpha():
        d["LETTERS"]+=1
    else:
        pass
print("LETTERS", d["LETTERS"])
print("DIGIT", d["DIGITS"])
```
</details>

#14: Write a program that accepts a sentence and calculate the number of upper case letters and lower case letters.
Suppose the following input is supplied to the program:
Hello world!
Then, the output should be:
UPPER CASE 1
LOWER CASE 9

Hints:
In case of input data being supplied to the question, it should be assumed to be a console input.
<details>
  <summary>Solution</summary>
  
```python3
File Edit Options Buffers Tools Python Prelude Projectile Help
s=input()
d={"UPPER CASE":0, "LOWER CASE":0}
for i in s:
    if i.isupper():
        d["UPPER CASE"]+=1
    elif i.islower():
        d["LOWER CASE"]+=1
    else:
        pass
print("UPPER CASE", d["UPPER CASE"])
print("LOWER CASE", d["LOWER CASE"])
```
</details>
