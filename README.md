Network Simulation with Data Transfer

Overview
This project simulates a computer network where multiple computers (nodes) are connected by routes (edges). It implements functionalities to add/remove computers, add routes between computers, and simulate data transfer between them. The shortest path between two computers is determined using Dijkstra's algorithm, and the transfer progress is displayed. The network can be saved, loaded from a file, and exported to a Graphviz .dot format for visualization.


Features :

1.Add/Remove Computers: Dynamically add or remove computers from the network.

2.Add Routes: Add bidirectional routes between computers with specified weight (latency).

3.Dijkstra’s Algorithm: Find the shortest path between two computers based on the network topology.

4.Data Transfer Simulation: Simulate data transfer between two computers, displaying transfer progress.

5.Network Persistence: Save the network configuration to a file and load it back.

6.Network Export: Export the network topology to a Graphviz .dot file for visualization.



Requirements :

C Compiler (e.g., GCC or MinGW)

Windows OS (since the code uses windows.h for Sleep function and file operations)



Compilation and Execution

Compile the code: gcc -o network_simulation network_simulation.c -lpthread

Run the program: ./network_simulation

To visualize the network, you can use Graphviz to generate a graph: dot -Tpng network.dot -o network.png



License

This project is open-source and available under the MIT License.


