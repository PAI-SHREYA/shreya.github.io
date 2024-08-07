---
title: Scheduling and Sequencing of Ad Placements
subtitle: Netflix's ad scheduling and sequencing system aims to optimize the placement of advertisements during streaming sessions to maximize user engagement and ad revenue. The system analyzes a variety of user data, such as viewing history, watch time, device type, and time of day, to tailor ad placements that are most likely to resonate with individual users. By delivering personalized and well-timed ads, Netflix ensures that ads are relevant and minimally intrusive.

caption:
  title: Scheduling and Sequencing of Ad Placements
  thumbnail: assets/img/portfolio/ad-placements.png
---
**Challenges and Market Benefits**

Netflix deals with a massive amount of data generated by millions of users. This includes real-time interactions, content metadata, and user preferences.
Efficiently processing and analyzing this data to make real-time ad placement decisions is a significant challenge.Content and user preferences are categorized by multiple attributes, making the scheduling problem multi-dimensional and complex.
Personalized and relevant ads increase user engagement and reduce the likelihood of users skipping ads or leaving the platform.Efficient ad scheduling and sequencing ensure optimal utilization of ad slots, maximizing ad revenue.Promoting diverse content through targeted ads helps in driving viewership of less popular titles, ensuring a better return on investment in content acquisition and production.

**Design Technique**

_**1.Boruvka's Algorithm**_

This is used to efficiently find the Minimum Spanning Tree (MST) of a graph. For ad scheduling, nodes represent ad slots, and edges represent the cost or benefit of scheduling ads consecutively.

The Boruvka's algorithm can be implemented as follows:

-->Nodes represent individual ad slots.

-->Edges represent transitions between ad slots, weighted by the cost or benefit of scheduling ads consecutively.

-->Start with each ad slot as a separate component.For each component, find the cheapest edge connecting it to another component.These edges are added to the MST.

-->Repeat until there is only one component left.

-->The resulting MST provides an optimized sequence of ad placements with minimal transition costs or maximal benefits.

<img src="assets/img/inside/boruvka.png" alt="KD-Tree Design" width="500">

_**2.Look Up Table**_

Using this we can quickly retrieve precomputed values to optimize scheduling decisions, such as the best times to display ads based on historical data.
Design Implementation:
-Create lookup tables that store precomputed values for various metrics (e.g., user engagement, optimal ad times).Populate the lookup table with data derived from historical ad performance.During scheduling, use the lookup table to quickly retrieve the optimal ad times or sequences.


_**3.Catalan Numbers:**_

Catalan numbers often appear in problems involving combinatorial structures. In ad scheduling, they can be used to model and optimize hierarchical decision-making processes, such as ad slot arrangements or sequences.Catalan numbers can be used to determine the number of ways to sequence ads under certain constraints, such as no two high-priority ads being adjacent.


_**4.Flavius Numbers:**_

Flavius numbers are less commonly known, but they can be used in scheduling algorithms to manage repetitive patterns or sequences.Flavius numbers are similar to Josephus problem solutions, where people are eliminated in a circle until only one remains.We can use this property to model round-robin scheduling or cyclic patterns.

_Design:_

<img src="assets/img/inside/ad-scheduling.jpeg" alt="sys arch" width="500">

 
**Complexity Analysis and Codes**

-**_Boruvka's Algorithm_**

Time Complexity:O(E log V) 

Space Complexity: O(V)

[Code](https://github.com/PAI-SHREYA/DSA/blob/main/Trees/Boruvka's.cpp)

**_Look Up Table_**

[Code](https://github.com/jiyapalrecha35/Google.github.io/blob/main/codes/lookupTable.cpp)

**_Catalan Number(Using Binomial Coefficient)_**

Time Complexity: O(n)

Space Complexity: O(1)

[Code](https://github.com/PAI-SHREYA/DSA/blob/main/Catalan.cpp)

**_Flavius Numbers_**

Time complexity: O(n)

Space complexity: O(1)

[Code](https://github.com/PAI-SHREYA/DSA/blob/main/Flavius.cpp)


