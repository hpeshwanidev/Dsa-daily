# 🏆 Majority Element — LeetCode #169

🔗 **Problem Link:** https://leetcode.com/problems/majority-element/  
💡 **Difficulty:** Easy  

---

## 🧠 Approach

This solution uses the **Boyer-Moore Majority Vote Algorithm**:

1. **Initialize**
   - Pick the first element as the initial **candidate**.
   - Set a **counter** (`times`) to 1.

2. **Traverse the array**
   - For each element:
     - If it matches the **current candidate**, increment the counter.
     - If it is different, decrement the counter.
     - If the counter becomes 0:
       - Assign the **current element as the new candidate**.
       - Reset the counter to 1.

3. **Return**
   - After one pass, the candidate left is the **majority element**.

---

## ⏱️ Complexity Analysis

| Complexity | Description |
|------------|-------------|
| **Time**  | `O(n)` — single pass through the array |
| **Space** | `O(1)` — constant extra space, no additional data structures |

---

## 📝 Notes

- This algorithm works because the majority element appears **more than n/2 times**, so it **cannot be completely canceled out**.
- No hash maps or nested loops are needed — this is **very efficient**.
- Elegant solution for majority element problems.

---
