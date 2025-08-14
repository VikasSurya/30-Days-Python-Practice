# 📅 Day 16 – Array Problems

## 📝 Problem 1 – Count of Elements Less Than or Equal to X

**Problem Statement:**  
Given an unsorted array `arr`. Find the count of elements less than or equal to the given element `x`.

**Example:**
Input:
x = 9
arr = [10, 1, 2, 8, 4, 5]

Output:
5

Explanation:
The 5 elements are 1, 2, 8, 4, and 5.

markdown
Copy
Edit

**Approach:**  
1. Initialize a counter to `0`.  
2. Loop through each element in the array.  
3. If the element is less than or equal to `x`, increment the counter.  
4. Return the counter.

**Python Code:**
```python
class Solution:
    def countOfElements(self, x, arr):
        count = 0
        for i in arr:
            if i <= x:
                count += 1
        return count
```
## 📝 Problem 2 – Value Equal to Index Value

**Problem Statement:**
Given an array arr. Your task is to find the elements whose value is equal to their index value (consider 1-based indexing).

Note: There can be more than one such element. Return all matching index values.

**Example:**

Input:  
arr = [15, 2, 45, 4, 7]  

Output:  
[2, 4]

Explanation:  
arr[2] = 2 and arr[4] = 4 match their 1-based index.


**Approach:**

Create an empty result list.

Iterate from index 1 to len(arr).

Compare the current index (1-based) with the element at (index-1).

If equal, append the element (or index) to the result list.

Return the result.

**Python Code:**

```class Solution:
    # Function to find values in array equal to their indices
    def valueEqualToIndex(self, arr):
        res = []
        for i in range(1, len(arr) + 1):
            if i == arr[i - 1]:
                res.append(arr[i - 1])
        return res
```
