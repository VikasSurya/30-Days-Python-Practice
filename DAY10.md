# 🚀 Day 10 – String Problems on Character Frequency

Today I solved two fundamental string problems that are frequently asked in coding interviews — one about finding the **first repeating character**, and the other about the **first non-repeating character**.

---

## 🔁 Problem 1: First Repeating Character

### 🔹 Problem Statement  
Given a string `s` containing only lowercase English letters, return the **first character that repeats** in the string.  
If no character repeats, return `#`.

### ✅ Example  
**Input:** `"geeksforgeeks"`  
**Output:** `'g'`

**Explanation:**  
Repeating characters: `g`, `e`, `k`, `s`  
`g` is the first one to repeat.

### 💻 Code
```python
class Solution:
    def firstRep(self, s):
        for i in range(len(s)):
            if s[i] in s[i+1:]:
                return s[i]
        return '#'
```

# 🔁 Problem 2: First Non-Repeating Character

## 🔹 Problem Statement  
Given a string `s` consisting of only lowercase English letters, return the **first character that does not repeat**.  
If all characters repeat, return `$`.

---

## ✅ Example  
**Input:** `"geeksforgeeks"`  
**Output:** `'f'`

**Explanation:**  
Characters like `g`, `e`, `k`, `s` repeat more than once.  
But `f` appears only once, and it's the first such character.

---

## 💡 Thought Process  
- Use a dictionary (`freq`) to count how many times each character appears.
- Then loop through the original string.
- The first character with frequency `1` is our answer.
- If none found, return `$`.

---

## 💻 Python Code
```python
class Solution:
    def nonRepeatingChar(self, s):
        freq = {}
        for ch in s:
            freq[ch] = freq.get(ch, 0) + 1
        for ch in s:
            if freq[ch] == 1:
                return ch
        return '$'

