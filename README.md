Network Simulation with Data Transfer
Overview
This project simulates a computer network where multiple computers (nodes) are connected by routes (edges). It implements functionalities to add/remove computers, add routes between computers, and simulate data transfer between them. The shortest path between two computers is determined using Dijkstra's algorithm, and the transfer progress is displayed. The network can be saved, loaded from a file, and exported to a Graphviz .dot format for visualization.

Features
Add/Remove Computers: Dynamically add or remove computers from the network.

Add Routes: Add bidirectional routes between computers with specified weight (latency).

Dijkstra’s Algorithm: Find the shortest path between two computers based on the network topology.

Data Transfer Simulation: Simulate data transfer between two computers, displaying transfer progress.

Network Persistence: Save the network configuration to a file and load it back.

Network Export: Export the network topology to a Graphviz .dot file for visualization.

Requirements
C Compiler (e.g., GCC or MinGW)

Windows OS (since the code uses windows.h for Sleep function and file operations)

Compilation and Execution
Compile the code:
bash
Copy
Edit
gcc -o network_simulation network_simulation.c -lpthread
Run the program:
bash
Copy
Edit
./network_simulation
Menu Options
When the program runs, you will be prompted with a menu for different operations:

Add Computer: Adds a new computer to the network.

Remove Computer: Removes an existing computer from the network by its ID.

Add Route: Adds a bidirectional route between two computers with a specified weight (latency in milliseconds).

Transfer Data: Simulates the transfer of data between two computers, displaying the transfer progress and updating the file logs of the computers involved.

Exit: Exits the program.

Export Network Visualization: Exports the network topology to a .dot file for use with Graphviz.

Network Persistence
The network configuration is saved in the file network.txt, which contains the following:

The number of computers in the network.

The routes between the computers, including the destination and weight (latency).

File Logs
Each computer has a corresponding text file (computer_X.txt, where X is the computer ID). These files log the data sent and received by that computer.

Example entry in the file:

css
Copy
Edit
Sent 5 packets to 3
Received 5 packets from 0
Export to Graphviz
The network topology can be exported to a .dot file using the Export Network Visualization option. This file can be used with Graphviz to visualize the network.

To visualize the network, you can use Graphviz to generate a graph:

bash
Copy
Edit
dot -Tpng network.dot -o network.png
Threads and Data Transfer
The Transfer Data functionality uses a separate thread to simulate the data transfer process. The thread shows the transfer progress and updates the data sent and received counters.

Example Usage
Add a computer: Select option 1 to add a computer.

Add a route: Select option 3 and provide two computers and the route weight.

Transfer data: Select option 4 and enter the source, destination, and number of packets to be transferred.

Export the network: Select option 6 to generate a .dot file for visualization.

License
This project is open-source and available under the MIT License.


