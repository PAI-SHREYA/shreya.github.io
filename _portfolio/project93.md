---
title: Search Optimization
subtitle: Users expect quick and accurate search results from applications and websites. Efficient search functionality is crucial for improving user experience, increasing engagement, and ensuring users find relevant content promptly. Optimizing search queries, processing large datasets efficiently, and handling dynamic data are key challenges in search optimization. 

caption:
  title: Search Optimization
  thumbnail: assets/img/portfolio/search_cover.png
---
**Design Technique**

_**1.Square Root Decomposition:**_
For optimizing search queries, particularly for range queries.Square Root Decomposition divides the data into smaller blocks to handle range queries more efficiently. This approach is beneficial when dealing with large datasets where direct query processing would be too slow.

_Scenario: User Engagement Scores for Netflix Titles_

We have a user engagement scores for various Netflix titles. These scores could be based on metrics such as views, likes, comments, or a combination thereof. We want to efficiently query and analyze which titles have the highest engagement scores using Square Root Decomposition.

<img src="assets/img/inside/sear-table.png">

Divide the list of titles into blocks. The number of blocks 𝑘= sqrt(n).
n is the total number of titles.

Netflix Titles:

Block 1: [Stranger Things, The Crown, Money Heist]
Block 2: [Bridgerton, Ozark, The Witcher]
Block 3: [Narcos, House of Cards, Black Mirror, The Umbrella Academy]

Square Root Decomposition is applied here to efficiently query and analyze user engagement scores for Netflix titles. By dividing the dataset into blocks and processing queries within these blocks, we can quickly identify titles with the highest engagement scores, providing insights into popular content on the platform.

_**2.MO's Algorithm:**_
Mo's Algorithm, also known as the "Sqrt Decomposition" algorithm, is typically used to answer offline range queries efficiently. It's particularly well-suited for problems where you need to answer multiple queries on a static array.It is not suitable for this use case because the catalog of movies and shows is constantly being updated with new releases, removals, and changes in metadata.Also,Search queries may involve complex filters, personalized recommendations, and relevance scoring rather than simple range queries.

_**3.Binary Search:**_
Binary search can be used for search optimization in the following scenarios:

-Quickly locating a specific movie title in a sorted list of titles.

-Although binary search is not inherently designed for prefix matching, it can be adapted to find the range of titles that start with a given prefix.

_**4. Trie Data Structure:**_
Tries, also known as prefix trees, are a efficient data structure for storing a dynamic set of strings where common prefixes are shared. They can be particularly useful for search optimization on the Netflix platform, especially for auto-completion, spell-checking and prefix-based search queries. 

<img src="assets/img/inside/trie.png">

**Complexity Analysis and Code**

-**_Square Root Decomposition_**

Time Complexity: O(N)

Auxiliary Space: O(MAXN), where MAXN is the maximum value of N

[Code](https://github.com/PAI-SHREYA/DSA/blob/main/sqrt_dec.cpp)

-**_MO's Algorithm_**

Time Complexity: O((N + Q) * sqrt(N) * F)

[Code](https://github.com/PAI-SHREYA/DSA/blob/main/mo.cpp)

-_**Binary Search**_

Time Complexity: O(log N)

Auxiliary Space: O(1)

[Code](https://github.com/PAI-SHREYA/DSA/blob/main/Binary_serach.cpp)

-_**Trie**_

Time Complexity: Insertion O(n), Searching O(n) and Deletion O(n)

Space Complexity Insertion O(n*m) ,Searching	O(1) and Deletion O(1)

[Code](https://github.com/PAI-SHREYA/DSA/blob/main/Trees/Trie.cpp)





