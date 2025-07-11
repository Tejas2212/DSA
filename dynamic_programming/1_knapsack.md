# Problem: Climbing Stairs  
🔗 https://www.naukri.com/code360/problems/0-1-knapsack_920542

### My Approach:
Used simple recursion initially




### Code:
```Java 
import java.util.* ;
import java.io.*; 

public class Solution{
    static int knapsack(int[] wt, int[] val, int n, int w) {

           if(n==0 || w==0){
		    return 0;
		   }
		   if(wt[n-1]> w){
		     return knapsack(wt,val,n-1,w);
		    
		   }else{
		     return Math.max(val[n-1]+knapsack(wt,val,n-1, w-wt[n-1]) , knapsack(wt,val, n-1,w));
		   }

    }
}

