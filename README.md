# LeetcodeProblem
**给你两个 非空 的链表，表示两个非负的整数。
 * 它们每位数字都是按照 逆序 的方式存储的，并且每个节点只能存储 一位 数字。
 请你将两个数相加，并以相同形式返回一个表示和的链表。
 你可以假设除了数字 0 之外，这两个数都不会以 0 开头。
 * @author TT
 * @create 2022/3/16 3:30 下午
 */
 
 public class Solution1 {
          public ListNode addTwoNumbers ( ListNode l1 , ListNode l2 ) {
                    int a = 0;
                    ListNode head = new ListNode ( );
                    ListNode pre = head;
                    while ( l1 != null || l2 != null || a!= 0) {
                              if ( l1 != null ) {
                                        a += l1.val;
                                        l1 = l1.next;
                              }

                              if ( l2 != null ) {
                                        a += l2.val;
                                        l2 = l2.next;
                              }

                              pre.val = a % 10;
                              a /= 10;

                              if ( l1 != null || l2 != null || a!=0) {
                                        pre.next = new ListNode ( 0 );
                                        pre = pre.next;
                              }

                    }


                    return head;
          }


//          public static void main ( String[] args ) {
//                    ListNode l1 = new ListNode ( 9 );
//                    ListNode l2 = new ListNode ( 1 );
//                    l2.next = new ListNode ( 9 );
//                    l2.next.next = new ListNode ( 9 );
//                    l2.next.next.next = new ListNode ( 9 );
//                    l2.next.next.next.next = new ListNode ( 9 );
//                    l2.next.next.next.next.next = new ListNode ( 9 );
//                    l2.next.next.next.next.next.next = new ListNode ( 9 );
//                    l2.next.next.next.next.next.next.next = new ListNode ( 9 );
//
//
//                    Solution1 solution1 = new Solution1 ( );
//                    solution1.addTwoNumbers ( l1,l2 );


}
