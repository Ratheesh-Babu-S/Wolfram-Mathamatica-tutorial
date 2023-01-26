# 21 Graph and Networks

21.1 Make a graph consisting of a loop of 3 nodes


```Wolfram Language
Graph[{1 -> 2, 2 -> 3, 3 -> 1}]
```

Note:

21.2. Make a graph with 4 nodes in which every node is connected


```Wolfram Language
Graph[
 Flatten[
  Table[i -> j, {i, 4}, {j, 4}]]]
```

Note:

21.3. Make a table of undirected graphs with between 2 and 10 nodes in which every node is connected


```Wolfram Language
Table[
 UndirectedGraph[
  Flatten[
   Table[i -> j, {i, n}, {j, n}]]], {n, 2, 10, 1}]
```

Note:

21.4. Use Table and Flatten to get {1,2,1,2,1,2}


```Wolfram Language
Flatten[
 Table[
  FindShortestPath[
   Flatten[
    Table[
     Table[j -> i, {i, n}, {j, n}], {n, 2}]], 1, 2], 3]]
```

Note:

21.5. Make a line plot of the result of concatenating all digits of all integers from 1 to 100


```Wolfram Language
ListLinePlot[
 Flatten[
  IntegerDigits[
   Table[i, {i, 1, 100}]]]]
```

Note:

21.6. Make a graph with 50 nodes, in which node i connects to node i+1


```Wolfram Language
Graph[
 Flatten
  [Table[i -> i + 1, {i, 50}]]]
```

Note:

21.7. Make a graph with 4 nodes, in which each connection connects i to Max[i,j]


```Wolfram Language
Graph[
 Flatten[
  Table[i -> Max[i, j], {i, 4}, {j, 4}]]]
```

Note:

21.8. Make a graph in which each connection connects i to j-i, where i and j both range from 1 to 5


```Wolfram Language
Graph[
 Flatten[
  Table[i -> j - i, {i, 5}, {j, 5}]]]
```

Note:

21.9. Generate a graph with 100 nodes, each with a connection going to one randomly chosen node.


```Wolfram Language
Graph[
 Flatten[
  Table[i -> RandomInteger[50], {i, 100}]]]
```

Note:

21.10. Generate a graph with 100 nodes, each connecting to two randomly chosen nodes


```Wolfram Language

```

Note:

21.11. For the graph {1->2,2->3,3->4,4->1,3->1,2->2}, make a grid giving the shortest paths between every pair of nodes, with the start node as row and end node as column.


```Wolfram Language

```

Note:

+21.1. Make a graph with 4 nodes in which every node is connected, displaying the resulting graph with radial drawing.


```Wolfram Language
Graph[
 Flatten[
  Table[i -> j, {i, 3}, {j, 3}, 1]], VertexLabels -> All]
```

Note:

+21.2. Generate a graph in which a single node is connected to 10 others


```Wolfram Language
Graph[
 Flatten[
  Table[i - 1 -> j, {i, 1}, {j, 10}]]]
```

Note:

+21.3. Use flatten to generate a table of the numbers 1 to 50 in which even numbers are colored red.


```Wolfram Language
Style[Table[i*2, {i, 1, 25, 1}], Red]
```

Note:

UseImageData, Flatten and Total to find the number of white pixels in Binarize[Rasterize["W"]].


```Wolfram Language

```

Note:

UseFlatten, IntegerDigits and Total to find the sum of all digits of all whole numbers up to 1000.


```Wolfram Language

```

Note:

Generate a grap hwith 200 connections, each between nodes with numbers randomly chosen between 0 and 100.


```Wolfram Language

```

Note:

Generate a plot that shows communities in a random graph with nodes numbered between 0 and 100, and 200 connections


```Wolfram Language

```

Note:
