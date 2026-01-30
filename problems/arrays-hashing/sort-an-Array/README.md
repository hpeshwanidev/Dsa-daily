# 🔢 Sort an Array — LeetCode #912

🔗 **Problem Link:** https://leetcode.com/problems/sort-an-array/  
💡 **Difficulty:** Medium  

---

## 🧠 Approach

This solution uses the **Merge Sort algorithm**, a classic divide-and-conquer sorting technique.

### 1. Divide
- If the array has 0 or 1 element, it is already sorted.
- Split the array into two halves: `left` and `right`.

### 2. Conquer
- Recursively sort the left half.
- Recursively sort the right half.

### 3. Merge
- Merge the two sorted halves into a single sorted array.
- Compare elements from both halves and place the smaller one into the result array.
- Append remaining elements after one half is exhausted.

---

## ⏱️ Complexity Analysis

| Complexity | Description |
|----------|-------------|
| **Time** | `O(n log n)` — merge sort always divides the array into halves and merges them |
| **Space** | `O(n)` — additional arrays are used for merging |

---

## 📝 Notes

- Merge Sort is a **stable sorting algorithm**.
- Guarantees `O(n log n)` time complexity in all cases (best, average, worst).
- Suitable for large datasets where predictable performance is required.
- Uses recursion and extra memory for merging.

---

## 🧩 Key Idea

- Break the problem into smaller subproblems.
- Solve them recursively.
- Combine the results efficiently.

---
