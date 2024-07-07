---
title: Load Balancing Across Servers
subtitle: Load balancing is an important component in managing server resources efficiently within large-scale infrastructures like Netflix's content delivery network (CDN). It involves distributing incoming network traffic across multiple servers to ensure optimal resource utilization, maximize throughput, and minimize response times. In the context of Netflix, which serves millions of users globally, effective load balancing is essential for maintaining high availability, scalability, and delivering seamless streaming experiences.


caption:
  title: Load Balancing Across Servers
  thumbnail: assets/img/portfolio/GSLB-003.png
---

**Design Techniques**

_**1.Dijkstra's Algorithm**_
Dijkstra's algorithm is primarily used for finding the shortest path in a graph with non-negative edge weights.Dijkstra's algorithm can help optimize network routes by finding the shortest path between servers or nodes, minimizing latency and maximizing data transfer efficiency.It can assist in determining the best routes for traffic based on factors such as current network conditions, server capacities, and geographic proximity.

Dijkstra's algorithm has a time complexity of O((V + E) log V) with a binary heap, where V is the number of nodes (servers) and E is the number of edges (connections). This can become computationally intensive for large-scale CDN infrastructures with numerous servers and dynamic traffic patterns.CDN environments are dynamic, with constantly changing traffic patterns and server loads. Dijkstra's algorithm assumes static edge weights, making it less suitable for adapting to real-time changes in network conditions and load balancing requirements.

_**2.Assignment Problem:**_
The assignment problem is a classic problem in operations research and combinatorial optimization that deals with assigning a set of tasks to a set of workers in a way that minimizes the overall cost or maximizes the overall profit.It can be used for optimizing resource allocation by assigning tasks based on factors like server capacity, workload, and task requirements, thereby balancing load and maximizing resource utilization.And,assigning incoming requests to servers that can process them most efficiently, considering factors such as server availability, response time, and geographic proximity to users.

**Complexity analysis and codes**

**_Dijkstra's Algorithm_**

Time complexity: O((V + E) log V), where V is the number of vertices and E is the number of edges.

Auxiliary Space: O(V), where V is the number of vertices and E is the number of edges in the graph.

[Code](https://github.com/PAI-SHREYA/DSA/blob/main/Graph%20Traversal/dijekstra.c)

**_Assignment Problem_**

Time complexity : O(n^3), where n is the number of workers and jobs. 

Space complexity :  O(n^2).

[Code](https://github.com/PAI-SHREYA/DSA/blob/main/Dynamic%20Programming/assignment.cpp)








