# Solution to [Check if an array is sorted](https://www.geeksforgeeks.org/problems/check-if-an-array-is-sorted0701/1)

---

## Problem Details
**Platform**: GeeksForGeeks  
**Difficulty**: Easy  
---

## Solution Overview
### General Overview
The problem is to check if the given array is sorted or not. The main idea is to traverse the array and check if each element is greater than the previous one.

### Detailed Step-by-Step Solution
1. **Step 1**: We traverse the array from the first element to the second last element.
2. **Step 2**: For each element, we check if it is greater than the next element.
3. **Step 3**: If the condition is true, then we return true else false.

> **Example**: If the array is [1, 2, 3, 4, 5], then the output will be true because each element is greater than the previous one.

---

## Complexity Analysis
- **Time Complexity**: O(n)
  - *The time complexity is linear because we are traversing the array only once.*
- **Space Complexity**: O(1)
  - *The space complexity is constant because we are not using any extra space.*

---

## Code Implementation
```python
class Solution:
    def arraySortedOrNot(self, arr) -> bool:
        n= len(arr)
        if n==1:
            return True
        left, right=0,1
        while right<n:
            if arr[left]>arr[right]:
                return False
            left+=1
            right+=1
        return True
```
---

## Test Cases
```python
arr = [1, 2, 3, 4, 5]
print(Solution().arraySortedOrNot(arr))  # Output: True

arr = [5, 4, 3, 2, 1]
print(Solution().arraySortedOrNot(arr))  # Output: False
```

---

## Additional Notes
- **Common Pitfalls**: A common mistake is assuming an array with repeating elements in non-decreasing order is unsorted. Also, consider edge cases like arrays with only one element or already sorted arrays.
- **Useful Snippets/Information**: The traversal pattern used in this solution can be reused in problems that require comparing adjacent elements.
- **Related Problems**: For more practice, try similar problems on LeetCode, such as "Check If Array Is Sorted and Rotated" (LeetCode 1752).
