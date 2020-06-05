# Voronoi Diagram

Another discretization method that generates a roadmap is called the Voronoi Diagram. Unlike the visibility graph method which generates the shortest paths, Voronoi Diagrams maximize clearance between obstacles.

A Voronoi Diagram is a graph whose edges bisect the free space in between obstacles. Every edge lies equidistant from each obstacle around it - with the greatest amount of clearance possible. You can see a Voronoi Diagram for our configuration space in the graphic below.

![](images/l251-voronoi-diagram-01-v4.png)

Once a Voronoi Diagram is constructed for a workspace, it can be used for multiple queries. Start and goal nodes can be connected into the graph by constructing the paths from the nodes to the edge closest to each of them.

Every edge will either be a straight line, if it lies between the edges of two obstacles, or it will be a quadratic, if it passes by the vertex of an obstacle.

## Quiz

Once again, it is worth investigating - will the roadmap built by the voronoi diagram contain a path from start to goal, and will it contain the optimal path.

> Is the Voronoi Diagram complete? Does it contain the optimal path?
>
> - [x] Complete
> - [ ] Optimal
> - [ ] Neither
>
> That’s right - the Voronoi Diagram is complete, but it does not contain the optimal path. However, it contains a path from start to goal with the most possible clearance, which in certain applications is more desirable than the optimal path.
