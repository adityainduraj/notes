- Used for problems like:
	- Searching in a nearly sorted array
	- Searching in a rotated sorting array
	- Searching in a list with unknown length
	- Searching in an array with duplicates
	- Finding the first or last occurence of an element
	- Finding the square root of a number
	- Finding a peak element
- Example - Searching in a Rotated Sorting Array
	- We use normal binary search with an additional check
	- We check which half is sorted, then check if element is in range of that sorted half, and then we search in that half
```python
def search_rotated_array(nums, target):
	left, right = 0, len(nums)-1

	while left <= right:
		mid = (left + right) // 2

		if nums[mid] == target:
			return mid
		if nums[left] <= nums[mid]:
			## this is the additional check
			if nums[left] <= target < nums[mid]:
				right = mid - 1
			else:
				left = mid + 1
		else:
			if nums[mid] < target <= nums[right]:
				left = mid + 1
			else:
				right = mid - 1

	return -1
```
- [[Leetcode Practice]] - 33, 153, 240