# 23 More About Numbers

23.1 Find Sqrt[2] 500-digit precision


```Wolfram Language
N[Sqrt[2], 500]
```

Note:

23.2 Generate 10 random real numbers between 0 and 1


```Wolfram Language
RandomReal[{0, 1}, 10]
```

Note:

23.3 Make a plot of 200 points with random real x and y coordinates between 0 and 1


```Wolfram Language
ListPlot[RandomReal[{0, 1}, {200, 2}]]
```

Note:

23.4 Create a random walk using AnglePath and 1000 random real numbers between 0 and 2\[Pi]


```Wolfram Language
Graphics[
 Line[
  AnglePath[RandomReal[{0, 2 Pi}, 1000]]]]
```

Note:

23.5 Make a table of Mod[n^2,10] for n from 0 to 30.


```Wolfram Language
Table[Mod[n^2, 10], {n, 0, 30}]
```

Note:

23.6 Make a line plot of Mod[n^2,10] for n from 1 to 100


```Wolfram Language
ListLinePlot[
 Table[Mod[n^n, 10], {n, 1, 100}]]
```

Note:

23.7 Make a table of the first 10 powers of \[Pi], rounded to integers.


```Wolfram Language
Table[Round[Pi^n], {n, 10}]
```

Note:

23.8 Make a graph by connecting n with Mod[n^2,100] for n from 0 to 99


```Wolfram Language
Graph[
 Table[n -> Mod[n^2, 100], {n, 0, 99}]]
```

Note:

23.9 Generate a graphics of 50 circles with random real coordinates 0 to 10, random real radii from 0 to 2, and random colors.


```Wolfram Language
Graphics[
 Table[
  Style[
   Circle[
    RandomReal[10, 2], RandomReal[2]], RandomColor[]], 50]]
```

Note:

23.10  Make a plot of the nth prime divided by n*log(n), for n from 2 to 1000.


```Wolfram Language
ListPlot[Table[N[Prime[n]/(n*Log[n])], {n, 2, 1000}]]
```

Note:

23.11 Make a line plot of the differences between successive primes up to 100


```Wolfram Language
a = Table[Prime[n], {n, 1, 100}];
ListLinePlot[
 Table[
  Abs[
   Part[a, b] - Part[a, b + 1]], {b, 1, 99}]]
```

Note:

23.13 Make an array plot of Mod[i,j] for i and j up to 50


```Wolfram Language
ArrayPlot[
 Table[
  Mod[i, j], {i, 50}, {j, 50}]]
```

Note:

23.14 Make a list for n from 2 to 10 of array plots for x and y up to 50 x^y mod n.


```Wolfram Language

```

Note:

23.15 Use Round to compute the fractional part of pi to 50 digits


```Wolfram Language
Round[FractionalPart[Pi], 10^-50]
```

Note:
