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
