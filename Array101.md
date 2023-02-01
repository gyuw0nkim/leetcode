
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
```

: count 와 maxcount 변수를 두고, 1이 나올때마다 count도 계속 1씩 더해줌. 그리고 maxcount 값을 count 값으로 
