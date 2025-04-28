
# DAA Assignment 2

&nbsp;&nbsp;&nbsp;&nbsp;In this project we implement two algorithms for finding Densest subgraph discovery in an undirected graph in C++. The algorithms are:

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1. The algorithm 1 from page 1721 from the paper titled Efficient Algorithms for Densest Subgraph Discovery; by Yixiang Fang ,Kaiqiang Yu ,Reynold Cheng ,Laks V.S. Lakshmanan ,Xuemin Lin (Link: [https://www.vldb.org/pvldb/vol12/p1719-fang.pdf]).  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2. The algorithm 4 from page 1725 from the paper titled Efficient Algorithms for Densest Subgraph Discovery; by Yixiang Fang ,Kaiqiang Yu ,Reynold Cheng ,Laks V.S. Lakshmanan ,Xuemin Lin (Link: [https://www.vldb.org/pvldb/vol12/p1719-fang.pdf]).    

&nbsp;&nbsp;&nbsp;&nbsp;We then executed these algorithms on four graph datasets:  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1. As733  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2. Yeast  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;3. Ca-HepTh  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;4. NetScience  


&nbsp;&nbsp;&nbsp;&nbsp;We treated these datasets as undirected graphs and applied these algorithms. The input is taken from a text file with some optional text, including number of vertices, followed by edges, and the rest of the lines denoting a pair of vertices with an edge between them. We store the graphs in adjacency list format. The results are shown in the algorithm-wise markdowns, and the report.  
&nbsp;&nbsp;&nbsp;&nbsp; Webpage Link:  [https://Saarthek-Raj.github.io/DAA-Assignment-2/]
## Contributions

&nbsp;&nbsp;&nbsp;&nbsp;The various tasks and their contributions are given below:    
&nbsp;&nbsp;&nbsp;&nbsp;1. Algorithm 1 implementation: Amritansh   
&nbsp;&nbsp;&nbsp;&nbsp;2. Algorithm 2 Implementation: Amritansh  
&nbsp;&nbsp;&nbsp;&nbsp;3. Report: Saarthek Raj , Abdul Rahman Yakoob 


## Run Locally

1.Download the zip file with codes from the submission.  
2. Download the dataset zip folder from the google drive link. (Link: https://drive.google.com/drive/folders/1GZz6tX6ZHZ5rjc-O70JKMAp1rdhZ5Ech).  
3. Extract the dataset .txt files from the zip folder and put them in the same folder where all the codes are.  
4. Go to the project directory.  
5. Compile the file and run it.  

For Unix/Mac:

```bash
  g++ <file-name>.cpp -o <file-name>.out 
  ./<file-name>.out <dataset>.txt <h>
```

For Windows:

```bash
  g++ <file-name>.cpp -o <file-name>.exe
  ./<file-name>.exe <dataset>.txt <h>
```
`<file-name>` can be algo1 or algo4, and `<h>` is number of vertices in the clique.
Example for Algorithm 1 with Yeast for edge-based density we input:  
```bash
  g++ algo1.cpp -o algo1.exe
  ./algo1.exe yeast.txt 2
```
