# 🧵 Longest Common Prefix — LeetCode #14

🔗 **Problem Link:** https://leetcode.com/problems/longest-common-prefix/  
💡 **Difficulty:** Easy  

---

## 🧠 Approach

1. **Handle edge cases**
   - If the input array is `null` or empty, return an empty string.

2. **Find the shortest string length**
   - The longest possible common prefix cannot be longer than the shortest string in the array.
   - Iterate through all strings to determine the minimum length.

3. **Character-by-character comparison**
   - Iterate index by index from `0` up to the shortest length.
   - Use the character from the first string as a reference.
   - Compare it with characters at the same index in all other strings.

4. **Stop on mismatch**
   - If any string has a different character at the current index, return the prefix built so far.

5. **Return result**
   - The accumulated characters form the longest common prefix.

---

## ⏱️ Complexity Analysis

| Complexity | Description |
|----------|-------------|
| **Time** | `O(n × m)` — where `n` is the number of strings and `m` is the length of the shortest string |
| **Space** | `O(m)` — for storing the resulting prefix |

---

## 📝 Notes

- The approach compares strings column-wise (character by character).
- Efficient for small to medium input sizes.
- Simple and easy to understand implementation.

---
