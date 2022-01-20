# Consecutive Prime Sum

Some prime numbers can be expressed as Sum of other consecutive prime numbers.

For example

5 = 2 + 3
17 = 2 + 3 + 5 + 7
41 = 2 + 3 + 5 + 7 + 11 + 13

Your task is to find out how many prime numbers which satisfy this property are present in the range 3 to N subject to a constraint that summation should always start with number 2.

Write code to find out number of prime numbers that satisfy the above mentioned property in a given range.

#### Input Format:
Each test case contains a number N <= 1000000000

#### Output Format:
Print the total number of all such prime numbers which are less than or equal to N.

### Solution (Python):

```py
b=int(input())
c=0
v=0
for n in range(b+1):

    if(n>1):
        def isPrime(n):
            for i in range(2,int(n**0.5)+1):
                if (n%i==0):
                    return False
        
            return True
   
        if(isPrime(n)):
            c=c+n
            
            if(isPrime(c) and c<b):
                
                v=v+1
            elif(c>b):
                break

print(v-1)

```
