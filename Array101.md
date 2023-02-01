
# 485. Max Consecutive Ones 
### 23/02/01/Wed

### [Solution1]

```java

class Solution {
  public int findMaxConsecutiveOnes(int[] nums {
  
    int count = 0;
    int maxcount = 0;
   
   for(int n : nums) {
      if(n == 1){
          count++;
          if (maxcount < count) maxcount = count;
      }
       else count = 0;       
      
      }
      
      return maxcount;
      
   }
}
  
