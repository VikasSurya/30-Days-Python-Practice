# Day 17 - Remove Vowels from a String ✅

## 🧠 Problem:
Given a string `s`, remove all vowels (`a, e, i, o, u` in both lowercase and uppercase) from it.

---

## 🔍 Example:

### Example 1:
**Input:**  
`s = "welcome to geeksforgeeks"`  
**Output:**  
`"wlcm t gksfrgks"`  

**Explanation:**  
All vowels are removed and consonants remain in the same order.

---

## 🚀 Approach:

1. Define a string containing all vowels (`"aeiouAEIOU"`).
2. Loop through each character in the given string.
3. If the character is **not a vowel**, add it to the result.
4. Return the result string.

---

## 🧑‍💻 Code (Python):

```python
class Solution:
    def removeVowels(self, s):
        vowels = "aeiouAEIOU"
        res = ''
        for char in s:
            if char not in vowels:
                res += char
        return res

# Example usage:
s = "welcome to geeksforgeeks"
print(Solution().removeVowels(s))  # Output: wlcm t gksfrgks
