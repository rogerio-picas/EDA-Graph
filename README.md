# City Antenna Network: Graph Implementation in C

## Project Overview
This project simulates an antenna network deployment within a "City" grid (character matrix). The environment is represented by a matrix where each `.` indicates an empty space, and characters such as `A` or `B` represent localized antennas. 

The core objective was to implement a system that automatically connects these antennas through a **Graph** structure, allowing for network traversal and connectivity analysis.

## Technical Implementation

### Multi-Graph Architecture
The system segregates network traffic by frequency. When an antenna is added to the city grid, it is automatically assigned to a specific graph based on its identifier:
* [cite_start]**Frequency A Graphs**: Dedicated to all antennas labeled `A`. [cite: 74]
* [cite_start]**Frequency B Graphs**: Dedicated to all antennas labeled `B`. [cite: 74]

### Graph Traversal Algorithms
To analyze connectivity and network reach, two fundamental traversal methods were implemented:
* [cite_start]**Breadth-First Traversal (BFT)**: Used to explore the network level by level, ideal for finding the shortest path between nodes. [cite: 116]
* [cite_start]**Depth-First Search (DFS)**: Implemented to explore as far as possible along each branch before backtracking, useful for detecting cycles and exploring complete network paths. [cite: 116]

### Memory & Grid Management
* [cite_start]**Dynamic Adjacency Lists**: The graphs were implemented using dynamic allocation to handle a variable number of connections efficiently. [cite: 21, 133]
* [cite_start]**Matrix-to-Graph Mapping**: Logic developed to translate spatial coordinates from the character matrix into nodes and edges within the graph. [cite: 21, 133]

## Academic Context
Developed as part of the **Advanced Data Structures** curriculum in the **Computer Systems Engineering** degree at **IPCA**. [cite_start]This project demonstrates proficiency in: [cite: 84, 85, 115]

1. [cite_start]**Complex Data Structures**: Designing graphs and integrating them with matrices. [cite: 116]
2. [cite_start]**Search Algorithms**: Implementing and comparing BFT vs DFS performance. [cite: 116]
3. [cite_start]**C Programming**: Advanced pointer manipulation and memory management. [cite: 21, 133]
