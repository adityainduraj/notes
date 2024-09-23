- Used in problems where we need to calculate sum of subarray
- We create a prefix-sum array where each element is the sum of elements leading up to that element
- Then we use the formula $SUM[i,j]=P[j]-P[i-j]$
-  Don't always need a new array for prefix sum, we can sometimes use the input array itself for better space complexity. Example:
	```python
	def create_prefix_sum(arr):
		for i in range(1, len(arr)):
			arr[i] += arr[i-1]
		return arr
	```
- Leetcode Problems to Practice - 303, 525, 560