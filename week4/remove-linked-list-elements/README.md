# Remove Linked List Elements

## 1. Problem

We get a linked list and a number val. We need to remove every node that has this value, and return the new head of the list.

## 2. Approach

The head node can also be removed, which makes it tricky. To solve this I make a dummy node and put it before the head. Then I use a pointer cur that starts at the dummy.

- If the next node has the value val, I skip it by pointing cur.next to cur.next.next.
- If not, I move cur forward.

When I reach the end, I return dummy.next, which is the new head.

## 3. Time Complexity

Time Complexity: O(n)

Each step either removes a node or moves forward one node. We never go back, so we visit every node one time.

## 4. Space Complexity

Space Complexity: O(1)

I only use a dummy node and one pointer. No extra space that depends on the size of the list.

## 5. Reflection / Improvement

We must check every node, so O(n) time is already the best. We could also solve it without a dummy node by first moving the head forward while it has the value val, but then we need extra code for the head. The dummy node makes it shorter and simpler.
