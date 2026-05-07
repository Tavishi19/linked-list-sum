# linked-list-sum
class ListNode:

 def addtwonumbers(l1,l2):

    dummy = ListNode (0)
    current = dummy
    carry = 0

    while l1 or l2 or carry:
         val1 = l1.val if l1 else 0
         val2 = l2.val if l2 else 0

         total = val1 + val2 + carry

         digit = total % 10
         carry = total // 10

         current.next = ListNode(digit)
         current = current.next 

         if l1:
             l1 = l1.next
         if l2:
            l2 = l2.next

    return dummy.next 


# first I defined a class listnode to create a linked list;
# then defined a function to add two numbers whose value is stores as linked lists;
# then created a dummy node to get a starting point and a current node which is a pointer that moves forward helping to build the list;
# then created a variable carry to store the carry value;
# used a while loop to go through the lists until both are fully scanned ;
# used if statements to get cureent value from each list;
# then calculated the toal ;
# this calculated the digit to be stored in current node and then move to the next;
# then returned the next of dummy node 
# there is no print statement or input statement because this is a function only which explain the logic assuming the input would be provided 
