# Minimize Waste Cells

Previously, it was important for every company to have a motto.Now, it is important for every company to have a banner.
Since companies want to save their resources, they decided to convert their motto into a banner.
How this works is, you create a square matrix of size N x N, and fill in the elements of this matrix using the motto in row-major order.
The remaining spaces in the matrix are called waste cells and are to be represented as '?'.
You have to choose N in such a way that the number of waste cells is minimized.

Input
Input consists of one line only, containing the company motto

Output
Output must consist of the matrix formed from the input string

Notes
The length of the input string will not exceed 1000

Sample Input 0 <br />
```
nike - just do it!
```
Sample Output 0<br />

```
nike 
- jus
t do 
it!??
?????
```
Sample Input 1

```
oneplus - never settle!
```
Sample Output 1
```
onepl
us - 
never
 sett
le!??
```
### Solution (python):

```py
import sys
line=sys.stdin.read()
n=int(len(line)**(0.5))
if n*n<len(line):
    n=n+1
line=line.ljust(n*n,'?')
for i in range(0,len(line),n):
    print(line[i:i+n])
```
