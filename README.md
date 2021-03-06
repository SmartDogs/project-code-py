# Leetcode Solutions using AI
GPT-2 Model for Leetcode Questions in python 

Note: the Answers might not make sense in some cases 
#### Demo

https://share.streamlit.io/gagan3012/project-code-py/app.py

#### Model

```
from transformers import AutoTokenizer, AutoModelWithLMHead

tokenizer = AutoTokenizer.from_pretrained("gagan3012/project-code-py")

model = AutoModelWithLMHead.from_pretrained("gagan3012/project-code-py")
```

#### Question:

```
Write a function to delete a node in a singly-linked list. You will not be given access to the head of the list, instead you will be given access to the node to be deleted directly. It is guaranteed that the node to be deleted is not a tail node in the list.
```

#### Answer:

```
""" Write a function to delete a node in a singly-linked list. You will not be given access to the head of the list, instead you will be given access to the node to be deleted directly. It is guaranteed that the node to be deleted is not a tail node in the list.

For example,
a = 1->2->3
b = 3->1->2
t = ListNode(-1, 1)

Note: The lexicographic ordering of the nodes in a tree matters. Do not assign values to nodes in a tree.
Example 1:

Input: [1,2,3]
Output: 1->2->5
Explanation: 1->2->3->3->4, then 1->2->5[2] and then 5->1->3->4.


Note:

The length of a linked list will be in the range [1, 1000].
Node.val must be a valid LinkedListNode type.
Both the length and the value of the nodes in a linked list will be in the range [-1000, 1000].
All nodes are distinct.
"""
# Definition for singly-linked list.
# class ListNode:
#     def __init__(self, x):
#         self.val = x
#         self.next = None

class Solution:
    def deleteNode(self, head: ListNode, val: int) -> None:
        """
        BFS
        Linked List
        :param head: ListNode
        :param val: int
        :return: ListNode
        """
        if head is not None:
            return head
        dummy = ListNode(-1, 1)
        dummy.next = head
        dummy.next.val = val
        dummy.next.next = head
        dummy.val = ""


s1 = Solution()
print(s1.deleteNode(head))
print(s1.deleteNode(-1))
print(s1.deleteNode(-1))

   ```
