# Sample-Based Path Planning
Sample-based path planning differs from combinatorial path planning in that it does not try to systematically discretize the entire configuration space. Instead, it samples the configuration space randomly (or semi-randomly) to build up a representation of the space. The resultant graph is not as precise as one created using combinatorial planning, but it is much quicker to construct because of the relatively small number of samples used.

Such a method is probabilistically complete because as time passes and the number of samples approaches infinity, the probability of finding a path, if one exists, approaches 1.

Such an approach is very effective in high-dimensional spaces, however it does have some downfalls. Sampling a space uniformly is not likely to reach small or narrow areas, such as the passage depicted in the image below. Since the passage is the only way to move from start to goal, it is critical that a sufficient number of samples occupy the passage, or the algorithm will return ‘no solution found’ to a problem that clearly has a solution.

![](images/c5-l3-img-sample-based-planning-v2.png)

Different sample-based planning approaches exist, each with their own benefits and downfalls. In the next few pages you will learn about,

- Probabilistic Roadmap Method
- Rapidly Exploring Random Tree Method

You will also learn about Path Smoothing - one improvement that can make resultant paths more efficient.
