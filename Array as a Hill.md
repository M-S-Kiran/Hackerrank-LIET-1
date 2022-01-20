# Array as a Hill

Array of integers is a hill, if:

it is strictly increasing in the beginning;
after that it is constant;
after that it is strictly decreasing.
The first block (increasing) and the last block (decreasing) may be absent. It is allowed that both of this blocks are absent.
For example, the following three arrays are a hill: [5, 7, 11, 11, 2, 1], [4, 4, 2], [7],
but the following three are not unimodal: [5, 5, 6, 6, 1], [1, 2, 1, 2], [4, 5, 5, 6].

Write a program that checks if an array is a hill.

#### Input Format

The first line contains integer n (1 ≤ n ≤ 100) — the number of elements in the array.

The second line contains n integers a1, a2, ..., an (1 ≤ ai ≤ 1000) — the elements of the array.

#### Output Format

Print "yes" if the given array is a hill. Otherwise, print "no".

### Solution (C++)

```c++
#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
using namespace std;


int main() {
    int n,j;
    cin>>n;
    int arr[n];
    if(n==1){
        cout<<"yes"; 
        return 0;
    }
    for(int i=0;i<n;i++){
        cin>>arr[i];
    }
    j=0;
    while((arr[j]<arr[j+1]) && (j<n-1)){
        j++;
    }
    while(arr[j]==arr[j+1]&&j<n-1)
        j++;
    while(arr[j]>arr[j+1]&&j<n-1){
        j++;
    } 
    if(j==n-1)
        cout<<"yes";
    else
        cout<<"no";
    return 0;
}

```
