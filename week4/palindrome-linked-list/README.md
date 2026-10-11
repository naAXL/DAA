# Palindrome Linked List

## 1. Problem

We get a linked list. We need to check if it reads the same from front to back and from back to front. If yes we return true, if not we return false.

## 2. Approach

We cannot go backwards in a singly linked list, so I reverse the second half and compare it with the first half.

- I use slow and fast pointers to find the middle. slow moves one step and fast moves two steps. When fast reaches the end, slow is at the middle.
- I reverse the list starting from slow.
- I compare the first half (from head) with the reversed half, node by node.

If any values are different I return false. If all of them match, I return true.

## 3. Time Complexity

Time Complexity: O(n)

Finding the middle takes about n / 2 steps, reversing the second half takes about n / 2 steps, and comparing takes about n / 2 steps. All of these add up to a number that grows with n.

## 4. Space Complexity

Space Complexity: O(1)

I reverse the nodes in place and only use a few pointers. I do not copy the list into an array, so the extra space does not grow with n.

## 5. Reflection / Improvement

An easier way is to copy all values into an array and check it from both ends. It is also O(n) time but uses O(n) extra space. The method I used meets the follow up (O(n) time and O(1) space). One small thing is that my solution leaves the second half reversed. If the list must stay the same, I could reverse the second half again after comparing.
