- Used to explore all paths or branches
- Problems:
	- Finding path between 2 nodes
	- Checking if graph contains a cycle
	- Finding a topological order in a Directed Acyclic Graph
	- Counting the number of connected components in a graph
- DFS can be implemented recursively, or iteratively using a stack
- Here is a generic approach to solve DFS related problems: 
	- Choose a starting point
	- Keep track of visited nodes to avoid cycles
	- Perform required operation
	- Explore unvisited neighbours until all nodes are visited
```python
def dfs_recursive(self, v. visited):
	visited.add(v)
	print(v, end=' ')

	for neighbour in self.grah[v]:
		if neighbour not in visited:
			self.dfs_recursive(neighbour, visited)
			
visited = set()
dfs_recursive(1, visited)
```
- [[Leetcode Practice]] - 133, 113, 210