# 24. More Forms of Visualization

24.1. Make a plot with lines joining the squares, the cubes and the 4th powers of integers up to 10


```Wolfram Language
a = Table[n^2, {n, 1, 10}];
b = Table[n^3, {n, 1, 10}];
c = Table[n^4, {n, 1, 10}];
ListLinePlot[{a, b, c}]
```

Note: 

24.2. Make a plot of the first 20 primes, joined by a line, filled to the axis and with a red dot at each prime


```Wolfram Language
ListLinePlot[
 Table[Prime[n], {n, 20}], Mesh -> Automatic, MeshStyle -> Red]
```

Note:

24.3. Make a 3D plot of the topography for 20 miles around Mount Fuji


```Wolfram Language
ListPlot3D[
 GeoElevationData[
  GeoDisk[Entity["Mountain", "FujiSan"], Quantity[100, "Miles"]]]]
```

Note:

 24.4 Make a relief plot of the topography for 100 miles around Mount Fuji


```Wolfram Language
ReliefPlot[
 GeoElevationData[
  GeoDisk[Entity["Mountain", "FujiSan"], Quantity[100, "Miles"]]]]
```

Note:

24.5 Make a 3 D plot of heights generated from Mod[i,j] with i and j going up to 100


```Wolfram Language
ListPlot3D[
 Table[Mod[i, j], {i, 1, 100}, {j, 1, 100}]]
```

Note:

24.6 Make a histogram of the differences between successive primes for the first 10000 primes


```Wolfram Language
a = Table[Prime[n], {n, 1, 10000}];
Histogram[Table[Abs[Part[a, b] - Part[a, b + 1]], {b, 1, 9999}]]
```

Note:

24.7 Make a histogram of the first digits of squares of integers up to 10000


```Wolfram Language
Histogram[Table[First[IntegerDigits[n^2]], {n, 10000}]]
```

Note:

24.8 Make a histogram of the length of Roman numerals up to 1000


```Wolfram Language
Histogram[Table[StringLength[RomanNumeral[n]], {n, 1000}]]
```

Note:

24.9 Make a histogram of sentence lengths in the Wikipedia article on computers


```Wolfram Language
Histogram[StringLength[TextSentences[WikipediaData["Computers"]]]]
```

Note:

24.10 Make a list of histograms of 10000 instances of totals of n random reals up to 100, with n going from 1 to 5 (illustrating the central limit theorem)


```Wolfram Language
Table[
    Histogram[
        Table[
            Total[
                RandomReal[100, n] (* generate n random numbers in the interval [0, 100] *)
           ] (* sum these n numbers *)
        , 10000] (* do this 10000 times *)
    ] (* make a historgram of these 10000 summed values *)
, {n, 1, 5}] (* generate histograms with n in {1, 2, 3, 4, 5} *)
```


```Wolfram Language
Note: 
```

24.11 Generate a 3 D list plot using the image data from a binarized size - 200 letter "w" as heights


```Wolfram Language
ListPlot3D[ImageData[Binarize[Rasterize[Style["W", 200]]]]]
```

Note:

24.12 Make a histogram of word lengths in the Wikipedia article on computers 


```Wolfram Language
Histogram[StringLength[TextWords[WikipediaData["Computers"]]]]
```

Note:
