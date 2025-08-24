# Day 18 - Search in Sorted Array

### Problem
Given an array sorted in ascending order and an integer `k`, return `true` if `k` is present in the array, otherwise `false`.

### Example
Input: `arr = [1, 2, 3, 4, 6], k = 6`  
Output: `true`  
Explanation: `6` is present at index `4`.

---

### Approach 1: Direct Membership Check
```python
if k in arr:
    return True
return False
```
### Approach 2: Binary Search (Optimized)
```
class Solution:
    def searchInSorted(self, arr, k):
        low, high = 0, len(arr) - 1
        while low <= high:
            mid = (low + high) // 2
            if arr[mid] == k:
                return True
            elif arr[mid] < k:
                low = mid + 1
            else:
                high = mid - 1
        return False
```

