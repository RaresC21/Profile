# Research 

### Deterministic Volume Approximation of Polytopes


Computing the volume of a convex body has been a long-studied question, important from both a theoretical and practical perspective. A key aspect of the problem lies in the representation of the set. In the most general case, access to the set is provided solely through an oracle. However, given only a well-guaranteed separation oracle, no deterministic polynomial-time algorithm can approximate the volume to within a factor exponential in the dimension. However, access to an explicit description of the set removes this obstacle. As such, we restrict our attention to computing the volume of polytopes, which are expressed as the intersection of halfspaces.

Surprisingly, there do exist efficient randomized algorithms to compute volume given only an oracle. The problem has essentially been reduced to sampling uniformly from the interior of the polytope.

We investigate whether the notion of chaos can serve as a substitute for randomness in this setting. Given the initial state of a system, we cannot predict the future state of a random process. On the other hand, a chaotic one is fully deterministic. But this process is sensitive to initial conditions: any small change in initial conditions will result in vastly different orbits. 


In particular, we consider the orbit created by the free motion of a point particle inside the polytope with mirror-like reflections off the boundary. Figure (a) depicts the trajectory of a point particle in a square. However this system is not chaotic as translating the initial point will result in largely the same result. To remedy this, we introduce an inward curvature to the boundary. Figure (b) depicts the trajectory of the same initial point, only with circles placed around the boundary.

<img src="images/billiards.png" alt="hi" class="inline"/>

For more details on the reduction from volume to sampling and chaos and billiards, see [here](https://github.com/RaresC21/Profile/blob/master/pdf/Deterministic_Volume_Approximation.pdf)

### Range Queries

Range queries are a fundamental operation used in many applications, especially as database queries. Here, we restrict ourselves to queries on a static, one-dimensional array, X. A classic example includes finding the minimum entry in a contiguous subarray. More generally, we are given some fixed function f, and a sequence of queries (l,r) to compute f(X[l], X[l+1], ..., X[r]). Most data structures preprocess the array to determine the value of f for a particular subset P of ranges. To answer any query, they simply merge the solutions from a subset of precomputed ranges in P. 

For instance, consider the range sum problem. Here, the function f simply takes the sum of its inputs. We may compute the sum of all prefixed of the array: P[i] = X[1] + X[2] + ... + X[i]. Then, given a query (l,r) the answer is simply P[r] - P[l-1]. This partitioning scheme makes use of the fact that summation has an inverse, subtraction. We are interested in a broader class of functions. To answer any query (l,r) we are only allowed to use precomputed ranges which form a partition of (l,r). This allows for functions such as min, max, gcd, and various others. See the paper below for more details.

I have worked on finding better partitioning schemes. Given an array of length n, we require O(n log n) preprocessing time to compute solutions to various ranges, and O(1) time to answer any query afterwards. More [details](https://github.com/RaresC21/Data-Structures/blob/master/NovelRangeQuery/Range_Queries.pdf), and an [implementation](https://github.com/RaresC21/Data-Structures/blob/master/NovelRangeQuery/NovelRangeQuery.cpp).
