- Uses a stack to find the next greater or next smaller element in an array
- Use stack to track indices of elements for which we have not found next greatest element
- Initialize the result array with -1s
- For each element, check if its greater than the element at the top of the stack. 
- If it is, pop that element and push the index of new greater element onto the stack. 
- If it is not, then just push index of new element onto the stack
```python
def next_greater_element(arr):
	n = len(arr)
	stack = []
	result = [-1] * n

	for i in range(n):
		while stack and arr[i] > arr[stack[-1]]:
			result[stack.pop()] = arr[i]
		stack.append(i)

	return result
```
- [[Leetcode Practice]] - 496, 739, 84