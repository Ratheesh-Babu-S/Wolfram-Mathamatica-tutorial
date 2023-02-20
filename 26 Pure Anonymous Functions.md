# 26. Pure Anonymous Functions

26.1 Use Range and a pure function to create a list of the first 20 squares


```Wolfram Language
#^2 &[Range[20]]
```

Note:

26.2 Make a list of the result of blending yellow, green and blue with red.


```Wolfram Language
Blend[{#, Red}] & /@ {Yellow, Green, Blue}
```

Note:

26.3 Generate a list of framed columns containing the upper case and lower case versions of each letter of the alphabet.


```Wolfram Language
Framed[Column[{#, ToLowerCase[#]}]] & /@ Alphabet["English", "IndexCharacters"]
```

Note:

26.4 Make a list of letters of the alphabet, in random colors, with frames having random background colors.


```Wolfram Language
Style[#, Background -> RandomColor[], 
   FontColor -> RandomColor[]] & /@ (Framed[#, FrameStyle -> Black, Background -> RandomColor[]] & /@ Alphabet[])
```

Note:

26.5 Make a table of G5 countries, together with their flags, and arrange the result in a fully framed grid


```Wolfram Language
Grid[{#, EntityValue[#, "Flag"]} & /@ CountryData["G5"], Frame -> All]
```

Note:

26.6 Make a list of word clouds for the Wikipedia articles about apple, peach and pear .


```Wolfram Language

```

Note:

26.7 Make a list of histograms of the word lengths in Wikipedia articles on apple, peach and pear


```Wolfram Language

```

Note:

26.8 Make a list of maps of Central America, highlighting each country in turn


```Wolfram Language

```

Note:

+26.1 Give a simpler form for (#^2 + 1 &) /@ Range[10]


```Wolfram Language

```

Note:
