Merge two sorted linked lists and return it as a new list. The new list should be made by splicing together the nodes of the first two lists.

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
    public ListNode mergeTwoLists(ListNode l1, ListNode l2) {
        if(l1 == null)
            return l2;
        if(l2 == null)
            return l1;
        ListNode dummy = new ListNode(-1), result = dummy;
        while(l1 != null || l2 != null){
            if(l1 == null){
                dummy.next = l2;
                l2 = l2.next;
            }else if(l2 == null)
            {
                dummy.next = l1;
                l1 = l1.next;
            }else{
                if(l1.val <= l2.val){
                    dummy.next = l1;
                    l1 = l1.next;
                } 
                else{
                    dummy.next = l2;     
                    l2 = l2.next;
                }
            }
            dummy = dummy.next;
            
        }
        return result.next;
    }
}
```
