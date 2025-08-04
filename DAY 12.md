# 🚀 Day 12 - String Manipulation Problems

---

## ✅ Problem 1: Upper Case Conversion  


### 🧾 Problem Statement  
Given a string `s`, convert the **first letter of each word** in the string to **uppercase**.  

### 📥 Input  
`s = "gEEKs"`  

### 📤 Output  
`"GEEKs"`  

---

### ✅ Example  

| Input                | Output              |
|---------------------|---------------------|
| "gEEKs for geeks"    | "GEEKs For Geeks"   |

---

### 💡 Approach  
- Traverse the string character by character.
- If the character is at index 0, capitalize it.
- If the character is preceded by a space, capitalize it.
- Otherwise, add the character as-is.

---

### ✅ Python Code  

```python
class Solution:
    def convert(self, s):
        res = ""
        for i in range(len(s)):
            if i == 0 or s[i - 1] == " ":
                res += s[i].upper()
            else:
                res += s[i]
        return res
```
# ✅ Problem: Convert a List of Characters into a String 

---

## 🧾 Problem Statement  
Given a list of characters, merge all of them into a **single string**.

---

## 📥 Input  
- `N = 13`  
- `Char array = ['g', 'e', 'e', 'k', 's', 'f', 'o', 'r', 'g', 'e', 'e', 'k', 's']`

---

## 📤 Output  
- `"geeksforgeeks"`

---

## 🧠 Explanation  
We are given a list of individual characters. The goal is to **combine them all into one string** without any spaces.

---

## 💡 Approach  
1. Initialize an empty string `res`.
2. Traverse each character in the list.
3. Append it to `res`, skipping spaces (if any).
4. Return the final string.

---

## ✅ Python Code  

```python
class Solution:
    def chartostr(self, arr, N):
        res = ""
        for i in arr:
            if i == ' ':
                continue
            else:
                res += i
        return res
