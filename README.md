# LeetCode – Add Two Numbers

## Problem

Given two non-empty linked lists representing two non-negative integers, add the two numbers and return the sum as a linked list.

The digits are stored in **reverse order**.

### Example

```text
Input:
l1 = [2,4,3]
l2 = [5,6,4]

Output:
[7,0,8]
```

Because:

```text
342 + 465 = 807
```

## Approach

We traverse both linked lists at the same time and add their values.

* Add the current digits and the `carry`.
* Store the last digit of the sum in a new node.
* Pass the remaining value as `carry`.
* Continue until both lists and the carry are finished.
* Use a dummy node to easily build the result list.

## Algorithm

1. Create a dummy node.
2. Set `carry = 0`.
3. Traverse both linked lists.
4. Calculate:

   ```text
   sum = x + y + carry
   ```
5. Calculate the new carry:

   ```text
   carry = sum / 10
   ```
6. Create a new node using:

   ```text
   sum % 10
   ```
7. Move to the next nodes.
8. Return `dummy.next`.

## Complexity

* **Time Complexity:** O(max(n, m))
* **Space Complexity:** O(max(n, m))

## Language

**Java**

## LeetCode

Problem #2 — Add Two Numbers
