**Shortest Path Finder (Dijkstra-like)**


This is a Python implementation of a shortest path finder in a weighted undirected graph using a Dijkstra-like algorithm, that calculates and outputs the shortest distance and path between nodes.


**Features**


Works with any weighted undirected graph represented as an adjacency list


Calculates shortest paths from a start node to:


A specific target node, or


All other nodes if no target is specified


Outputs the distance and the path taken


Simple structure that is easy to modify or grow


**How It Works**


The graph is represented as a dictionary where:


The keys are the names of the nodes (Ex A, B)


The values are lists containing tuples in the form of (neighbor, weight)


The shortest_path function:


Inits distances and paths.


Iteratively updates each nodes shortest known distances.


Stores actual path taken.


Prints results for specific target nodes, target all nodes or print nothing.


**Example Graph**

my_graph = {
    'A': [('B', 5), ('C', 3), ('E', 11)],
    'B': [('A', 5), ('C', 1), ('F', 2)],
    'C': [('A', 3), ('B', 1), ('D', 1), ('E', 5)],
    'D': [('C', 1), ('E', 9), ('F', 3)],
    'E': [('A', 11), ('C', 5), ('D', 9)],
    'F': [('B', 2), ('D', 3)]
}

Calling the function:


shortest_path(my_graph, 'A', 'F')

will output:


A-F distance: 8
Path: A -> C -> B -> F  


**How to get started**

Clone the repo or copy the code into a .py file

Run with Python 3:

python3 shortest_path.py 


Edit the my_graph dictionary or function call as necessary

⚙**Function Signature** 
shortest_path(graph, start, target='') 


graph: The graph dictionary 

start: Starting node 

target: Target node to find the path to (optional field) 

If target is left blank the function will print distances/paths to every node 


**Notes**

The function assumes the graph is undirected 

The function does not leverage a priority queue like heapq, so it's not terribly optimized for large graphs. 

Great for educational/demo purposes or small graphs 

**License** 

This project is free and open source to use or alter.
