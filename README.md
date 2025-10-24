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

## Example Output
========================================
EV CHARGING INFRASTRUCTURE OPTIMIZATION
========================================
Using 3 Algorithms: Dijkstra, Prim, BFS

Stations placed at:
  Node 4 (Demand: 35)
  Node 3 (Demand: 10)
  Node 5 (Demand: 25)


=== DIJKSTRA'S ALGORITHM ===
Finding shortest weighted paths from each station

From Station N4:
  To N1: 6 units
  To N2: 8 units
  To N3: 11 units
  To N4: 0 units
  To N5: 7 units
  To N6: 3 units

From Station N3:
  To N1: 5 units
  To N2: 3 units
  To N3: 0 units
  To N4: 11 units
  To N5: 7 units
  To N6: 11 units

From Station N5:
  To N1: 7 units
  To N2: 5 units
  To N3: 7 units
  To N4: 7 units
  To N5: 0 units
  To N6: 4 units


=== PRIM'S ALGORITHM (MST) ===
Connecting all stations with minimum cost


MST Edges for station connection:
  N5 <--> N4 (cost: 9)
  N3 <--> N5 (cost: 7)

Total MST cost: 16 units


=== BFS ALGORITHM ===
Calculating hop-based coverage from stations

From Station N4 (hop count):
  To N1: 1 hops
  To N2: 1 hops
  To N3: 2 hops
  To N4: 0 hops
  To N5: 1 hops
  To N6: 1 hops

From Station N3 (hop count):
  To N1: 2 hops
  To N2: 1 hops
  To N3: 0 hops
  To N4: 2 hops
  To N5: 1 hops
  To N6: 2 hops

From Station N5 (hop count):
  To N1: 2 hops
  To N2: 1 hops
  To N3: 1 hops
  To N4: 1 hops
  To N5: 0 hops
  To N6: 1 hops


=== COMPARISON: Dijkstra vs BFS ===
From Station N4:

    Node   Dijkstra (cost)     BFS (hops)
----------------------------------------
      N1                 6              1
      N2                 8              1
      N3                11              2
      N4                 0              0
      N5                 7              1
      N6                 3              1


========================================
SUMMARY
========================================
Stations: 3 placed
MST Cost: 16 units to connect stations

Algorithms Used:
1. Dijkstra: Found shortest weighted paths
2. Prim: Minimized station connection cost
3. BFS: Analyzed hop-based coverage

