class Solution {
    public ListNode reverseList(ListNode head) {
        Stack<Integer> s = new Stack<>();
        while(head != null){
            s.push(head.val);
            head = head.next;
        }

        ListNode dummy = new ListNode(99);
        ListNode res = dummy;
        while(!s.isEmpty()){
            ListNode ptr = new ListNode(s.pop());
            dummy.next = ptr;
            dummy = dummy.next;
        }
        return res.next;
    }
}
