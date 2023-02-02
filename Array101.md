
# 485. Max Consecutive Ones 
##### 23/02/01/Wed

```  
Input: nums = [1,1,0,1,1,1]  
Output: 3  
Explanation: The first two digits or the last three digits are consecutive 1s. The maximum number of consecutive 1s is 3.
```  

### [Solution1: using conditional statements]

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

: count 와 maxcount 변수를 두고, 1이 나올때마다 count도 계속 1씩 더해줌. 그리고 maxcount 값을 count 값으로 업데이트. 그리고 0이 나오는 순간 count는 0으로 갱신되지만 maxcount 값은 계속 유지. 그리고 maxcount 값을 출력


### [Solution2: using ternary operator]

```java

class Solution {
  public int findMaxConsecutiveOnes(int[] nums {
  
  int count = 0, maxcount = 0;
  for (int n : nums)
    maxcount = Math.max(maxcount, count = n == 0 ? 0 : count + 1);
    
   return maxcount;
   
}
```

: 삼항연산자(조건문?참:거짓의 형태)를 써서 maxcount, count 중 더 큰 값을 반환하는 코드가 됨. 




# 977. Squares of a Sorted Array
##### 23/02/02/Thu

```  
Given an integer array nums sorted in non-decreasing order, return an array of the squares of each number sorted in non-decreasing order.  

Input: nums = [-4,-1,0,3,10]
Output: [0,1,9,16,100]
Explanation: After squaring, the array becomes [16,1,0,9,100].
After sorting, it becomes [0,1,9,16,100].
```  


### [Solution1: ]

```java

class Solution {
  public int[] sortedSquares(int[] nums {
   
   
   
    }
 return count; 
  }
}
```





