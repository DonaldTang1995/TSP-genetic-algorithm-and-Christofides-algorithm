The project is a genetic algorithm to solve the TSP problem.

Christofides algorithm is used to initialize the gene and genetic algorithm runs.
Christofides algorithm:
1.get the minumum spanning tree of the graph
2.find all vertexes with odd degree in the minumum spanning tree
3.find a perfect matching of those vertexes in step 2
4.find euler tour
5.remove the repeated vertex
genetic algorithm:
initialize: put one gene generated by Christofides algorithm into the gene pool and randomly generate the rest.
encode: 1,2,3,4...n represents a tour from 1 to n.
select: sort the gene pool according to the score, for ith gene,it has the probability of i/sum(1..n) to be selected.
cross: randomly some pair of gene, randomly exchange their gene code.
mutation: randomly swap 2 numbers in a gene.

To use this program:
make
./TSP_Solver filename1 filename2..

In makefile, set $DEBUG to -DDEBUG, the program will output the middle result

If the number of vertexes is less than 1000, the program will run 600s, otherwise, the program will run 1200s.

Tested on ubuntu 14.04LTS,g++ 4.8.4