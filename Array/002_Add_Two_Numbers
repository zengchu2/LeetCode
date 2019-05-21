#002_Add_Two_Numbers

## Question
You are given *two non-empty linked lists* representing two non-negative integers. The digits are *stored in reverse order* and each of their nodes contain a single digit. Add the two numbers and return it as a linked list.

You may assume the two numbers do not contain any leading zero, except the number 0 itself.

## My Solution
Since both string are non-empty, just ***walk through two arraies*** and sum up.
Notice that I only create the ***next*** list node on case **there are still next** or **there is still carry bit**.

## Code
···
    public ListNode addTwoNumbers(ListNode l1, ListNode l2) {
        ListNode head = new ListNode(0);
        ListNode cur = head;
        int carry = 0;
        int x, y, sum;
        while(l1 != null || l2 != null){
            x = (l1 != null) ? l1.val : 0;
            y = (l2 != null) ? l2.val : 0;
            sum = x + y + carry;
            cur.val = sum % 10;
            carry = sum / 10;
            if(l1 != null) l1 = l1.next;
            if(l2 != null) l2 = l2.next;
            if(l1 == null && l2 ==null){
                break;
            } else {
                // There is a next element.
                cur.next = new ListNode(0);
                cur = cur.next;
            }
        }
        if(carry != 0){
            cur.next = new ListNode(carry);
        }
        return head;

    }
···
