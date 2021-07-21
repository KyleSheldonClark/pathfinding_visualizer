Pathfinding Visualizer
=======================

Pathfinding Algorithms
-------------------------
- Dijkstra's Algorithm
- A* Search Algorithm


Maze Generation Algorithms
-----------------------------
- Randomized Prim's Algorithm
- Randomized Depth-First Search (Iterative Implementation)
  - Choose a random dell from the grid.
    - For this cell randomly choose one of it's unvisited neighbours.
      - remove the wall between the first cell and the chose neighbour.
      - mark the neighbour as visited, and add to the stack.
    - Continue until a cell which has no unvisited neighbours is reached this is considered a dead end.
      - When a dead end is reached backtrack through the path until a cell with an unvisited neighbour is reached.
    - Continue the path generation starting at this cell.
    - Repeat this process until all cells have been visited and we backtrack all the way to the starting cell.
