# 169. Majority Element

## Description

Given an array `nums` of size `n`, return the majority element.

The majority element is the element that appears more than `⌊n / 2⌋` times. You may assume that the majority element always exists in the array.

 

### Example 1:
``` md
Input: nums = [3,2,3]
Output: 3
```
### Example 2:
```md
Input: nums = [2,2,1,1,1,2,2]
Output: 2
```

## Code
### Boyer-Moore Voting Algorithm
```py
class Solution:
    def majorityElement(self,nums):
        count = 0
        current = 0
        for i in nums:
            if count == 0:
                current = i
            count += 1 if i == current else -1
        return current
```

### Using Set
```py

```