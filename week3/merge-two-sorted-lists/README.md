# Merge Two Sorted Lists

## 1. Problem

We get two linked lists that are already sorted from small to big. We need to join them into one sorted list and return its head. We must reuse the nodes from the two lists, not make new ones.

## 2. Approach

I make a dummy node to start the new list, and a pointer called tail that always points to the last node of the new list.

- I compare the first nodes of both lists.
- The smaller one gets attached to tail, and I move forward in that list.
- I move tail forward too.

I repeat this until one list is empty. Then I attach the rest of the other list to the end, because it is already sorted. At the end I return dummy.next, which is the head of the merged list.

## 3. Time Complexity

Time Complexity: O(n + m)

n and m are the lengths of the two lists. Each step moves forward one node in one of the lists, and we never go back. So in the worst case we visit every node one time.

## 4. Space Complexity

Space Complexity: O(1)

I only use a few pointers and one dummy node. I do not create new nodes for the values, I just reconnect the old ones, so the space does not grow with the input.

## 5. Reflection / Improvement

We have to look at every node at least once, so O(n + m) time is already the best we can do. Another way is to use recursion, but it would use extra space for the calls, so the loop version is better.
