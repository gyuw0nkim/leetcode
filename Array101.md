
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


### [Solution1: 그냥 제곱한 다음에 sorted로 정렬. 근데 나중에 디스커션을 보니까 이 값은 초기 입력값을 아예 새로운 값으로 대체하는거라 별로 좋지 않은 풀이라고 하는데.... 그래서 뭐 포인터를 쓰던데.... 그거까지 잘 모르겠슴....]

```Python
class Solution(object):
  def sortedSquares(self, nums):
  
    square = [num**2 for num in nums]
    
    return list(sorted(square))

```

뭐지 ㅅㅂ 계속 안되다가 그냥 들여쓰기 하니까 갑자기 돌아간다. 들여쓰기 규칙이 뭐가 있나보다 해서 찾아봤다.  
들여쓰기는 코드를 읽기 쉽도록 일정한 간격을 띄워서 작성하는 방법입니다. 특히 파이썬은 들여쓰기 자체가 문법입니다. 예를 들어 if의 다음 줄은 항상 들여쓰기를 해야 합니다. 만약 들여쓰기를 하지 않으면 문법 에러이므로 코드가 실행되지 않습니다. 파이썬은 공백 2칸, 공백 4칸, 탭 문자 등을 각각 사용해도 동작이 잘 됩니다. 하지만 파이썬 코딩 스타일 가이드(PEP 8)에서는 공백 4칸으로 규정하고 있습니다. 따라서 공백 4칸을 사용하는 것이 좋습니다.



# 1089. Duplicate Zeros
##### 23/02/09/Thu

```  
Given a fixed-length integer array arr, duplicate each occurrence of zero, shifting the remaining elements to the right.

Note that elements beyond the length of the original array are not written. Do the above modifications to the input array in place and do not return anything.

Input: arr = [1,0,2,3,0,4,5,0]
Output: [1,0,0,2,3,0,0,4]
Explanation: After calling your function, the input array is modified to: [1,0,0,2,3,0,0,4]

Input: arr = [1,2,3]
Output: [1,2,3]
Explanation: After calling your function, the input array is modified to: [1,2,3]
```  

### [Solution]

```python

n = len(arr)
i = 0

while(i < n):
    if(arr[i] == 0):
      arr.insert(i+1, 0)
      arr.pop()
      i += 2
    
    else:
      i += 1
    
```


# 88. Merge Sorted Array
##### 23/02/14/Tue

```  
You are given two integer arrays nums1 and nums2, sorted in non-decreasing order, and two integers m and n, representing the number of elements in nums1 and nums2 respectively.  

Merge nums1 and nums2 into a single array sorted in non-decreasing order.  

The final sorted array should not be returned by the function, but instead be stored inside the array nums1. To accommodate this, nums1 has a length of m + n, where the first m elements denote the elements that should be merged, and the last n elements are set to 0 and should be ignored. nums2 has a length of n.  

Example 1:

Input: nums1 = [1,2,3,0,0,0], m = 3, nums2 = [2,5,6], n = 3
Output: [1,2,2,3,5,6]
Explanation: The arrays we are merging are [1,2,3] and [2,5,6].
The result of the merge is [1,2,2,3,5,6] with the underlined elements coming from nums1.


Example 2:

Input: nums1 = [1], m = 1, nums2 = [], n = 0
Output: [1]
Explanation: The arrays we are merging are [1] and [].
The result of the merge is [1].


Example 3:

Input: nums1 = [0], m = 0, nums2 = [1], n = 1
Output: [1]
Explanation: The arrays we are merging are [] and [1].
The result of the merge is [1].
Note that because m = 0, there are no elements in nums1. The 0 is only there to ensure the merge result can fit in nums1.
```  

### [Solution]

```python
