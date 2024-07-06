---
title: User Activity Analysis
subtitle: Netflix aims to improve its user experience by analyzing real-time user engagement metrics such as the number of views, churn rates, or total watch time over specific periods. By monitoring these metrics, Netflix identifys trends that help in content acquisition and production decisions. 


caption:
  title: User Activity Analysis
  thumbnail: assets/img/portfolio/Tiny-PNG-The_Secret_Game_Changer_Social_Media_Customer_Engagement_.png
---
**Challenges and Market Benefits:**

**Design Technique:**

**_1.Kadane's Algorithm_**:Kadane's Algorithm is used to find the maximum sum subarray within a one-dimensional array of numbers. In this case, this can be used to find the period of maximum user engagement by analyzing time-series data of user interactions, such as views or likes.Let's consider a scenario where we want to analyze user activity to identify binge-watching patterns and detect the longest streaks of continuous viewing activity by each user.
In the below graph,Kadane's algorithm is implemented to find the maximum sum of a contiguous subarray within a user's viewing activity data. It iterates through the array, maintaining two variables: max_ending_here (current subarray sum) and max_so_far (maximum sum found so far). By updating these variables dynamically, Kadane's algorithm identifies the longest streak of continuous viewing activity.
<img src="assets/img/inside/2_graph.png" alt="Kadane Graph">
However,Kadane's Algorithm is limited to finding the maximum sum in a one-dimensional array and does not directly support complex queries or dynamic updates. It is best suited for scenarios where the primary goal is to identify peak engagement periods in a straightforward manner. 

**_2.DFS and BFS:_**
DFS and BFS can be used to analyze user interactions to detect patterns, preferences, and potential issues by traversing user interaction graphs.DFS can be used to explore user interaction sequences , identifying binge-watching patterns. DFS can reveal if a user consistently watches multiple episodes of a series in one sitting, highlighting binge-watching behavior.BFS can be used to analyze user behavior at each level, tracking how users discover new content and interact with the platform.
The below image gives a basic implementation and graph traversal.
<img src="assets/img/inside/2_traversal.png" alt="KDFSGraph">
**_Inferences_:**
-Nodes represent Netflix content and users, edges represent interactions with weights indicating intensity.
-Based on the graph visualization and interaction weights, "Stranger Things" (M1) and "Money Heist" (M3) appear to be popular among users (User1 and User3 respectively), as they have higher interaction weights (watching and likes).
-The DFS and BFS traversal results show the sequence of interactions and exploration paths starting from User1, revealing how users may discover new content or engage with related items based on their initial interactions.

_**3.Union-Find  and Root Method:**_
This method can be used to detect connected components in user behavior data.Union-Find method can be used to identify clusters of users with similar behaviors, enabling personalized marketing strategies. The root method helps in quickly finding and merging these clusters, ensuring efficient user segmentation.


**Complexity Analysis and Codes**
- _**Kadanes's Algorithm**_:
  
  Construction: O(n log n) 
  
  Update (Point Update): O(log n) 
  
  Query (Prefix Sum): O(log n)
  
  Space Complexity: O(n)
  
  [Code](https://github.com/PAI-SHREYA/DSA/blob/main/Trees/FenwickTree.cpp)
- _**DFS**_:
  
  Access, search, insertion, and deletion: O(log n),where n is the number of data points.
  
  Space complexity: O(n)
  
  [Code](https://github.com/PAI-SHREYA/DSA/blob/main/Trees/KD_Tree.cpp)

  - _**BFS**_:
  
  Access, search, insertion, and deletion: O(log n),where n is the number of data points.
  
  Space complexity: O(n)
  
  [Code](https://github.com/PAI-SHREYA/DSA/blob/main/Trees/KD_Tree.cpp)
- _**Union Find**_:
  
  Access, search, insertion, and deletion: O(log n),where n is the number of data points.
  
  Space complexity: O(n)
  
  [Code](https://github.com/PAI-SHREYA/DSA/blob/main/Trees/KD_Tree.cpp)










