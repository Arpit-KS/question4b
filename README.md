# question4b
Project: Dijkstra‑C by maximetinu
Implements Dijkstra’s shortest‑path algorithm using C.

Supports both terminal and CSV input/output, configurable via command‑line arguments.

Code is modularized into distinct responsibilities via three public interfaces:

dijkstra.h – core algorithm logic

IO_dijkstra.h – functions handling user or file input/output

graph_drawer.h – integration with Graphviz to optionally render shortest‑path graphs 


🧩 Code Structure & Function Breakdown
1. Core directory structure
src/ and include/ folders containing:

dijkstra.h / dijkstra.c – algorithm core

IO_dijkstra.h / IO_dijkstra.c – input/output utilities

graph_drawer.h / graph_drawer.c – optional Graphviz integration

2. dijkstra.h / dijkstra.c: Core algorithm
Initializes and manages distance arrays, visited sets, and predecessor tracking.

Implements main Dijkstra routine: pick the node with minimum tentative distance, relax neighbors, repeat until done.

Structured for maximum reusability via its clean API and abstraction from I/O


3. IO_dijkstra.h / .c: Input/output layer
Parses adjacency matrix from a CSV file or standard input.

Handles user interaction for selecting source and target nodes.

Outputs results either to console or writes to output file, optionally raw or verbose mode.

Separates I/O logic from core algorithm logic 


4. graph_drawer.h / .c: Graph visualization
Interfaces with Graphviz via the dot command if installed.

Produces graphical output of the computed shortest path.

Not mandatory—algorithm still runs without visualization



This layered approach isolates:

Algorithmic logic (pure Dijkstra’s)

Input/output handling

Optional graph rendering


Why This Project Stands Out
Modular design: concerns separated to keep code clean and maintainable

Multiple I/O modes: supports both console and file-based workflows

Extendable: core algorithm is reusable independently of I/O

Optional visualization: with Graphviz you can render graphs, but not required for core functionality

