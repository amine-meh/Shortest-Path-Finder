# Shortest Path Finder

This repository contains a Python program that visualizes the shortest path in a maze using the Breadth-First Search (BFS) algorithm. The program uses the `curses` library to display the maze and the pathfinding process in the terminal.

## Features
- Implements the BFS algorithm to find the shortest path in a maze.
- Real-time visualization of the pathfinding process.
- Highlights the path from the start point to the end point.

## Maze Representation
The maze is represented as a 2D list where:
- `"#"` represents walls.
- `"O"` is the starting point.
- `"X"` is the end point.
- Spaces (`" "`) are traversable paths.

Example maze:
```python
maze = [
    ["#", "O", "#", "#", "#", "#", "#", "#", "#"],
    ["#", " ", " ", " ", " ", " ", " ", " ", "#"],
    ["#", " ", "#", "#", " ", "#", "#", " ", "#"],
    ["#", " ", "#", " ", " ", " ", "#", " ", "#"],
    ["#", " ", "#", " ", "#", " ", "#", " ", "#"],
    ["#", " ", "#", " ", "#", " ", "#", " ", "#"],
    ["#", " ", "#", " ", "#", " ", "#", "#", "#"],
    ["#", " ", " ", " ", " ", " ", " ", " ", "#"],
    ["#", "#", "#", "#", "#", "#", "#", "X", "#"]
]
```

## How It Works
1. **Initialize the Maze:** The program starts by initializing the maze and locating the start point (`O`).
2. **Breadth-First Search (BFS):**
   - Uses a queue to explore the maze level by level.
   - Keeps track of visited cells to avoid redundant computations.
3. **Visualization:**
   - The maze is displayed in the terminal using the `curses` library.
   - The path being explored is highlighted in real-time.
4. **Path Output:** When the end point (`X`) is reached, the shortest path is highlighted.

## Requirements
- Python 3.x
- `curses` library (pre-installed with Python on Unix-based systems)

## Installation
Clone this repository:
```bash
git clone https://github.com/your-username/shortest-path-finder.git
cd shortest-path-finder
```

## Usage
Run the program:
```bash
python shortest_path_finder.py
```

## File Structure
```
shortest-path-finder/
├── shortest_path_finder.py  # Main program file
```

## Functions Overview
### `start_position(maze, start)`
- Finds the starting position in the maze.

### `find_path(maze, stdscr)`
- Implements the BFS algorithm to find the shortest path.

### `find_neighbors(maze, row, col)`
- Returns a list of valid neighboring cells.

### `print_maze(maze, stdscr, path=[])`
- Displays the maze in the terminal and highlights the path.

### `main(stdscr)`
- Initializes `curses` and starts the visualization.

## Demo
The program highlights the pathfinding process:
- Walls are shown in blue.
- The explored path is highlighted in red.

## License
This project is licensed under the MIT License.

## Contributions
Feel free to fork this repository and submit pull requests to improve the program.

## Author
- **Your Name** - Med Amine

---
Enjoy visualizing shortest pathfinding with Python! 🎉
