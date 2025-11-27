## Ex.No:5

## Ex.Name:Write a CPP function to print  the cheapest price from src to all other cities for the given graph. (Note: Source vertex is 0 always).

## Aim:
To write a CPP function to print  the cheapest price from src to all other cities for the given graph. (Note: Source vertex is 0 always).

## Algorithm:
1. Read number of vertices and edges.
2. Create adjacency list storing (neighbor, weight) pairs.
3. Initialize distance vector with INF and set distance of source (0) to 0.
4. Use a min-priority queue to process vertices with smallest distance first.
5. Pop vertex from queue, and update distances of neighbors if cheaper path found.
6. Repeat until queue is empty.
7. Print the shortest distance from source to all other vertices.

## Program:
```
void Graph::shortestPath(int src)
{
	set< pair<int, int> > setds;
	vector<int> dist(V, INF);
	setds.insert(make_pair(0, src));
	dist[src] = 0;
	while (!setds.empty())
	{
		pair<int, int> tmp = *(setds.begin());
		setds.erase(setds.begin());

	
		int u = tmp.second;
                	list< pair<int, int> >::iterator i;
		for (i = adj[u].begin(); i != adj[u].end(); ++i)
		{
			int v = (*i).first;
			int weight = (*i).second;
			if (dist[v] > dist[u] + weight)
			{
				
				if(dist[v]!=INF){
				    setds.erase(setds.find(make_pair(dist[v], v)));
				}
				// Write your condition here to complete the function
				
				
				dist[v] = dist[u] + weight;
				setds.insert(make_pair(dist[v], v));
			}
		}
	}

	// Print shortest distances stored in dist[]
	printf("Vertex Distance from Source\n");
	for (int i = 0; i < V; ++i)
		printf("%d  %d\n", i, dist[i]);
}
```


## Output:
<img width="793" height="807" alt="Screenshot 2025-11-04 214743" src="https://github.com/user-attachments/assets/bd88d470-8591-4ca3-bf00-745c009c3987" />

## Result:
Thus the program created successfully from src to all other cities for the given graph

