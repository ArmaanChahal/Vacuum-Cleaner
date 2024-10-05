# Vacuum Cleaner Pathfinding Simulation

This project simulates a vacuum cleaner agent navigating a grid environment to clean dirty spots using pathfinding algorithms, such as A* with Manhattan and Euclidean heuristics. The goal is to explore the performance differences between different heuristics in terms of nodes explored and the path taken.

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Setup](#setup)
- [Usage](#usage)
- [Algorithms](#algorithms)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

## Overview
This project is a Python simulation of an intelligent agent (vacuum cleaner) navigating a grid environment filled with dirt. The agent's task is to clean the dirty spots by finding the most efficient path to traverse the grid. The project uses two versions of the A* algorithm, each with a different heuristic:
- **Manhattan Heuristic**: Best suited for grid-based movement where only horizontal and vertical movements are allowed.
- **Euclidean Heuristic**: Assumes diagonal movement is possible and aims for the shortest straight-line path.

## Features
- A* algorithm with support for Manhattan and Euclidean distance heuristics.
- Comparison of path cost and the number of nodes explored between the two heuristics.
- Visualization of the grid environment with the agent's movements.
- Customizable grid size and dirt distribution.

## Setup
1. **Clone the repository**:
    ```bash
    git clone https://github.com/ArmaanChahal/Vacuum-Cleaner.git
    cd Vacuum-Cleaner
    ```

2. **Install dependencies**:
    Ensure you have Python 3.x installed. You can install necessary packages via `pip`:
    ```bash
    pip install -r requirements.txt
    ```

3. **Run the simulation**:
    ```bash
    python3 vacuum_search.py
    ```

## Usage
- When running the simulation, the agent will attempt to clean all the dirt in the grid. It will display the explored nodes and the path cost at the end.
- The user can select between A* with the Manhattan heuristic or the Euclidean heuristic by modifying the code or command-line arguments (if applicable).

## Algorithms
### A* Manhattan Heuristic
- Calculates the distance between two points based on vertical and horizontal moves only.
- More suited for grid-based movements where diagonal moves are not allowed.
- Explores more nodes but ensures valid paths when diagonal movement is restricted.

### A* Euclidean Heuristic
- Calculates the straight-line distance between two points.
- Optimistic in nature, assuming diagonal movement is allowed.
- Explores fewer nodes, resulting in shorter paths but might overestimate the feasibility of some routes.

## Results
| Heuristic  | Path Count | Nodes Explored |
|------------|-------------|----------------|
| Manhattan  | 59          | 154            |
| Euclidean  | 72          | 101            |

These results demonstrate how the A* Euclidean heuristic explores fewer nodes but results in a slightly longer path compared to the Manhattan heuristic. The Manhattan heuristic ensures valid paths with fewer turns, but it tends to explore more nodes.

## Contributing
Contributions are welcome! If you'd like to improve the project or fix any issues, feel free to fork the repository and submit a pull request.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
