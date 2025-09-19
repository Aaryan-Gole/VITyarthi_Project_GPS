# Smart GPS Navigation: A Comparative Study of Pathfinding Algorithms

## Overview
This project analyzes a Python-based pathfinding toolkit designed for smart GPS navigation in grid-based maps. It includes comparative evaluation of BFS, UCS, and A* search algorithms for static and dynamic obstacle environments[files:1].

## Features
- Implements Breadth-First Search (BFS), Uniform Cost Search (UCS), and A* algorithms[files:1].
- Supports static and dynamic grid-based map scenarios[files:1].
- Measures performance: nodes expanded, path cost, execution time, memory usage[files:1].
- Visualizations for performance comparisons by map size and obstacle density[files:1].

## Environment Model
- **2D Grid Representation**: Each cell has a movement cost. Obstacles are marked as `-1`.
- **Movement**: 4-directional or optional diagonal moves, with cost differences[files:1].
- **Map Types**: Static maps (small, medium, large) and dynamic maps (real-time obstacle updates)[files:1].

## Agent and Algorithms
- **Architecture**: Modular search engine with clear state/action/goal separation[files:1].
- **Breadth-First Search**: Finds shortest path in unweighted graphs, optimal on uniform cost grids[files:1].
- **Uniform Cost Search**: Uses a priority queue for optimal paths in weighted environments[files:1].
- **A* Search**: Combines UCS with admissible heuristics (Manhattan/Euclidean distance)[files:1].

## Heuristics
- Manhattan distance for grid movement (no diagonals)[files:1].
- Euclidean distance for environments with diagonal movement[files:1].
- Heuristic selection based on allowed moves; zero heuristic reduces A* to UCS for benchmarking[files:1].

## Experimental Results

| Algorithm | Map Size | Nodes Expanded | Path Cost | Time (ms) | Memory (KB) |
|-----------|----------|---------------|-----------|-----------|-------------|
| BFS       | Small    | 25            | 8         | 2.1       | 1.2         |
|           | Medium   | 400           | 38        | 15.3      | 8.7         |
|           | Large    | 2500          | 98        | 95.2      | 45.3        |
| UCS       | Small    | 22            | 8         | 2.3       | 1.4         |
|           | Medium   | 285           | 35        | 12.8      | 6.9         |
|           | Large    | 1850          | 87        | 78.5      | 38.1        |
| A*        | Small    | 13            | 8         | 1.8       | 0.9         |
|           | Medium   | 95            | 35        | 4.2       | 2.8         |
|           | Large    | 425           | 87        | 28.7      | 15.6        |[files:1]

### Handling Dynamic Obstacles
- A* maintains high success rate and efficient replanning as obstacle density increases[files:1].
- Local replanning and obstacle prediction suggested for future enhancements[files:1].

## Analysis
- A* consistently reduces computational cost (60–80% fewer node expansions) while maintaining optimality[files:1].
- Framework scales from small to large maps, with A* showing nearly linear growth[files:1].
- Navigation efficiency sustained in dynamic environments; suitable for embedded systems and city-level route planning[files:1].

## Future Enhancements
- Machine learning for obstacle prediction
- Hierarchical pathfinding for massive maps
- Multi-criteria optimization (e.g., time, fuel)
- Real-world GPS data validation[files:1]

## Author
Aaryan Gole  
Reg. No. 24MIM10003  
Int. MTech5 Student, VIT Bhopal, MP

---

*This README.md follows recommended GitHub Markdown structure for overview, features, usage, results, and credits[web:3][web:6].*
