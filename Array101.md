
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


# 1295. Max Consecutive Ones 
##### 23/02/02/Thu

```  
Input: nums = [12,345,2,6,7896]  
Output: 2  
Explanation:   
12 contains 2 digits (even number of digits).  
345 contains 3 digits (odd number of digits).  
2 contains 1 digit (odd number of digits).  
6 contains 1 digit (odd number of digits).  
7896 contains 4 digits (even number of digits).  
Therefore only 12 and 7896 contain an even number of digits.  
Given an integer array nums sorted in non-decreasing order, return an array of the squares of each number sorted in non-decreasing order.  
Input: nums = [-4,-1,0,3,10]
Output: [0,1,9,16,100]
Explanation: After squaring, the array becomes [16,1,0,9,100].
After sorting, it becomes [0,1,9,16,100].
```  


### [Solution1: using String.valueOf]

```java
class Solution {
  public int findNumbers(int[] nums {
    int count = 0;
    for(int num : nums){
      if (String.valueOf(num).length() % 2 == 0)
        count++;
  public int[] sortedSquares(int[] nums {
   
   
   
    }
 return count; 
  }
}
```
- Question 1: where did for(int num : nums) came from? because yesterday it was for(int n : nums) and what's the difference between num and n ? i didn't do variable declaration for both(n, num) but how can i use it MUDDED  
: int 를 이용해서 for문 안에서 바로 변수선언을 하기 때문에 n으로 쓰든 num으로 쓰든 banana로 쓰든 상관이 없다. 

- Question 2: why there is () after length() ? what is the difference between length and length()
: length와 length()는 쓰임이 다르다. length는 길이를 반환했을 때 data type이 array 형태이고, length()는 string object의 형태이다. 그냥 반환하는 데이터 형태가 달라서 그런 듯?



# 977. Squares of a Sorted Array
##### 23/02/03/Fri

```  
Given an integer array nums sorted in non-decreasing order, return an array of the squares of each number sorted in non-decreasing order.  

Input: nums = [-4,-1,0,3,10]
Output: [0,1,9,16,100]
Explanation: After squaring, the array becomes [16,1,0,9,100].
After sorting, it becomes [0,1,9,16,100].
```  


### [Solution1: ]

```
```





