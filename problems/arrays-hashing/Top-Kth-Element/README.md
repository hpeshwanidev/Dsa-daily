# 📊 Top K Frequent Elements — LeetCode #347

🔗 **[View Problem](https://leetcode.com/problems/top-k-frequent-elements/)**  
💡 **Difficulty:** Medium  

---

## 🧠 Approach

1. Use a `HashMap` to count the frequency of each number in the array.
2. Extract the unique elements using `map.keySet()` and store them in an `ArrayList`.
3. Sort the list based on the frequency of each element in descending order using a custom comparator.
4. Take the first `k` elements from the sorted list as the most frequent elements.
5. Return them as an array.

---

## ⏱️ Complexity Analysis

| Complexity | Description |
|-----------|-------------|
| **Time**  | O(n log n) — sorting unique elements |
| **Space** | O(n) — hashmap and list storage |

---
