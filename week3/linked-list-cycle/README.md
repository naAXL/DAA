# Linked List Cycle

## 1. Problem

We get the head of a linked list. We need to check if the list has a cycle, which means some node can be reached again if we keep following the next pointers. We return true if there is a cycle, and false if not.

## 2. Approach

I use two pointers, slow and fast, that both start at the head.

- slow moves one step at a time.
- fast moves two steps at a time.

If the list has no cycle, fast will reach the end (null) and I return false. If the list has a cycle, fast will go around the loop and eventually catch up to slow, so they will meet at the same node, and I return true.

## 3. Time Complexity

Time Complexity: O(n)

If there is no cycle, fast reaches the end after about n / 2 steps. If there is a cycle, fast catches slow after going around the loop a small number of times. Either way the number of steps grows with n.

## 4. Space Complexity

Space Complexity: O(1)

I only use two pointers, slow and fast. I do not store the nodes anywhere, so the space does not grow with the size of the list.

## 5. Reflection / Improvement

Another way is to save every visited node in a HashSet and check if we see the same node again. That is also O(n) time, but it uses O(n) extra space, so the two pointer way is better. We cannot go faster than O(n) time because we may need to look at every node.
