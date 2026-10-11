# Remove Duplicates from Sorted List

## 1. Problem

We get a linked list that is already sorted. Some numbers show up more than once. We need to remove the repeated ones so every number appears only one time, and return the list.

## 2. Approach

Because the list is sorted, the same numbers are always next to each other. I use one pointer called cur and start at the head.

- If cur and the next node have the same value, I skip the next node by pointing cur.next to cur.next.next.
- If they are different, I move cur forward.

I keep going until there is no next node. Then I return the head.

## 3. Time Complexity

Time Complexity: O(n)

Each step either removes a node or moves forward one node. We never go back, so we look at every node at most one time.

## 4. Space Complexity

Space Complexity: O(1)

I only use one pointer. I do not make a new list or use a set, so the space does not grow with the input.

## 5. Reflection / Improvement

We have to look at every node at least once, so O(n) is already the best time. Another way is to use a HashSet to remember seen numbers, but that uses O(n) extra space and is not needed because the list is sorted.
