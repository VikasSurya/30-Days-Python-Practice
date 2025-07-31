# 🚀 Day 9 – Python Challenge

## ✅ Problem 1: Check if Array is Palindrome

**Problem Statement:**  
Given an array `arr`, check if it is a palindrome.  
An array is a palindrome if it reads the same forwards and backwards.

**Example:**
```
Input:  arr = [1, 2, 3, 2, 1]  
Output: True  
Explanation: The reversed array [1, 2, 3, 2, 1] is same as original.
```

### 🔍 Solution:

```python
from typing import List

class Solution:
    def isPerfect(self, arr: List[int]) -> bool:
        # Method 1: Reverse approach
        if arr == arr[::-1]:
            return True
        return False

        # Method 2: Two-pointer approach (more efficient)
        left, right = 0, len(arr) - 1
        while left < right:
            if arr[left] != arr[right]:
                return False
            left += 1
            right -= 1
        return True
```

---

## ✅ Problem 2: Find Element in Array

**Problem Statement:**  
Given an array `arr[]` and an integer `x`, return the index of the first occurrence of `x`, or `-1` if not found.

**Example:**
```
Input:  arr = [1, 2, 3, 4], x = 3  
Output: 2  
Explanation: Element 3 is found at index 2.
```

### 🔍 Solution:

```python
class Solution:
    def search(self, arr, x):
        for i in range(len(arr)):
            if arr[i] == x:
                return i
        return -1
```

---

## ✅ Summary

- Used **slicing** and **two-pointer** approach to check for palindrome.
- Used **linear search** to find the index of an element in an array.
- Practiced array traversal, condition checking, and basic logic building.

