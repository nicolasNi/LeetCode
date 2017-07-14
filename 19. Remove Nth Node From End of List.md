Given a linked list, remove the nth node from the end of list and return its head.

For example,

>   Given linked list: **1->2->3->4->5**, and **n = 2**.

>   After removing the second node from the end, the linked list becomes **1->2->3->5**.

**Note:**

Given n will always be valid.

Try to do this in one pass.


```java
/**
 * Definition for singly-linked list.
 * public class ListNode {
 *     int val;
 *     ListNode next;
 *     ListNode(int x) { val = x; }
 * }
 */
public class Solution {
    public ListNode removeNthFromEnd(ListNode head, int n) {
        if(head == null || n < 1)
            return null;
        ListNode first = head, second = head;
        for(int i = 1; i < n; i++){
            if(first == null)
                return null;
            first = first.next;
        }
        if(first.next != null){
            while(first.next.next != null){
                first = first.next;
                second = second.next;
            }
            second.next = second.next.next;
            return head;
        }else{
            return head.next;
        }
    }
}
```
