# 🔁 Contains Duplicate — LeetCode #217

🔗 **Problem Link:** https://leetcode.com/problems/contains-duplicate/  
💡 **Difficulty:** Easy  

---

## 🧠 Approach

1. **Use a HashSet**
   - A `HashSet` stores only unique values.
   - It allows constant-time lookup on average.

2. **Iterate through the array**
   - For each number:
     - Check if it already exists in the set.
     - If it does, a duplicate is found → return `true`.
     - Otherwise, add the number to the set.

3. **No duplicates found**
   - If the loop completes without finding any repeated values, return `false`.

---

## ⏱️ Complexity Analysis

| Complexity | Description |
|----------|-------------|
| **Time** | `O(n)` — each element is processed once |
| **Space** | `O(n)` — HashSet stores up to `n` elements |

---

## 📝 Notes

- This approach is more efficient than a brute-force nested loop solution.
- HashSet provides fast lookups, making the solution scalable for large inputs.

---
