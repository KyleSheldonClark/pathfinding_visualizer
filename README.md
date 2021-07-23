Pathfinding Visualizer
=======================

Pathfinding Algorithms
-------------------------
- Dijkstra's Algorithm
  - Mark all nodes as unvisited.
    - Assign every node a distance from start value(Zero for initial node. Infinity for all other nodes).
    - Mark initial node as current node.
    - For the current node.
      - Consider all neighbouring nodes.
      - Update neighbouring nodes distance with distance from current node plus current nodes distance from start.
      - When all neighbours have been checked and updated mark current node as visited and remove from strSet.
    - If the destination node has been marked visited the program stops. The algorithm is finished.
    - Otherwise take smallest node from strSet, mark as current node and repeat above steps.

- A* Search Algorithm


Maze Generation Algorithms
-----------------------------
### Randomized Prim's Algorithm
  - Start with a grid full of walls.
  - Choose a random cell.
    - Mark cell as part of the maze.
    - Add all neighbours of the cell to the walls to check list.
  - While there are walls in the list.
    - Pick a random wall from the list.
      - If only one of the cells the wall divides is visited:
        - Make the wall a passage and mark the unvisited cell as part of the maze.
        - Add all neighbours of the cell to the walls to check list.
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
