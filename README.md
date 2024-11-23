# CI2024_lab3

The algorithm solves the puzzle using bidirectional A* search, which combines two simultaneous searches: one forward from the initial state and one backward from the goal state. Each search explores the most promising states first, guided by the cost function 
f=g+h, where:
g is the cost to reach the current state.
h is a heuristic estimate of the remaining cost to reach the goal state. 
This algorithm uses a combination of Manhattan Distance and Linear Conflict as the heuristic:
Manhattan Distance calculates the total vertical and horizontal distance for each tile to reach its target position.
Linear Conflict adds a penalty when two tiles in the same row or column block each other from reaching their goals, improving the heuristic's accuracy.
The algorithm stops when the forward and backward searches meet at a common state, forming an intersection. The solution is reconstructed by combining the paths from both directions.
The resolution time may vary from one initial configuration to another.
Larger puzzles, like 4×4 or 5×5, have exponentially larger state spaces, making them considerably slower to solve due to the higher number of states to evaluate and the greater computational cost of the heuristic.