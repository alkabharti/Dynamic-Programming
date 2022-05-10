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


```java
static int f(int n, int[] dp)
{
    if(n<=1) return n;
    
    if(dp[n]!= -1) return dp[n];
    return dp[n]= f(n-1,dp) + f(n-2,dp);
}
```

![image](https://user-images.githubusercontent.com/23376002/167126480-04637616-3950-4ced-954a-c200645672ac.png)


### 2. Tabulation :
In the tabulation approach to DP (also known as the table-filling method) we solve all sub-problems and store their results on a matrix. these results are then used to solve larger problems that depend on the previously computed results. Because of this, the tabulation approach is also known as a **bottom-up approach**.

- **Time Complexity : O(N)**  
- **Space Complexity : O(N)**


```java
public static void main(String args[]) 
{

  int n=5;
  int dp[]=new int[n+1];
  Arrays.fill(dp,-1);
  dp[0]= 0;
  dp[1]= 1;
  
  for(int i=2; i<=n; i++)
  {
      dp[i] = dp[i-1]+ dp[i-2];
  }
  System.out.println(dp[n]);  
}
```

![image](https://user-images.githubusercontent.com/23376002/167256612-fa264ad2-eb2c-4214-8573-7ea35b5ff0ff.png)


### 3. Space Optimization :


```java
public static void main(String args[]) 
{
    int n=5;

    int prev2 = 0;
    int prev = 1;

    for(int i=2; i<=n; i++){
        int cur_i = prev2+ prev;
        prev2 = prev;
        prev= cur_i;
    }
    System.out.println(prev);
}
```

- **Time Complexity : O(N)**  
- **Space Complexity : O(1)**




## How to find if a problem is of DP:

- Count the no. of ways
- If need to find min/max from multiple ways (best way)
- Count distinct ways



**Reference :** 

- https://takeuforward.org/data-structure/dynamic-programming-introduction/
- https://takeuforward.org/dynamic-programming/striver-dp-series-dynamic-programming-problems/
