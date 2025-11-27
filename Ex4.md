## Ex.No:4

## Ex.Name:Writ a CPP function to find the bipartite of a graph which is given by user.

## Aim:
To writ a CPP function to find the bipartite of a graph which is given by user.

## Algorithm:
1. Read number of vertices and edges.
2. Create adjacency list using vector of vectors.
3. Initialize a color array with -1 (uncolored).
4. For each uncolored vertex, perform BFS and color alternate levels with 0 and 1.
5. If a neighbor has the same color as current vertex, the graph is not bipartite.
6. If all vertices are colored successfully, the graph is bipartite.
   
## Program:
```
bool isBipartite(int V, vector<int> adj[])
{
    vector<int> col(V, -1);
 
    queue<pair<int, int> > q;
   
    for (int i = 0; i < V; i++)
    {
        if (col[i] == -1)
        {
            q.push({ i, 0 });
            col[i] = 0;
            while (!q.empty()) 
            {
                pair<int, int> p = q.front();
                q.pop();
            
                int v = p.first;
                int c = p.second;
                 
                for (int j : adj[v])
                {
                   
                    if (col[j] == c)
                        return 0;
                   
                    if (col[j] == -1)
                    {
                        col[j] = (c) ? 0 : 1;
                        q.push({ j, col[j] });
                    }
                }
            }
        }
    }
    return 1;
}
```


## Output:
<img width="706" height="787" alt="Screenshot 2025-11-04 214123" src="https://github.com/user-attachments/assets/de4fd914-cf19-4f67-9375-6e102f796386" />

## Result:
Thus the program created successfully to find the bipartite of a graph which is given by user.

