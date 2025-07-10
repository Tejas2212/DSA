# Problem: Climbing Stairs  
🔗 https://leetcode.com/problems/climbing-stairs

### My Approach:
Used simple recursion initially, then optimized with bottom-up DP (tabulation) to reduce time complexity.

### Code:
```python
class Solution:
    def climbStairs(self, n: int) -> int:
        if n <= 2:
            return n
        dp = [0] * (n + 1)
        dp[1], dp[2] = 1, 2
        for i in range(3, n + 1):
            dp[i] = dp[i - 1] + dp[i - 2]
        return dp[n]
```
