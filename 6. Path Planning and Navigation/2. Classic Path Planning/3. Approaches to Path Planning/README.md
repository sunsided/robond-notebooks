# Approaches to Path Planning

In this lesson, you will be studying three different approaches to path planning. The first, called **discrete** (or **combinatorial**) **path planning**, is the most straightforward of the three approaches. The other two approaches, called **sample-based path planning** and **probabilistic path planning**, will build on the foundation of discrete planning to develop more widely applicable path planning solutions.

## Discrete Planning

Discrete planning looks to explicitly discretize the robot’s workspace into a connected graph, and apply a graph-search algorithm to calculate the best path. This procedure is very precise (in fact, the precision can be adjusted explicitly by changing how fine you choose to discretize the space) and very thorough, as it discretizes the complete workspace. As a result, discrete planning can be very computationally expensive - possibly prohibitively so for large path planning problems.

The image below displays one possible implementation of discrete path planning applied to a 2-dimensional workspace.

![](images/c5-l2-09-img-image-of-discrete-v1.png)

Discrete path planning is elegant in its preciseness, but is best suited for low-dimensional problems. For high-dimensional problems, sample-based path planning is a more appropriate approach.

## Sample-Based Planning
Sample-based path planning probes the workspace to incrementally construct a graph. Instead of discretizing every segment of the workspace, sample-based planning takes a number of samples and uses them to build a discrete representation of the workspace. The resultant graph is not as precise as one created using discrete planning, but it is much quicker to construct because of the relatively small number of samples used.

A path generated using sample-based planning may not be the best path, but in certain applications - it’s better to generate a feasible path quickly than to wait hours or even days to generate the optimal path.

The image below displays a graph representation of a 2-dimensional workspace created using sample-based planning.

![](images/c5-l2-11-prm-1516-v2.png)

## Probabilistic Path Planning
The last type of path planning that you will learn about in this module is probabilistic path planning. While the first two approaches looked at the path planning problem generically - with no understanding of who or what may be executing the actions - probabilistic path planning takes into account the uncertainty of the robot’s motion.

While this may not provide significant benefits in some environments, it is especially helpful in highly-constrained environment or environments with sensitive or high-risk areas.

The image below displays probabilistic path planning applied to an environment containing a hazard (the lake at the top right).

![](images/mdpimage-53-v2.png)
