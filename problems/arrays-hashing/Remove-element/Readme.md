# 🗑️ Remove Element — LeetCode #27

🔗 **Problem Link:** https://leetcode.com/problems/remove-element/  
💡 **Difficulty:** Easy  

---

## 🧠 Approach

1. **Two-pointer technique**
   - Use a pointer `k` to track the position where the next valid element should be placed.
   - Iterate through the array using index `i`.

2. **Filter elements**
   - If the current element is **not equal** to the given value `val`:
     - Copy it to index `k`.
     - Increment `k`.

3. **In-place modification**
   - Elements equal to `val` are skipped.
   - The first `k` positions of the array contain the updated result.

4. **Return result**
   - Return `k`, which represents the number of elements not equal to `val`.

---

## ⏱️ Complexity Analysis

| Complexity | Description |
|----------|-------------|
| **Time** | `O(n)` — each element is visited once |
| **Space** | `O(1)` — in-place modification with constant extra space |

---

## 📝 Notes

- The relative order of elements is preserved.
- No additional data structures are used.
- Efficient and optimal for this problem.

---
