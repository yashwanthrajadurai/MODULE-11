## Ex.No:2
## Ex.Name:Write a CPP function to add edge and weight of the above graph to find MST.

## Aim:
To write a CPP function to add edge and weight of the above graph to find MST.

## Algorithm:
1. Create a vector to store all edges.
2. Define a function to take start vertex, end vertex, and weight.
3. Add the edge to the vector.
4. Repeat for all edges of the graph.
5. Use this vector later to compute MST.

## Program:
```
void addEdge(int x, int y, int w)
	{
		edgelist.push_back({ w, x, y });
	}
```


## Output:
<img width="1125" height="811" alt="Screenshot 2025-11-04 213400" src="https://github.com/user-attachments/assets/be031ce6-aac6-4585-b127-be877b5707b8" />

## Result:
Thus the program created successfully to add edge and weight of the above graph to find MST.

