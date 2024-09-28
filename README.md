8-Puzzle Problem Solving Using BFS, DFS, and DFID
This code solves an 8-puzzle problem using three search algorithms:

Breadth-First Search (BFS) <br/>
  The problem involves moving the blank tile (represented by the number 9) in a 3x3 grid to reach a goal configuration. The algorithms generate new puzzle states     by moving the blank tile in four possible directions (up, down, left, and right) and search for the goal state.<br/>

# Code Structure
## Helper Functions
### Makepairs(NewNode, NodePair) 
  Purpose: This function creates pairs of the current node with its parent node. <br/>
  Arguments:<br/>
           NewNode: List of new nodes generated after moving the blank tile.<br/>
           NodePair: The current node that acts as the parent of the new nodes.<br/>
  Returns: A list of pairs of new nodes and their parent node.<br/>
    
### RemoveSeen(Closed, children)
  Purpose: Removes nodes that have already been visited (i.e., nodes in the Closed list) from the newly generated nodes.<br/>
  Arguments:<br/>
        Closed: List of nodes that have already been visited.<br/>
        children: List of new nodes generated.<br/>
  Returns: A list of nodes that haven't been visited yet.<br/>

### Reverse(lst)
  Purpose: Reverses a list.<br/>
  Arguments:<br/>
          lst: A list to reverse.<br/>
  Returns: The reversed list.<br/>
    
### ReconstructPath(NodePair, Closed)
  Purpose: Reconstructs the path from the initial node to the goal node by tracing back through the parent nodes.<br/>
  Arguments:<br/>
        NodePair: The goal node or current node.<br/>
        Closed: List of all nodes and their parents.<br/>
  Returns: A list representing the path from the start node to the goal node.<br/>
  
### swap(Nodepair, ni, nj, i, j)
  Purpose: Swaps two tiles in the puzzle.<br/>
  Arguments:<br/>
        Nodepair: The current puzzle configuration.<br/>
        ni, nj: Coordinates of the first tile.<br/>
        i, j: Coordinates of the second tile.<br/>
  Returns: The updated puzzle configuration after the swap.<br/>

### HammingDist(Node)
  Purpose: The number of tiles out of place.<br/>
  Arguments:<br/>
          Node = The current puzzle configuration
  Returns: Distance        

### MoveGen(Nodepair, i, j)
  Purpose: Generates new nodes by moving the blank tile in four possible directions (right, left, up, down).<br/>
  Arguments:<br/>
          Nodepair: The current puzzle configuration.<br/>
          i, j: Coordinates of the blank tile (9).<br/>
  Returns: A list of new puzzle configurations.<br/>
        
### func(NodePair)
  Purpose: Finds the position of the blank tile (9) in the current puzzle configuration.<br/>
  Arguments:<br/>
        NodePair: The current puzzle configuration.<br/>
  Returns: The coordinates (i, j) of the blank tile.<br/>

      
# Search Algorithms

### BFS(OpenNode, GoalNode , h)
  Purpose: Performs Breadth-First Search (BFS).<br/>
  Arguments:<br/>
          OpenNode: The initial node.<br/>
          GoalNode: The goal configuration.<br/>
          h : The number of tiles out of place.
  Returns: The path to the goal node.<br/>
