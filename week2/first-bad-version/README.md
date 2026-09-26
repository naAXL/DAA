# First Bad Version

## 1. Problem

There are versions numbered 1 to n. At some point, versions start being bad, and every version after that is also bad. We get a function isBadVersion(version) to check if a version is bad. We need to find the first bad version using as few checks as we can.

## 2. Approach

I use binary search on the version numbers. I keep a lo and hi range, starting from 1 and n.

- I check the middle version.
- If it is bad, the first bad version is this one or an earlier one, so I move hi down to mid.
- If it is not bad, the first bad version must come later, so I move lo up to mid + 1.

I keep doing this until lo and hi are the same number. That number is the first bad version.

## 3. Time Complexity

Time Complexity: O(log n)

Each check cuts the range of versions in half. So I need fewer checks as the range gets smaller, which gives log n instead of n.

## 4. Space Complexity

Space Complexity: O(1)

I only use a few number variables (lo, hi, mid). No extra memory is used that depends on the size of n.

## 5. Reflection / Improvement

This is already a fast solution with few checks. I do not think there is a better way in the worst case. If bad versions usually show up early, checking early numbers first might help sometimes, but it would not be better in the worst case.
