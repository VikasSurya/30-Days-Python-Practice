# Day 14 - LeetCode 125. Valid Palindrome ✅

## 🧠 Problem:
A string is a **palindrome** if, after:
- converting all uppercase letters into lowercase letters, and  
- removing all **non-alphanumeric** characters,  

…it reads **the same forward and backward**.

**Return `True` if the string is a palindrome, else return `False`.**

---

## 🔍 Example:

### Example 1:
**Input:**  
`s = "A man, a plan, a canal: Panama"`  
**Output:**  
`True`  
**Explanation:**  
After cleaning: `"amanaplanacanalpanama"` → it's the same forward and backward.

### Example 2:
**Input:**  
`s = "race a car"`  
**Output:**  
`False`

---

## 🚀 Approach:

1. **Remove non-alphanumeric characters** using regex:  
   `re.sub(r'[^A-Za-z0-9]', '', s)`
2. **Convert the cleaned string to lowercase**.
3. Use **two pointers**:
   - One starting at the beginning
   - One at the end
   - Move both inward and compare characters.
4. If mismatch → return False.
5. If loop completes → return True.

---

## 🧑‍💻 Code (Python):

```python
import re

class Solution:
    def isPalindrome(self, s: str) -> bool:
        # Clean the string: remove non-alphanumerics and lowercase it
        cl = (re.sub(r'[^A-Za-z0-9]', '', s)).lower()

        start = 0
        end = len(cl) - 1

        while start < end:
            if cl[start] != cl[end]:
                return False
            start += 1
            end -= 1

        return True
