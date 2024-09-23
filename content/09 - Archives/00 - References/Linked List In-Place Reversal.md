- Consider the example of reversing a linked list
- Use 3 pointers, *previous*, *current* and *next* 
- Set *previous* to null, set *current* to head of the linked list
- Use a while loop to go through the list till *current* is null
- Set *next* to node after *current* 
- Then reverse pointer so that *current* points to *previous*. Then move *previous* to *current* and *current* to *next*. 
- Example Code:
	```python
	def reverse_linked_list(head):
		prev = None
		current = head
	
		while current is not None:
			next = current.next
			current.next = prev
			prev = current
			current = next
	
		return prev ## head of reversed linked list
	```
- [[Leetcode Practice]] - 206, 92, 24