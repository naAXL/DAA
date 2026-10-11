# Intersection of Two Linked Lists

## 1. Problem

We get the heads of two linked lists. At some point they might join and share the same nodes from there to the end. We need to return the first node where they meet. If they never meet, we return null. The lists must stay the same after we finish.

## 2. Approach

I use two pointers, a and b. a starts at headA and b starts at headB. Both move one step at a time.

- When a reaches the end of list A, I move it to the head of list B.
- When b reaches the end of list B, I move it to the head of list A.

The lists can have different lengths, but after switching, both pointers walk the same total distance (length A + length B). So they will be at the same node at the same time. If the lists meet, that node is the intersection. If they do not meet, both pointers become null together, and I return null.

## 3. Time Complexity

Time Complexity: O(m + n)

m and n are the lengths of the two lists. Each pointer walks through both lists at most one time, so the number of steps grows with m + n.

## 4. Space Complexity

Space Complexity: O(1)

I only use two pointers. I do not change the lists and I do not store any nodes.

## 5. Reflection / Improvement

Another way is to put all nodes of list A into a HashSet and then check list B against it. That is also O(m + n) time but uses O(m) extra space, so the two pointer way is better. We cannot do better than O(m + n) time because we may need to look at all the nodes.
