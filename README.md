# Dynamic-Programming

### Overlapping Subproblems : 
Whenever we end up solving same subproblems again and again and again. 

### Memoization :
To solve the above problem, we have **memoization :** tend to store the value of sub problems in some map/table. 


### How to convert Recursion into DP :

- Declare a DP array : dp[n+1] (n is the size of sub problems)
- Storing the answer which is being computed for every subproblem. 
- Checking if subproblem has been previously solved. 
