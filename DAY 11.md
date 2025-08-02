# 🔺 Day 11 – Peak Element Problem (Linear Search Approach)

Today I solved the "Peak Element" problem using a simple linear scan approach.

---

## 🔹 Problem Statement  
You are given an array `arr[]` where **no two adjacent elements are equal**.  
An element is called a **peak** if it is **greater than both its neighbors**.  
Return the **index of any one peak element**.

📌 Notes:  
- Consider elements outside the bounds (`arr[-1]` and `arr[n]`) as **negative infinity (-∞)**.  
- If there are multiple peak elements, return the index of **any one of them**.  
- The output will be `"true"` if your returned index satisfies the peak condition.

---

## ✅ Example  
**Input:** `arr = [1, 2, 4, 5, 7, 8, 3]`  
**Output:** `true`  
**Explanation:**  
`arr[5] = 8` is a peak because `arr[4] < 8 > arr[6]`.

---

## 💡 Approach (Linear Scan)

- Insert `-inf` at the start and end of the array to simplify edge checks.
- Loop from index `1` to `len(arr) - 2`:
  - At each index `i`, check if it's greater than its neighbors:
    ```python
    if arr[i-1] < arr[i] and arr[i] > arr[i+1]
    ```
  - If true, return `i - 1` (we adjust because we added `-inf` at the start).
- If no peak found (which shouldn't happen per constraints), return `0`.

---

## 💻 Python Code
```python
class Solution:   
    def peakElement(self, arr):
        arr.insert(0, float('-inf'))  # Insert -∞ at the start
        arr.append(float('-inf'))     # Append -∞ at the end

        for i in range(1, len(arr) - 1):
            if arr[i - 1] < arr[i] and arr[i] > arr[i + 1]:
                return i - 1  # Adjust index due to inserted -inf

        return 0
