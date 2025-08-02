# 🔄 Day 1 – Print Alternate Elements of an Array

Today’s problem was a simple one, but very useful for learning indexing and loop control.

---

## 🔹 Problem Statement  
You are given an array `arr[]`, and you need to return a list of elements in **alternate order**, starting from index `0`.

📌 That means:  
Take element at index `0`, skip index `1`, take index `2`, skip index `3`, and so on.

---

## ✅ Example  
**Input:** `arr = [1, 2, 3, 4]`  
**Output:** `[1, 3]`

**Explanation:**  
Take index 0 → `1`  
Skip index 1 → `2`  
Take index 2 → `3`  
Skip index 3 → `4`

---

## 💡 Approach  

- Initialize an empty list `result`.
- Loop through the array from index `0` to `len(arr)`.
- For every even index `i`, append `arr[i]` to `result`.
- Finally, return the `result`.

---

## 💻 Python Code
```python
class Solution:
    def getAlternates(self, arr):
        result = []
        for i in range(0, len(arr)):
            if i % 2 == 0:
                result.append(arr[i])
        return result
