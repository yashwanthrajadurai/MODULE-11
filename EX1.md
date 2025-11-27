## Ex.No:1
## Ex.Name: Given a weighted, undirected and connected graph of V vertices and E edges. The task is to find the sum of weights of the edges of the Minimum Spanning Tree. Write the main function to generate the MST.
## Aim:
To write the main function to generate the MST


## Algorithm:
1. Start the program.
2. Read the number of vertices and edges.
3. Store all edges with their weights.
4. Sort edges in non-decreasing order of weight.
5. Use a Disjoint Set (Union-Find) to avoid cycles.
6. Pick smallest edge that doesn’t form a cycle and add it to MST.
7. Repeat until (V-1) edges are included.
8. Display the MST edges and total weight.
9. Stop the program

## Program:
```
int main()
{
	int V;
	int edges,vertices,u,v,w;
    cin>>vertices>>edges;
    V=vertices;
	Graph g(V);
	
    for(int i=0;i<edges;i++)
    {
        cin>>u>>v>>w;
        g.addEdge(u,v,w);
    }
    cout<<"Prim's MST edges are: ";
    g.primMST();
    
  
	return 0;
}
```


## Output:
<img width="753" height="795" alt="Screenshot 2025-11-04 212539" src="https://github.com/user-attachments/assets/689d7fb4-baf2-4843-84d6-fcc5e688db67" />

## Result:
Thus the program created successfully the main function to generate the MST.

