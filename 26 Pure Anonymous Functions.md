# 26. Pure Anonymous Functions

26.1 Use Range and a pure function to create a list of the first 20 squares


```
#^2 &[Range[20]]
```


```

```

26.2 Make a list of the result of blending yellow, green and blue with red.


```
Blend[{#, Red}] & /@ {Yellow, Green, Blue}
```


```

```

26.3 Generate a list of framed columns containing the upper case and lower case versions of each letter of the alphabet.


```
Framed[Column[{#, ToLowerCase[#]}]] & /@ Alphabet["English", "IndexCharacters"]
```


```

```

26.4 Make a list of letters of the alphabet, in random colors, with frames having random background colors.


```
Style[#, Background -> RandomColor[], 
   FontColor -> RandomColor[]] & /@ (Framed[#, FrameStyle -> Black, Background -> RandomColor[]] & /@ Alphabet[])
```


```

```

26.5 Make a table of G5 countries, together with their flags, and arrange the result in a fully framed grid


```

```


```

```

26.6 Make a list of word clouds for the Wikipedia articles about apple, peach and pear .


```

```


```

```

26.7 Make a list of histograms of the word lengths in Wikipedia articles on apple, peach and pear


```

```


```

```

26.8 Make a list of maps of Central America, highlighting each country in turn


```

```


```

```

+26.1 Give a simpler form for (#^2 + 1 &) /@ Range[10]
