# 🚀 Longest Common Prefix - Python Solution

## 🔍 Problem Statement

Write a function to find the **longest common prefix** string amongst an array of strings.

If there is no common prefix, return an **empty string** `""`.

### ✅ Example:

**Input:**  
```python
strs = ["flower", "flow", "flight"]
```

**Output:**  
```
"fl"
```

## 💻 Code

```python
from typing import List

class Solution:
    def longestCommonPrefix(self, strs: List[str]) -> str:
        if not strs:
            return ""

        smallest = min(strs)

        for i in range(len(smallest)):
            char = smallest[i]

            for word in strs:
                if word[i] != char:
                    return smallest[:i]

        return smallest
```

## 🧪 Test Cases

```python
sol = Solution()

print(sol.longestCommonPrefix(["flower", "flow", "flight"]))  # Output: "fl"
print(sol.longestCommonPrefix(["dog", "racecar", "car"]))     # Output: ""
print(sol.longestCommonPrefix(["interview", "interval", "internal"]))  # Output: "inte"
print(sol.longestCommonPrefix(["a"]))  # Output: "a"
print(sol.longestCommonPrefix([]))    # Output: ""
```

## ⏱️ Time & Space Complexity

- **Time Complexity:** O(N × M)  
  N = number of strings  
  M = length of the smallest string

- **Space Complexity:** O(1)
