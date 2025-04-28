
# DAA Assignment 2

&nbsp;&nbsp;&nbsp;&nbsp;In this project we implement two algorithms for finding Densest subgraph discovery in an undirected graph in C++. The algorithms are:

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1. The algorithm 1 from page 1721 from the paper titled Efficient Algorithms for Densest Subgraph Discovery; by Yixiang Fang ,Kaiqiang Yu ,Reynold Cheng ,Laks V.S. Lakshmanan ,Xuemin Lin (Link: [https://www.vldb.org/pvldb/vol12/p1719-fang.pdf]).  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2. The algorithm 4 from page 1725 from the paper titled Efficient Algorithms for Densest Subgraph Discovery; by Yixiang Fang ,Kaiqiang Yu ,Reynold Cheng ,Laks V.S. Lakshmanan ,Xuemin Lin (Link: [https://www.vldb.org/pvldb/vol12/p1719-fang.pdf]).    

&nbsp;&nbsp;&nbsp;&nbsp;We then executed these algorithms on four graph datasets:  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1. as-Skitter (Link: https://snap.stanford.edu/data/as-Skitter.html)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2. Email-Enron (Link: https://snap.stanford.edu/data/email-Enron.html)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;3. Wiki-Vote (Link: https://snap.stanford.edu/data/wiki-Vote.html)    

&nbsp;&nbsp;&nbsp;&nbsp;We treated these datasets as undirected graphs and applied these algorithms. The input is taken from a text file with some optional text, including number of vertices, followed by edges, and the rest of the lines denoting a pair of vertices with an edge between them. We store the graphs in adjacency list format. The results are shown in the algorithm-wise markdowns, and the report.
&nbsp;&nbsp;&nbsp;&nbsp; Github Repository: https://github.com/DarkTalisman20/DAA-Assignment-1
&nbsp;&nbsp;&nbsp;&nbsp; Webpage Link: https://darktalisman20.github.io/DAA-Assignment-1/
## Contributions

&nbsp;&nbsp;&nbsp;&nbsp;The various tasks and their contributions are given below:  
&nbsp;&nbsp;&nbsp;&nbsp;1. Algorithm 1 implementation: Amritansh Tiwari
&nbsp;&nbsp;&nbsp;&nbsp;2. Algorithm 2 Implementation: Amritansh Tiwari 
&nbsp;&nbsp;&nbsp;&nbsp;4. Report: Sarthak , Abdul Rahman Yakoob 

## Run Locally

1.Download the zip file with codes from the submission.  
2. Download the dataset zip folder from the google drive link. (Link: [https://drive.google.com/drive/folders/16u1PDHzcSc9NJv8H8-DymsLPtUoBTNyt?usp=sharing](https://drive.google.com/drive/folders/16u1PDHzcSc9NJv8H8-DymsLPtUoBTNyt?usp=sharing)).  
3. Extract the dataset .txt files from the zip folder and put them in the same folder where all the codes are.  
4. Go to the project directory.  
5. Compile the file and run it.  

For Unix/Mac:

```bash
  g++ <file-name>.cpp -o <file-name>.out
  ./<file-name>.out <dataset>.txt
```

For Windows:

```bash
  g++ .cpp -o <file-name>.exe
  ./<file-name>.exe <dataset>.txt
```

Example for ELS with Wiki-Vote we input:  
```bash
  g++ els.cpp -o els.exe
  ./els.exe Wiki-Vote.txt
```

file-name can be tomita, or els, or chiba.  
dataset can be wiki-Vote or as-skitter or email-Enron.  
Webpage Link: [https://darktalisman20.github.io/DAA-Assignment-1/](https://darktalisman20.github.io/DAA-Assignment-1/)  
