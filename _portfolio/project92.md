---
title: Cross-Device Sync
subtitle: Netflix's cross-device sync feature allows users to continue watching content across multiple devices.A user might start watching a movie on their smart TV, pause it, and then continue from the same point on their smartphone. This capability enhances user experience by providing continuity and convenience, ensuring that users can pick up right where they left off, regardless of the device they are using.

caption:
  title: Cross-Device Sync
  thumbnail: assets/img/portfolio/ShopifyPlus_Cross_Device_Targeting_3840x2160.png
---
**Challenges and Market Benefits**
Users appreciate the ability to switch devices seamlessly, leading to higher satisfaction and engagement.Offering a reliable cross-device sync feature can differentiate Netflix from other streaming services, attracting and retaining more users.Maintaining consistent data across different devices, especially in scenarios with intermittent connectivity or offline usage could be a challenge. We need to ensure that the playback position, settings, and user preferences are updated in real-time across all devices.

**Design Technique**

_**1.Lazy Propagation**_
Lazy propagation is a technique used to delay updates to a data structure until necessary. This can be particularly useful for handling updates in distributed systems or across multiple devices, such as syncing user preferences, watch history, and bookmarks on Netflix.Suppose a user is watching a movie on their phone and then switches to their TV. The user's watch progress, preferences, and recently watched items need to be synchronized across devices.Instead of immediately pushing every small update to all devices, updates are recorded and propagated lazily when a device requests the latest data.
This reduces the amount of data transmitted and can handle bursts of updates efficiently.

_**2. Bloom Filters**_
Bloom filters are a space-efficient probabilistic data structure used to test whether an element is a member of a set. They are useful for scenarios where false positives are acceptable but false negatives are not.Bloom filters can be used to maintain a compact representation of the user's watch history.
When a device queries the server, it can quickly check the Bloom filter to see if the user has watched a particular show or movie.

**Complexity Analysis and Codes**

_**-Lazy Propagation**_

Time Complexity: O(n logn)

Space Complexity: O(n logn)

[Code](https://github.com/PAI-SHREYA/DSA/blob/main/Software%20Principles/LazyPropagation.cpp)

_**- Bloom Filters**_

For m bits and k hash function,

Time Complexity: O(k) for insertion and search.
Space Complexity: O(m)

[Code](https://github.com/PAI-SHREYA/DSA/blob/main/Bloom.cpp)







