## Ex.No:3
## Ex.Name:Write a CPP code to print shortest distances in the program to find Dijkstra's shortest path from A to all other vertices.

## Aim:
To write a CPP code to print shortest distances in the program to find Dijkstra's shortest path from A to all other vertices.

## Algorithm:
1. Start the program.
2. Read number of vertices and edges.
3. Create an adjacency list storing pairs (neighbor, weight).
4. Initialize a distance vector with INF and set distance of source to 0.
5. Use a min-priority queue to process vertices with smallest distance first.
6. Pop a vertex from queue, and update distances of adjacent vertices if shorter path found.
7. Repeat until the queue is empty.
8. Print the shortest distances from source to all vertices.
9. Stop the program

## Program:
```
cout<<"Vertex Distance from Source\n";
	for (int i = 0; i < V; ++i)
		cout<<char(i + 65)<<" "<<dist[i]<<"\n";
		}
```


## Output:
<img width="1125" height="811" alt="Screenshot 2025-11-04 213400" src="https://github.com/user-attachments/assets/54c75ef9-bec2-429c-b77c-274c48b470ba" />

## Result:
Thus the program created successfully to find Dijkstra's shortest path from A to all other vertices.

