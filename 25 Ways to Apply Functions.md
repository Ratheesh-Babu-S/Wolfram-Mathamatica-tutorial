# 25. Ways to Apply Functions

25.1. Use /@ and Range to reproduce the result of Table[f[n],{n,5}]


```Wolfram Language
f /@ Range[5]
```

Note:

25.2. Use /@ twice to generate Table[f[g[n]],{n,10}]


```Wolfram Language
f /@ g /@ Range[10]
```

Note:

25.3. Use // to create a[b[c[d[x]]]]


```Wolfram Language
x // d // c // b // a
```

Note:

25.4. Make a list of letters of the alphabet, with a frame around each one


```Wolfram Language
Framed /@ Alphabet[]
```

Note:

25.4. Color negate an image of each planet, giving a list of the results


```Wolfram Language
ColorNegate /@ EntityValue[EntityClass["Planet", All], "Image"]
```

Note:

25.6. Use /@ to draw separate maps of each country in the G5.


```Wolfram Language
GeoGraphics/@EntityList[EntityClass["Country","GroupOf5"],"Map"]
```

Note:

25.7. Binarize each flag in Europe, and make an image collage of the result.


```Wolfram Language
ImageCollage[Binarize/@EntityValue[EntityClass["GeographicRegion","Europe"["Countries"],"Flag"]]]
```

Note:

Find a list of the dominant colors in images of the planets, putting the results for each planet in a column.


```Wolfram Language
Column/@DominantColors[EntityValue[EntityClass["Planets","All"],"Image"]]
```

Note:

25.9 Find the total of the letter numbers given by Letter Number for the letters in the word  "wolfram"


```Wolfram Language
LetterNumber[Characters["Wolfram"]] // Total
```

Note:
