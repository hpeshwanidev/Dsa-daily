# 🔑 Design HashSet — LeetCode #705

🔗 **Problem Link:** https://leetcode.com/problems/design-hashset/  
💡 **Difficulty:** Easy  

---

## 🧠 Approach

This solution implements a **simple HashSet using separate chaining**:

1. **Buckets**
   - Use a list of lists (`buckets`) to store elements.
   - Each bucket handles a set of keys that hash to the same index.
   - Initialize **10,000 buckets** to reduce collisions.

2. **Hash Function**
   - Use `key % 10000` to determine the bucket index for a key.

3. **Add**
   - Calculate the bucket index for the key.
   - If the key is not already in the bucket, add it.

4. **Remove**
   - Calculate the bucket index.
   - If the key exists in the bucket, remove it.

5. **Contains**
   - Calculate the bucket index.
   - Return true if the key exists in the bucket, otherwise false.

---

## ⏱️ Complexity Analysis

| Operation | Time Complexity | Space Complexity |
|-----------|----------------|----------------|
| `add`     | O(n/b) on average, O(n) worst case | O(n) |
| `remove`  | O(n/b) on average, O(n) worst case | O(n) |
| `contains`| O(n/b) on average, O(n) worst case | O(n) |

> **n** = number of elements in the set  
> **b** = number of buckets (10,000 in this implementation)  

- Average-case complexity is close to O(1) per operation because the hash distributes keys evenly.

---

## 📝 Notes

- This is a **basic HashSet implementation** using **chaining** to handle collisions.
- No built-in `HashSet` is used — everything is implemented manually.
- The `Integer.valueOf(key)` is used to remove the object instead of the index when removing elements from the bucket.
- Efficient for moderate key ranges and reduces collisions using many buckets.

---