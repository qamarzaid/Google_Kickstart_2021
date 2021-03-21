## Google Kickstart 2021- Round A
### Problem: K-Goodness String

##### Problem:
```
Charles defines the goodness score of a string as the number of indices i such that Si≠SN−i+1 where 1≤i≤N/2. 
For example, the string CABABC has a goodness score of 2 since S2≠S5 and S3≠S4.

Charles gave Ada a string S of length N, consisting of uppercase letters and asked her to convert it into a string 
with a goodness score of K. In one operation, Ada can change any character in the string to any uppercase letter. 
Could you help Ada find the minimum number of operations required to transform the given string into a string with 
goodness score equal to K?
```
##### Input:
```
The first line of the input gives the number of test cases, T. T test cases follow.

The first line of each test case contains two integers N and K. The second line of each test case contains a string S 
of length N, consisting of uppercase letters.
```
##### Output
```
For each test case, output one line containing Case #x: y, where x is the test case number (starting from 1) and y is
the minimum number of operations required to transform the given string S into a string with goodness score equal to K.
```
##### Sample Input
```
2
5 1
ABCAA
4 2
ABAA
```
##### Sample Output
```
Case #1: 0
Case #2: 1
```
##### Code C++:
```c++
#include<bits/stdc++.h>
using namespace std;

#define pb push_back
#define mk make_pair


void solve(int j)
{
    int n, k, c = 0, nop = 0;
    cin>>n>>k;
    string s;
    cin>>s;


    for (int i = 0; i < n / 2; i++)
    {
        if (s[i] != s[(n - 1) - (i + 1) + 1])
        {
            c++;
            // cout<<"c = "<<c<<" s[i] = "<<s[i]<<"\n";
        }
    }

    if (c == k)
    {
        cout<<"Case "<<"#"<<j<<":"<<" "<<nop<<"\n";
        return;
    }
    else
    {
        nop = abs(k - c);
        cout<<"Case "<<"#"<<j<<":"<<" "<<nop<<"\n";
        return;

    }
}

int main()
{
    ios::sync_with_stdio(0);
    cin.tie(0);

    int t;
    int j = 0;
    cin>>t;
    while (t-- > 0)
    {
        j++;
        solve(j);
    }
}
```
[Code Demo Link](https://replit.com/@ZaidQamar/k-goodness-string#main.cpp)
