# Dynamic-Programming

### Overlapping Subproblems : 
Whenever we end up solving same subproblems again and again and again. 

## DP Problems can be solved using two approaches :

### 1. Memoization :
To solve the above problem, we have **memoization :** tend to store the value of sub problems in some map/table. <br/>
Memoization is also known as a **top-down approach**. It starts from solving the highest-level sub-problems. Initially, it solves the highest-level subproblem and then solve the next sub-problem recursively and the next. 

### How to convert Recursion into DP :

- Declare a DP array : dp[n+1] (n is the size of sub problems)
- Storing the answer which is being computed for every subproblem. 
- Checking if subproblem has been previously solved. 
- **Time Complexity : O(N)** --> N recursive calls, others will take constant time as they are already computed. 
- **Space Complexity : O(N)**--> Recursion stack **+ O(N)**--> Array


![image](https://user-images.githubusercontent.com/23376002/167126480-04637616-3950-4ced-954a-c200645672ac.png)


### 2. Tabulation :
In the tabulation approach to DP (also known as the table-filling method) we solve all sub-problems and store their results on a matrix. these results are then used to solve larger problems that depend on the previously computed results. Because of this, the tabulation approach is also known as a **bottom-up approach**.

- **Time Complexity : O(N)**  
- **Space Complexity : O(N)**

