# Dynamic-Programming

### Overlapping Subproblems : 
Whenever we end up solving same subproblems again and again and again. 

### Memoization :
To solve the above problem, we have **memoization :** tend to store the value of sub problems in some map/table. 


### How to convert Recursion into DP :

- Declare a DP array : dp[n+1] (n is the size of sub problems)
- Storing the answer which is being computed for every subproblem. 
- Checking if subproblem has been previously solved. 
- **Time Complexity : O(N)** --> N recursive calls, others will take constant time as they are already computed. 
- **Space Complexity : O(N)**--> Recursion stack + O(N)--> Array


![image](https://user-images.githubusercontent.com/23376002/167126480-04637616-3950-4ced-954a-c200645672ac.png)





