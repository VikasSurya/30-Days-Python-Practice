1. Longest Common Prefix

Write a function to find the longest common prefix string amongst an array of strings.
If there is no common prefix, return an empty string "".

Example 1:

Input: strs = ["flower","flow","flight"]
Output: "fl"

**********Solution**********


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
