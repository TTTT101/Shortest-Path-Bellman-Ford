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

## Algorithm implemented
In Python, Bellman Ford only requires Numpy package to solve. 
1. The algorithm set the distance to source node as 0 and to all other nodes as infinity.
2. For each edge, if the distance to the source node + edge weight is less than the current distance of the destination node -> Update the distance of the destination node. Iterates N-1 times in which N is the number of nodes.
3. After N-1 iterations, check all edges

1.	Input Generation:
	•	Randomly generates coordinates for 25 nodes in a 4-dimensional space.
	•	Calculates shipping costs and two types of distances between nodes:
	•	  L1 Distance: Sum of absolute differences in each dimension.
	•	  Lmax Distance: Maximum absolute difference across dimensions.
	2.	Cost Matrix:
	•	Combines shipping costs with either L1 or Lmax distances to form a graph’s weight matrix.
	3.	Bellman-Ford Algorithm:
	•	Iteratively updates the shortest path costs from a source node to other nodes.
	•	Tracks the arcs (edges) used to achieve the minimum cost for each node.
	4.	Path Reconstruction:
	•	After determining the shortest paths, reconstructs and prints the paths between nodes.

## Results visualized
