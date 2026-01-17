# City Antenna Network: Graph Implementation in C

## Project Overview
This project simulates an antenna network deployment within a "City" grid (character matrix). The environment is represented by a matrix where each `.` indicates an empty space, and characters such as `A` or `B` represent localized antennas. 

The core objective was to implement a system that automatically connects these antennas through a **Graph** structure, allowing for network traversal and connectivity analysis.

## Technical Implementation

### Multi-Graph Architecture
The system segregates network traffic by frequency. When an antenna is added to the city grid, it is automatically assigned to a specific graph based on its identifier:
* **Frequency A Graphs**: Dedicated to all antennas labeled `A`.
* **Frequency B Graphs**: Dedicated to all antennas labeled `B`.

### Graph Traversal Algorithms
To analyze connectivity and network reach, two fundamental traversal methods were implemented:
* **Breadth-First Traversal (BFT)**: Used to explore the network level by level, ideal for finding the shortest path between nodes.
* **Depth-First Search (DFS)**: Implemented to explore as far as possible along each branch before backtracking, useful for detecting cycles and exploring complete network paths.

### Memory & Grid Management
* **Dynamic Adjacency Lists**: The graphs were implemented using dynamic allocation to handle a variable number of connections efficiently.
* **Matrix-to-Graph Mapping**: Logic developed to translate spatial coordinates from the character matrix into nodes and edges within the graph.

## Academic Context
Developed as part of the **Advanced Data Structures** curriculum in the **Computer Systems Engineering** degree at **IPCA**.This project demonstrates proficiency in:

1. **Complex Data Structures**: Designing graphs and integrating them with matrices.
2. **Search Algorithms**: Implementing and comparing BFT vs DFS performance.
3. **C Programming**: Advanced pointer manipulation and memory management.

---
### How to Compile & Run
1. Clone the repository: `git clone https://github.com/rogerio-picas/EDA-Graph`
2. Compile the project: `gcc -o antenna_graph main.c` (adjust filename if necessary)
3. Run: `./antenna_graph`
