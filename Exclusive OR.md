# Exclusive Or
Find the XOR of two numbers and print it.

Hint : Input the numbers as strings.

Input Format

First line contains first number X and second line contains second number Y.
The numbers will be given to you in binary form.

Constraints

0 <= X <= 2^1000
0 <= Y <= 2^1000

Output Format

Output one number in binary format, the XOR of two numbers.

### Sample Input 0

11011 <br />
10101

### Sample Output 0

01110

### Solution (Python):
```py
s1=input()
s2=input()
if(len(s1)>len(s2)):
    s2=s2.zfill(len(s1))
else:
    s1=s1.zfill(len(s2))
for i in range(len(s1)):
    print('0',end='') if s1[i]==s2[i] else print('1',end='')
```
