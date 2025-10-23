## Optimization of Electric Vehicle Charging Station Placement and Network Connectivity

## Project Overview
This project implements a solution for optimizing the placement and connectivity of Electric Vehicle (EV) charging stations in a weighted graph representing a network of locations. It uses graph algorithms to:

- Determine strategic locations for charging stations based on EV demand.
- Compute the shortest travel distances from stations to all other nodes.
- Connect the stations with minimum infrastructure cost.
- Analyze network coverage by hop count (number of edges) for reachability.

The project uses three fundamental graph algorithms: Dijkstra’s algorithm, Prim’s Minimum Spanning Tree algorithm, and Breadth-First Search (BFS).

## Features
- Greedy placement of charging stations maximizing demand coverage.
- Efficient shortest weighted path computations from stations using Dijkstra’s algorithm.
- Minimum cost connection among charging stations using Prim’s MST algorithm.
- BFS-based hop count analysis for connectivity insights.

## Algorithms Used
- *Dijkstra’s Algorithm*: To find shortest weighted paths from a station node to all others.
- *Prim’s Algorithm*: To build Minimum Spanning Tree connecting all stations with minimal wiring cost.
- *Breadth-First Search (BFS)*: To calculate minimal hop distances representing connectivity steps.

## Project Structure
- main.cpp - Contains the full source code including:
  - Data definitions for graph nodes and EV demand.
  - Implementations of Dijkstra, Prim, BFS algorithms.
  - Greedy approach to station placement.
  - Console output demonstrating algorithm results and comparisons.

## How to Run
1. Clone the repository.
2. Compile the source code with a C++ compiler (e.g. g++ main.cpp -o ev_optimization).
3. Run the executable (e.g. ./ev_optimization).
4. Observe the optimized station placement, shortest path results, MST connections, and BFS hop coverage in the console output.



