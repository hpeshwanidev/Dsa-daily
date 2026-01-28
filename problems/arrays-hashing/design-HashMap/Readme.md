# 🗺️ Design HashMap — LeetCode #706

🔗 **Problem Link:** https://leetcode.com/problems/design-hashmap/  
💡 **Difficulty:** Easy  

---

## 🧠 Approach

This solution implements a **basic HashMap using separate chaining**:

1. **Buckets**
   - Use a list of lists (`buckets`) to store key-value pairs.
   - Each bucket stores multiple `Pair` objects (key-value) to handle collisions.
   - Initialize **10,000 buckets** to reduce collisions.

2. **Hash Function**
   - Use `key % 10000` to determine which bucket a key belongs to.

3. **Put**
   - Calculate the bucket index for the key.
   - If the key already exists in the bucket, **update its value**.
   - Otherwise, **add a new key-value pair** to the bucket.

4. **Get**
   - Calculate the bucket index.
   - Search the bucket for the key.
   - Return its value if found, otherwise return `-1`.

5. **Remove**
   - Calculate the bucket index.
   - Iterate over the bucket and remove the `Pair` if the key matches.

---

## ⏱️ Complexity Analysis

| Operation | Average Time Complexity | Worst-case Time Complexity | Space Complexity |
|-----------|-----------------------|---------------------------|----------------|
| `put`     | O(n/b)                | O(n)                      | O(n)           |
| `get`     | O(n/b)                | O(n)                      | O(n)           |
| `remove`  | O(n/b)                | O(n)                      | O(n)           |

> **n** = total number of key-value pairs  
> **b** = number of buckets (10,000 in this implementation)  

- Average-case complexity is close to **O(1)** per operation, assuming keys are distributed evenly.

---

## 📝 Notes

- This implementation does **not use Java’s built-in HashMap**.
- Uses **separate chaining** (a list per bucket) to handle hash collisions.
- The `Pair` class stores the key and value together.
- Iterators are used during removal to safely delete elements from a bucket.
- Efficient for a wide range of integer keys.

---

## 🔧 Example Usage

```java
MyHashMap map = new MyHashMap();
map.put(1, 100);
map.put(2, 200);
map.get(1); // returns 100
map.remove(2);
map.get(2); // returns -1
