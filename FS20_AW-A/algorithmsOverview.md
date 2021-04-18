# Algorithms

## Graphs

### DFS
- Runtime: $O(|V| + |E|)$

### Prim
- Runtime: $O((|V| + |E|) \ln |V|)$

### Kruskal
- Runtime: $O(|E| \log |V|)$

### Find Articulation Point (/Bridges)
- Key Idea:
    - Assign $dfs[v] \forall v \in V$
    - Calculate $low[v] \forall v \in V$
    - Determine $isArtriculationPoint[v] \forall v \in V$
- Runtime: $O(|E|)$

### Greedy-Matching (inklusionsmaximal)
- Runtime: $O(|E|)$
- Note: $|M_{\text{Greedy}}| \ge \frac{1}{2}|M^*|$

### Kardinalitätsmaximales Matching
- Runtime: $O(|E| \cdot \sqrt{|V|})$

### Eulertour
- Precondition: Graph is zusammenhängend and eulerisch
- Key Idea:
    - Runner runs as long as there are unvisited edges left
    - Turtle follows path, and starts runner at a junction
    - Merge cycles
- Runtime: $O(|E|)$

### Hamiltonkreis
- Key Idea:
    - DP
- Runtime: $O(|V|^2 \cdot 2^{|N|})$
- Speicher: $O(|V| \cdot 2^{|N|})$

### Metric TSP 2 Approx.
- Key Idea:
    - Find MST
    - Double all edges
    - Walk along the edges and skip edges leading to already visited nodes.
- Runtime: $O(|V|^2)$

### Metric TSP 1.5 Approx.
- Key Idea:
    - Find MST
    - $S$ contains all nodes with odd degree
    - Find minimal perfect matching on $S$
    - Walk along the edges and skip edges leading to already visited nodes.
- Runtime: $O(|V|^3)$

### Greedy-Coloring
- Note: Uses at most $\Delta G + 1$ colors
- Runtime: $O(|E|)$

### Bunt
- Note: $k = O(\log n)$
- Runtime: $O(2^kkm)$

### Zufallsfärbung
- Key Idea:
    - Color nodes in $[k := B + 1]$ colors to find a path of length $B$
    - Check if there is a colorful path of length $k - 1$
    - If failed, repeat with new random coloring
- Note: Monte Carlo
- Runtime: $O(\lambda (2e)^k km)$

### Forld-Fulkerson
- Note:
    - Grantees to terminate for integer capacities
    - Capacities are less than $U$
- Key Idea:
    - Find augmenting path
    - Increase flow on path
- Runtime: $O(U |E| |V|)$

### Capacity Scaling
- Note: Capacity are integers and less than $U$
- Runtime: $O(nm(1 + \log U)$

### Dynamic Trees
- Runtime: $O(mn \log n)$

### Cut
- Runtime: $O(n^2)$

### CutBootstrapping
- Runtime: $O(n^2 \cdot poly \cdot \log n)$

### CompleteEnumeration
- Key Idea: Select subset of $3$ points and test if circle contains all other points
- Runtime: $O(n^4)$

### CompleteEnumerationClever
- Key Idea: Select $11$ points at random and construct $C$. Double all points lying outside of $C$
- Runtime: $O(n \log n)$

### Jarvis-Wrap
- Runtime: $O(hn)$

### LocalRepair
- Note: Points are ordered according to their $x$ coordinate.
- Runtime: $O(n)$
