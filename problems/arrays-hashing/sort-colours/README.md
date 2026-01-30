# 🎨 Sort Colors — LeetCode #75

🔗 **Problem Link:** https://leetcode.com/problems/sort-colors/  
💡 **Difficulty:** Medium  

---

## 🧠 Approach

This solution uses a **simple comparison-based sorting approach** (similar to Bubble Sort / Selection Sort):

1. **Iterate through the array**
   - Use two nested loops to compare elements pairwise.
   
2. **Swap elements**
   - If an element is greater than a subsequent element, swap them.
   
3. **Continue until the array is sorted**
   - After all comparisons and swaps, the array will be sorted in-place.

---

## ⏱️ Complexity Analysis

| Complexity | Description |
|-----------|-------------|
| **Time**  | O(n²) — due to nested loops over the array |
| **Space** | O(1) — sorting is done in-place |

---

## 📝 Notes

- This algorithm **sorts the array in-place** without using extra space.
- It is **not the most efficient approach** for the Sort Colors problem.  
  The optimal solution uses the **Dutch National Flag algorithm** with a **single pass** and O(n) time.
- Works correctly for small arrays or when simplicity is more important than performance.

---

## 🔧 Example Usage

```java
int[] colors = {2,0,2,1,1,0};
new Solution().sortColors(colors);
// colors is now [0,0,1,1,2,2]