# Shortest-Path-Bellman-Ford
Performing the shortest path using Bellman Ford algorithim to compute the distance between nodes. In this case, we minimize cost (shortest cost path) which is the sum of a shipping cost matrix and the distance matrix.

_Requirements:_

(1) Find the shortest path from each node to the node 24th. Consider the l1 norm to compute the distances between nodes (l1(x − y) = ∑4i=1 |xi − yi|where x and y have 4 dimensions)

(2) Find the shortest path from node  0 to each node. Consider the l∞ norm to compute the distances between nodes (l∞(x − y) = maxi=1,...,4[|xi − yi|] where x and y have 4 dimensions).

_*Details on the norms used to compute distances in https://en.wikipedia.org/wiki/Norm (mathematics)_

End result is the optimal shortest path between any two nodes - minimizing total shipping cost.

## Data description
Using numpy random seed to genrate the data frame that contain 25 nodes and 4 dimemsions. Each node randomly coordinates from 0 to 50.

## Visual network design 
![image](https://github.com/user-attachments/assets/76b03328-36e3-4874-9369-95f029021460)

## Algorithm implemented

In Python, Bellman Ford only requires Numpy package to solve. The l1_distances and lmax_distances matrices are calculated based on differences between coordinates. And the Cost Matrix combines shipping costs with either L1 or Lmax distances to form a graph’s weight matrix.

	•	  L1 Distance: Sum of absolute differences in each dimension.
	•	  Lmax Distance: Maximum absolute difference across dimensions.
	
 1. Bellman-Ford Algorithm:
	•	Iteratively updates the shortest path costs from a source node to other nodes.
	•	Tracks the arcs (edges) used to achieve the minimum cost for each node.
	
 2. Path Reconstruction:
	•	Tracks the arcs used for minimum cost
	•	After determining the shortest paths, reconstructs and prints the shortest path for each node:

## Results visualized
