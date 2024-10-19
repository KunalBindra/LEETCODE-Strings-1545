# LEETCODE-Strings-1545
### Step 1: First Call
- **Input:** `n = 3`, `k = 5`
- **Base Case:** Since `n != 1`, the base case is not triggered.
- Calculate `midIndex = 2^(3-1) = 4`.
- Since `k = 5 > midIndex = 4`, the next call is `findKthBit(n-1, midIndex * 2 - k)`:
  - `findKthBit(2, 4 * 2 - 5) = findKthBit(2, 3)`

### Step 2: Second Call
- **Input:** `n = 2`, `k = 3`
- **Base Case:** Since `n != 1`, the base case is not triggered.
- Calculate `midIndex = 2^(2-1) = 2`.
- Since `k = 3 > midIndex = 2`, the next call is `findKthBit(n-1, midIndex * 2 - k)`:
  - `findKthBit(1, 2 * 2 - 3) = findKthBit(1, 1)`

### Step 3: Third Call
- **Input:** `n = 1`, `k = 1`
- **Base Case:** Since `n = 1`, return `'0'`.

### Step 4: Returning Values
- From Step 3, return `'0'` to Step 2.
- In Step 2, since the return value is `'0'`, invert it to `'1'` and return `'1'` to Step 1.
- In Step 1, since the return value is `'1'`, invert it to `'0'` and return `'0'`.

### Final Result: The k-th bit for `n = 3` and `k = 5` is `'0'`.

This dry run shows that the code correctly computes the k-th bit in a recursive manner by dividing the problem into smaller sub-problems based on the middle index.
