- Level by level graph traversal
- Problems:
	- Finding shortest path between 2 nodes in an unweighted graph
	- Printing all nodes of a tree level by level
	- Finding all connected components in a graph
	- Finding shortest transformation sequence from one word to another
```python
def bfs(self, start):
	visited = set()
	queue = deque([start])

	visited.add(start)

	while queue:
		vertex = queue.popleft()
		print(vertex, end = ' ')

		for neighbour in self.graph[vertex]:
			if neighbour not in visited:
				visited.add(neighbour)
				queue.append(neighbour)
```
- Approach Explained:
	- Add starting node to the queue
	- Set up a visited set, continue as long as the queue is not empty
	- Dequeue a node and process it
	- Enqueue unvisited neighbours
	-  Add processed nodes to the visited set
	- Continue till empty
- [[Leetcode Practice]] - 102, 994, 127