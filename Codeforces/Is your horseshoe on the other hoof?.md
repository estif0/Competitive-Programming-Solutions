# Solution to [Is your horseshoe on the other hoof?](https://codeforces.com/contest/228/problem/A)

---

## Problem Details
- **Platform**: Codeforces
- **Difficulty**: Easy

---

## Solution Overview
### General Overview
The problem is to find the minimum number of horseshoes Valera needs to buy in order to have four horseshoes of different colors.

### Detailed Step-by-Step Solution
1. **Step 1**: Take four horseshoes as input.
2. **Step 2**: Create a set from the four horseshoes.
3. **Step 3**: Return the difference between the size of the set and 4.


---

## Complexity Analysis
- **Time Complexity**: O(1)
  - The time complexity is constant because we are only performing a single set operation.
- **Space Complexity**: O(1)
  - The space complexity is constant because we are only storing four horseshoes in a set.

---

## Code Implementation
```python
arr = [int(i) for i in input().split()]
print(4-len(set(arr)))
```

---
