---
title: Adaptive Streaming
subtitle: Adaptive streaming, also known as adaptive bitrate streaming (ABR), is a technique used to deliver video content over the internet in a way that adjusts the quality of the video in real-time based on the user's network conditions and device capabilities. This ensures smooth playback with minimal buffering, even under fluctuating bandwidth conditions.
image: assets/img/portfolio/adaptivestream1-1024x392.jpg


caption:
  title: Adaptive Streaming
  thumbnail: assets/img/portfolio/adaptive-bitrate-streaming.png
---
**Design Technique**

_**1.Segment Trees for Bandwidth Monitoring:**_
Segment Trees are used for efficient range queries and updates, which can help in monitoring bandwidth over different periods.Segment trees can be used to keep track of bandwidth usage statistics over different time intervals, allowing the system to quickly query and update the available bandwidth. This data can then be used to adjust the streaming quality in real-time.

_**2.Sliding Window Algorithm for Real-Time Adaptation:**_
Sliding Window Algorithm helps in processing streaming data in real-time, providing a way to manage the data flow and make decisions based on the most recent data.
The sliding window algorithm can be used to continuously monitor the recent bandwidth availability and user device performance. This helps in making quick adjustments to the streaming quality, ensuring that the changes are responsive to current conditions.

_**3.A-star Search for Optimal Segment Selection:**_
A Search Algorithm* can be used to find the optimal sequence of video segments to download that maximizes quality while minimizing buffering.
A* can be used to find the best sequence of segments to download next, considering factors like current bandwidth, buffer levels, and segment bitrates. This ensures that the most suitable segments are downloaded to maintain playback quality and avoid buffering.

_**4.Red-Black Trees for Managing Segment Metadata**_
Red-Black Trees are self-balancing binary search trees that ensure that the tree remains balanced, providing O(log n) time complexity for insertions, deletions, and lookups.
Red-Black Trees can be used to manage and retrieve metadata about video segments efficiently, such as segment sizes, bitrates, and download times. This helps in quickly accessing and updating segment information needed for adaptive streaming decisions.

_**5.Bloom Filters for Duplicate Segment Detection:**_
Bloom Filters are probabilistic data structures used to test whether an element is a member of a set, with a possibility of false positives but no false negatives.
Bloom filters can be used to detect and avoid downloading duplicate segments, ensuring efficient use of bandwidth. By quickly checking if a segment has already been downloaded or is currently in the buffer, the system can avoid redundant data transfers.


**Complexity Analysis and Code**

-**_Segment Trees_**

Time Complexity: For tree construction : O(n) For query: O(longn)

Space Complextity : O(4*n) ~ O(n)

[Code](https://github.com/PAI-SHREYA/DSA/blob/main/Trees/03_Minimum_Segment.cpp)

-**_Sliding Window_**

Time Complexity: O(n), where n is the size of input array.

Space Complexity: O(1)

[Code](https://github.com/PAI-SHREYA/DSA/blob/main/sliding.cpp)

-_**A-star Search**_

Time Complexity: O(E) (Worst case) for traversal, where E is the total number of edges.

Space Complexity: O(V) where V is the number of vertices

[Code](https://github.com/PAI-SHREYA/DSA/blob/main/Graph%20Traversal/A*-search.cpp)

_**Red-Black Trees**_

Time Complexity: O(log N) for insertion, deletion and lookup operations, where N is the number of elements.

Space Complexity: O(N).

[Code](https://github.com/PAI-SHREYA/DSA/blob/main/Trees/Red-Black-Tee.cpp)

-_**Bloom Filters**_

For m bits and k hash function,

Time Complexity: O(k) for insertion and search.

Space Complexity: O(m)

[Code](https://github.com/PAI-SHREYA/DSA/blob/main/Bloom.cpp)




