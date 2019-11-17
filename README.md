# Research 

### Deterministic Volume Approximation of Polytopes


Computing the volume of a convex body has been a long-studied question, important from both a theoretical and practical perspective. A key aspect of the problem lies in the representation of the set. In the most general case, access to the set is provided solely through an oracle. However, given only a well-guaranteed separation oracle, no deterministic polynomial-time algorithm can approximate the volume to within a factor exponential in the dimension. However, access to an explicit description of the set removes this obstacle. As such, we restrict our attention to computing the volume of polytopes, which are expressed as the intersection of halfspaces.

Surprisingly, there do exist efficient randomized algorithms to compute volume given only an oracle. The problem has essentially been reduced to sampling uniformly from the interior of the polytope.

We investigate whether the notion of chaos can serve as a substitute for randomness in this setting. Given the initial state of a system, we cannot predict the future state of a random process. On the other hand, a chaotic one is fully deterministic. But this process is sensitive to initial conditions: any small change in initial conditions will result in vastly different orbits. 


In particular, we consider the orbit created by the free motion of a point particle inside the polytope with mirror-like reflections off the boundary. Figure (a) depicts the trajectory of a point particle in a square. However this system is not chaotic as translating the initial point will result in largely the same result. To remedy this, we introduce an inward curvature to the boundary. Figure (b) depicts the trajectory of the same initial point, only with circles placed around the boundary.

![Chaotic Billiards](https://github.com/RaresC21/Profile/blob/master/images/billiards.png)

For more details on the reduction from volume to sampling and chaos and billiards, see [here](https://github.com/RaresC21/Profile/blob/master/pdf/Deterministic_Volume_Approximation.pdf)
