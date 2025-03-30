## Problem Description

Given two strings `s` and `t`, return `true` if `s` is a subsequence of `t`, or `false` otherwise. A subsequence is a sequence that can be derived from another sequence by deleting some elements without changing the order of the remaining elements.

**Example 1**:
Input: s = "abc", t = "ahbgdc"
Output: true

複製

**Example 2**:
Input: s = "axc", t = "ahbgdc"
Output: false

複製

**Example 3**:
Input: s = "", t = "g"
Output: true

複製

**Constraints**
0 <= s.length <= 100
0 <= t.length <= 10^4
s and t consist only of lowercase English letters.

複製

## Solution

### _Related Topic_
`Two Pointers` `String`

### _C++ Code_
```cpp
class Solution {
public:
    bool isSubsequence(string s, string t) {
        int i = 0, j = 0;
        while (i < s.length() && j < t.length()) {
            if (s[i] == t[j]) {
                i++;
            }
            j++;
        }
        return i == s.length();
    }
};
Complexity Anlysis
Time Complexity: O(n + m) // where n is the length of s and m is the length of t
Space Complexity：O(1) // only constant extra space is used
