# Experimental Results

The implementations were tested on several datasets. We ran the implementations of the three algorithms on four datasets. The code was executed on a Macbook Air 1, with 8 GB RAM; execution time may differ for different devices. The datasets, with their names, number of edges, and vertices, are as follows:

| Dataset      | Vertices | Edges  |
|--------------|----------|--------|
| As733        | 6474     | 13895  |
| Netscience   | 1461     | 2742   |
| Yeast        | 1458     | 1948   |
| Ca-HepTh     | 9877     | 51971  |

---

Both the algorithms returned the same results for densities of densest subgraph, number of nodes, and number of h-cliques. The results are as follows:

## Densities of k-clique densest subgraph

| Result    | As733   | NetScience | Yeast    | Ca-HepTh  |
|-----------|---------|------------|----------|-----------|
| 2-Clique  | 8.875   | 9.5        | 2.71429  | 15.5      |
| 3-Clique  | 35.9091 | 57         | 3.71429  | 155       |
| 4-Clique  | 85.125  | 242.25     | 2.71429  | 1123.75   |
| 5-Clique  | 126.767 | 775.2      | 1        | 6293      |

---

## Number of vertices in the densest subgraph

| Result    | As733 | NetScience | Yeast | Ca-HepTh |
|-----------|-------|------------|-------|----------|
| 2-Clique  | 40    | 20         | 7     | 9877     |
| 3-Clique  | 33    | 20         | 7     | 9877     |
| 4-Clique  | 32    | 20         | 7     | 9877     |
| 5-Clique  | 30    | 20         | 7     | 9877     |

---

## Number of h-cliques in the densest subgraph

| Result    | As733 | NetScience | Yeast | Ca-HepTh |
|-----------|-------|------------|-------|----------|
| 2-Clique  | 355   | 20         | 7     | 496      |
| 3-Clique  | 1185  | 20         | 7     | 4960     |
| 4-Clique  | 2724  | 20         | 7     | 35960    |
| 5-Clique  | 3803  | 20         | 7     | 201376   |

---

## Execution Times in milliseconds

| Clique size | Algorithm  | As733      | NetScience | Yeast     | Ca-HepTh   |
|-------------|------------|------------|------------|-----------|------------|
| 2-Clique    | Exact      | 288229 ms (4.5 min) | 11523 ms (0.19 min) | 9087 ms (0.16 min) | 603314 ms (~10 min) |
|             | CoreExact  | 261796 ms (4.3 min) | 1516 ms (0.025 min) | 9158 ms (0.16 min) | 576454 ms (9.6 min) |
| 3-Clique    | Exact      | 633709 ms (10.5 min) | 23619 ms (0.39 min) | 12414 ms (0.21 min) | 1853753 ms (~30.8 min) |
|             | CoreExact  | 571231 ms (9.5 min) | 3060 ms (0.051 min) | 12791 ms (0.22 min) | 1820999 ms (~30.3 min) |
| 4-Clique    | Exact      | 367144 ms (6.1 min) | 36212 ms (0.60 min) | 1992 ms (0.033 min) | 2302033 ms (~38.37 min) |
|             | CoreExact  | 343926 ms (5.7 min) | 5058 ms (0.084 min) | 708 ms (0.012 min)  | 2269619 ms (~37.82 min) |
| 5-Clique    | Exact      | 354023 ms (5.9 min) | 74719 ms (1.25 min) | 941 ms (0.016 min)  | 6210599 ms (~103.51 min) |
|             | CoreExact  | 318915 ms (5.3 min) | 5712 ms (0.096 min) | 1025 ms (0.0171 min) | 6171616 ms (~102.86 min) |

---

As we can see from the execution times, the time taken increases with an increase in the number of vertices and edges in the graph. The smallest dataset (Yeast) took less than a fourth of a minute for all the values of h and both algorithms. In contrast, the largest dataset (Ca-HepTh) took more than 100 minutes for 5-Clique enumeration. For most cases, CoreExact is faster than Exact. The possible reason for exceptions is that clique enumeration took more time than the time gained by pruning the search space to find densest subgraphs.

