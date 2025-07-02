# LeetCode: Remove Linked List Elements

🔗 **Problem Link:**  
[Remove Linked List Elements](https://leetcode.com/problems/remove-linked-list-elements/?envType=problem-list-v2&envId=linked-list)

##  Problem Summary
Given the `head` of a singly linked list and an integer `val`, remove all the nodes of the linked list that have `val` as their value and return the new head.

##  Approach
To handle edge cases like removing the head node, we use a **dummy node** that points to the head of the list. We then use a pointer `current` starting at the dummy node and traverse the list. At each step:

- If `current.next.val == val`, we skip the node by updating `current.next = current.next.next`
- Otherwise, we move forward with `current = current.next`

This allows us to safely remove any node, including the head, without special handling.

##  Why Use a Dummy Node?
The dummy node simplifies edge cases (like removing the head) by ensuring there’s always a node before the node we might remove.

##  Time and Space Complexity
- **Time:** O(n), where n is the number of nodes in the list  
- **Space:** O(1), no extra space is used apart from a few pointers

##  Example
Input:
head = [1,2,6,3,4,5,6], val = 6
Output:
[1,2,3,4,5]
