Pathfinding Visualizer
=======================

Pathfinding Algorithms
-------------------------
- Dijkstra's Algorithm
- A* Search Algorithm


Maze Generation Algorithms
-----------------------------
### Randomized Prim's Algorithm
  - Start with a grid full of walls.
  - Choose a random cell.
    - Mark cell as part of the maze.
    - add all neighbours of the cell to the walls to check list.
  - While there are walls in the list.
    - Pick a random wall from the list.
      - If only one of the cells the wall divides is visited:
        - Make the wall a passage and mark the unvisited cell as part of the maze.
        - add all neighbours of the cell to the walls to check list.
      - Remove the wall from the walls to check list.

### Randomized Depth-First Search (Iterative Implementation)
  - Choose a random cell from the grid.
    - For this cell randomly choose one of it's unvisited neighbours.
      - remove the wall between the first cell and the chose neighbour.
      - mark the neighbour as visited, and add to the stack.
    - Continue until a cell which has no unvisited neighbours is reached this is considered a dead end.
      - When a dead end is reached backtrack through the path until a cell with an unvisited neighbour is reached.
    - Continue the path generation starting at this cell.
    - Repeat this process until all cells have been visited and we backtrack all the way to the starting cell.
