# Binary Search

## 1. Problem

We get a list of numbers that is already sorted from small to big, and a target number. We need to find the target in the list and return its index. If it is not in the list, we return -1. We need to do this fast, in O(log n) time.

## 2. Approach

I use two pointers, lo at the start and hi at the end of the list. I keep checking the middle number.

- If the middle number is the target, I return that index.
- If the middle number is smaller than the target, I move lo to look on the right side.
- If the middle number is bigger than the target, I move hi to look on the left side.

I keep doing this until I find the target or there is nothing left to check. If I never find it, I return -1.

## 3. Time Complexity

Time Complexity: O(log n)

Every time I check the middle, I throw away half of the list. So the list gets small very fast, and I need fewer steps each time.

## 4. Space Complexity

Space Complexity: O(1)

I only use a few variables (lo, hi, mid). I do not use any extra list or array, so the space does not grow with the input.

## 5. Reflection / Improvement

This is already a fast and simple way to solve the problem. I do not think there is a much better way for a normal sorted list. If the numbers were spread out evenly, there is something called interpolation search, but it is more complex and not always faster.
