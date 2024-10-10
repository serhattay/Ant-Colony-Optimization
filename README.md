
TRAVELING SALESMAN PROBLEM SOLVER USING ANT COLONY OPTIMIZATION (ACO)
====================================================================

This repository contains a Java-based implementation of the Traveling Salesman Problem (TSP) solver using the Ant Colony Optimization (ACO) algorithm. ACO is a bio-inspired algorithm that mimics the behavior of ants in nature to find optimal paths through the use of pheromone trails. This program optimizes the time complexity of solving the TSP and produces a graphical representation of the nodes, the shortest path, and pheromone levels.

JAVA CLASSES
------------

- Node.java: Defines the structure of a node in the graph, including its properties such as position and label. Each node represents a city or location that needs to be visited in the TSP.

- Pheromone.java: Manages the pheromone levels between nodes. This class includes methods for updating pheromones, which guide the ants in selecting the best paths. The pheromone trails decay over time to encourage exploration of new paths.

- SerhatTay.java: The main class that orchestrates the ACO algorithm. This class handles the initialization of nodes, the ant population, and the graphical output. It runs the algorithm over multiple iterations, producing the final visualization of the shortest path and pheromone trails.

FEATURES
--------

- Ant Colony Optimization Algorithm: Uses a population of ants to find an efficient solution to the TSP by simulating the natural behavior of ants.
- Graphical Output: Displays a graphical representation of the nodes, the shortest path, and the pheromone levels between nodes.
- Pheromone Trail Visualization: Shows the intensity of pheromones as thicker lines, helping you understand which paths are being reinforced by the algorithm.
- Customizable Parameters: Allows users to adjust ACO parameters, such as the number of ants, pheromone evaporation rate, and number of iterations.

HOW TO RUN
----------

Prerequisites:
- Java Development Kit (JDK 8 or later)
- A suitable Integrated Development Environment (IDE) like Eclipse or IntelliJ, or the ability to run Java from the command line.

Steps:
1. Clone or download this repository to your local machine:

    git clone https://github.com/serhattay/Ant-Colony-Optimization.git
    cd Ant-Colony-Optimization

2. Open the project in your IDE or navigate to the folder in the command line.

3. Compile and run the SerhatTay.java file:

    javac SerhatTay.java
    java SerhatTay

4. The program will compute the shortest path between the nodes and display a graphical output showing:
   - The nodes (cities) and their positions.
   - The shortest path found by the ants.
   - The pheromone trails between the nodes, represented by varying line thicknesses.

EXAMPLE
-------

Once executed, the graphical output will look similar to this:
- Nodes: Represented as circles.
- Shortest Path: Highlighted with a distinct color showing the optimal route.
- Pheromones: Represented by varying line thickness, with thicker lines indicating stronger pheromone levels.

CONFIGURATION
-------------

The behavior of the ACO algorithm can be customized by editing the SerhatTay.java class. Key parameters you may want to adjust:
- Number of Ants: The population of ants that traverse the graph.
- Pheromone Evaporation Rate: Controls how quickly pheromones decay, encouraging exploration.
- Alpha and Beta: Weights for pheromone strength and distance heuristic, respectively.
- Iterations: The number of cycles the algorithm will run before stopping.

ANT COLONY OPTIMIZATION OVERVIEW
--------------------------------

The Ant Colony Optimization (ACO) algorithm works by simulating how ants find the shortest path to food sources by laying down pheromones. Ants will tend to follow trails with higher pheromone concentrations, but some exploration of new paths is always encouraged.

The algorithm consists of the following steps:
1. Initialization: The ants are placed randomly on different nodes (cities).
2. Tour Construction: Each ant constructs a tour by probabilistically selecting the next node to visit, influenced by pheromone strength and distance.
3. Pheromone Update: After all ants have completed their tours, pheromones are updated. Paths that were part of shorter tours receive more pheromones.
4. Evaporation: Pheromones decay over time, preventing the algorithm from prematurely converging to a suboptimal solution.
5. Iteration: The process repeats for a defined number of iterations or until convergence.

CONTRIBUTING
------------

Contributions are welcome! If you'd like to contribute to this project, please fork the repository and submit a pull request with your changes.
