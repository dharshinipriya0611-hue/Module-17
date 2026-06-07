# Ex. No: 17A - Generate a Graph for a Given Fixed Degree Sequence

## AIM:
To write a Python program to demonstrate the adjacency list representation of the given graph.

## ALGORITHM:
1. Start the program.
2. Define a class AdjNode to create a node for each adjacent vertex:
3. Store the vertex number. Store the link to the next adjacent node. Step 3: Define a class Graph to create the graph using adjacency lists:

4. Initialize the number of vertices. Create a list (array) of size V, where each element is initially None. Step 4: Define a method add_edge(src, dest) to:

5. Add dest to the adjacency list of src. Add src to the adjacency list of dest (for undirected graphs). Step 5: Define a method print_graph() to:
6. Traverse the adjacency list of each vertex. Print the vertex and its adjacent nodes. Step 6: In the main program:
7. Create a Graph object with V vertices. Call add_edge() for all desired edges. Call print_graph() to display the adjacency list. Step 7: End the program.

## PYTHON PROGRAM
~~~
name: D Dharshini priya 
reg.no:212223090004


class AdjNode:
	def __init__(self, data):
		self.vertex = data
		self.next = None

class Graph:
	def __init__(self,vertices):
		self.V = vertices
		self.graph = [None]*self.V

	
	def add_edge(self, src, dest):
		# Adding the node to the source node
		node = AdjNode(dest)
		node.next = self.graph[src]
		self.graph[src] = node
		node = AdjNode(src)
		node.next = self.graph[dest]
		self.graph[dest] = node

	
	def print_graph(self):
	  
		for i in range(self.V):
			print("Adjacency list of vertex {}\n {}".format(i,i), end="")
			temp = self.graph[i]
			while temp:
				print(" -> {}".format(temp.vertex), end="")
				temp = temp.next
			print(" \n")
if __name__ == "__main__":
	V = 5
	graph = Graph(V)
	graph.add_edge(0, 1)
	graph.add_edge(0, 4)
	graph.add_edge(1, 2)
	graph.add_edge(1, 3)
	graph.add_edge(1, 4)
	graph.add_edge(2, 3)
	graph.add_edge(3, 4)

	graph.print_graph()
~~~

## OUTPUT
<img width="624" height="485" alt="image" src="https://github.com/user-attachments/assets/7896126f-eeed-4202-8c24-c8860accb50f" />


## RESULT
Thus the program is created and verified.
