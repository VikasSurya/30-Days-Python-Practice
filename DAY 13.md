# 🧠 Day 13 – One Odd Occurrence Problem (Python)

## 📌 Problem Statement  
Given an array of **positive integers** where all numbers occur an **even number of times** *except one number*, which occurs an **odd number of times**, return that number.

---

## 🧪 Example

```python
Input:  arr = [1, 2, 3, 2, 3, 1, 3]
Output: 3
```

🧾 **Explanation**:  
- `1` appears twice ✅  
- `2` appears twice ✅  
- `3` appears **three times** ❗ → This is the odd occurring number.

---

## 🧠 Approach 1: Using Dictionary (Hash Map)

### ✅ Logic  
- Traverse the array and count frequency of each element using a dictionary.  
- Check which number has an odd frequency (`count % 2 != 0`).  
- Return that number.

---

## ✅ Python Code – Dictionary Method

```python
class Solution:
    def getOddOccurrence(self, arr):
        result = {}
        
        for i in arr:
            if i in result:
                result[i] += 1
            else:
                result[i] = 1
                
        for i in result:
            if result[i] % 2 != 0:
                return i
```

---
% 2 != 0:
                return i
