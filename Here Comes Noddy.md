The city of toyland can be represented as a N*M matrix.
Our beloved Noddy rides his car around the town.
He starts at (0,0), then goes towards right. Upon reaching a dead end he will always take a right turn. Noddy will never visit a block that he has already visited before.
Upon returning home Noddy has forgotten everything that he saw during is drive. Help him by printing the numbers on the blocks of the town in the order that Noddy visited.

_Input Format_

First line contains two integers, N and M.
Next N lines contain M integers each, collectively they denote the N*M matrix.

Constraints

1 <= N,M <= 10

Output Format

Output N*M integers on one line with a space between every two consecutive integers. These must be the numbers written on the blocks of toyland in order that Noddy visited.

Sample Input 0

3 3
1 2 3
4 5 6
7 8 9
Sample Output 0

1 2 3 6 9 8 7 4 5
Explanation 0

Noddy's Journey :
- Start at (0,0) which is 1.
- Move right to (0,1) which is 2.
- Move right to 3.
- Dead end, so Noddy turns right and moves to 6.
- Move further down to 9
- Dead end so Noddy turns right and moves to 8
- Move further left to 7
- Dead end so Noddy turns right and moves to 4
- Dead end ahead so Noddy turns right and moves to 5
- his journey ends here as now he has seen all the blocks.


####Solution( Python ):

n,m=list(map(int,input().split()))
lst=[input().split() for i in range(n)]
top=0
right=m-1
left=0
down=n-1
while(top<=down and left<=right):
    for i in range(left,right+1):
        print(lst[top][i],end=' ')
    top+=1
    for i in range(top,down+1):
        print(lst[i][right],end=' ')
    right-=1
    if not (left<=right and top<=down):
        break
    for i in range(right,left-1,-1):
        print(lst[down][i],end=' ')
    down-=1
    for i in range(down,top-1,-1):
        print(lst[i][left],end=' ')
    left+=1
    
