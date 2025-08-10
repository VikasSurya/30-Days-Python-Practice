# Day 15 - Print 1 To N Without Loop ✅

## 🧠 Problem:
You are given an integer **n**.  
Print all numbers from **1 to n** in a single line, separated by spaces.  

**Note:**  
- You must **use recursion only**.
- No loops allowed.

---

## 🔍 Example:

### Example 1:
**Input:**  
`n = 10`  
**Output:**  
`1 2 3 4 5 6 7 8 9 10`

---

## 🚀 Approach:

1. If `n` becomes `0`, stop recursion (**base case**).
2. Recursively call the function for `n-1`.
3. Print the current number after returning from recursion.
4. This ensures numbers are printed from `1` to `n` in order.

---

## 🧑‍💻 Code (Python):

```python
class Solution:    
    def printNos(self, n):
        # Base case: Stop when n is 0
        if n == 0:
            return
        
        # Recursive call for n-1
        self.printNos(n - 1)
        
        # Print current number
        print(n, end=" ")
