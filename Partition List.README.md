class Solution {
    public ListNode partition(ListNode head, int x) {
       ListNode lesserList = new ListNode(99);
       ListNode greaterList = new ListNode(99);
       ListNode sptr = lesserList;
       ListNode gptr = greaterList;

       while(head != null){
        if(head.val < x){
            sptr.next = head;
            sptr = sptr.next;
        }
        else{
            gptr.next = head;
            gptr = gptr.next;
        }
        head = head.next;
       }
       gptr.next = null;
       sptr.next = greaterList.next;
       return lesserList.next;
    }
}
