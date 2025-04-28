# Algorithms
## Algorithm 1

Algorithm 1 (Exact) is the baseline exact algorithm for solving the Clique Densest Subgraph (CDS) problem, which aims to find a subgraph with the highest h-clique-density. It uses a binary search approach combined with flow network techniques.
Here's how the Exact algorithm works:

&nbsp;&nbsp;&nbsp;&nbsp;It initializes lower and upper bounds for the density parameter α. The lower bound is set to 0, and the upper bound is calculated as the maximum clique-degree of any vertex divided by the clique size.
The algorithm creates a flow network F(V_F, E_F) with:  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;A source node s and a sink node t.  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Nodes representing all vertices in the original graph.  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Directed edges from s to each vertex with capacity equal to that vertex's clique-degree.  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Directed edges between vertices that form (h-1)-cliques, with capacity set to infinity.  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Directed edges from each vertex to t with capacity α.  


&nbsp;&nbsp;&nbsp;&nbsp;It performs binary search on the parameter α:

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;In each iteration, it builds the flow network with the current α value.  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Computes the minimum s-t cut (S,T) using Goldberg's algorithm.  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Updates α based on the result:  

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;If S={s}, then α is too large, so the upper bound is updated.  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Otherwise, α is too small, so the lower bound is updated.  




&nbsp;&nbsp;&nbsp;&nbsp;The algorithm terminates when the gap between upper and lower bounds becomes sufficiently small, and returns the subgraph D induced by the set S{s}.  

The paper notes that while Exact provides optimal solutions, it has limitations:  

&nbsp;&nbsp;&nbsp;&nbsp;Initial bounds on α may not be tight.
&nbsp;&nbsp;&nbsp;&nbsp;The flow network can become large for graphs with many clique instances.
&nbsp;&nbsp;&nbsp;&nbsp;The algorithm rebuilds the flow network on the entire graph in each iteration.

These limitations are addressed in Algorithm 4 (CoreExact), which improves efficiency through the core-based approach.

## Algorithm 4

Algorithm 4 (CoreExact) is an optimized approach for solving the Clique Densest Subgraph (CDS) problem, which aims to find a subgraph with the highest h-clique-density. The algorithm improves upon the basic Exact algorithm by leveraging k-clique-cores and several optimization techniques to reduce computational cost.
Here's how CoreExact works:

It begins by performing core decomposition using Algorithm 3, which computes the clique-core number of each vertex.
It then locates the (k'', Ψ)-core using pruning criteria, where k'' represents the core with the highest h-clique-density among residual graphs.
The algorithm initializes a set C to contain all connected components of the (k'', Ψ)-core that might contain the CDS.
For each connected component in C, it:

Builds a flow network if the component's core number is high enough
Performs binary search to find the optimal α value
Uses minimum s-cut calculations to identify dense subgraphs
Updates bounds as the search progresses


The algorithm employs three key optimizations:

Tighter bounds on α using (k,Ψ)-cores
Pruning techniques to identify which cores might contain the CDS
A strategy to make the flow network gradually smaller during iterations


Finally, it returns the subgraph D with the highest h-clique-density.

The main advantage of CoreExact over the basic Exact algorithm is efficiency - it significantly reduces computational cost by:

Working with smaller subgraphs (cores) rather than the entire graph
Using tighter bounds for binary search
Progressively reducing the flow network size
