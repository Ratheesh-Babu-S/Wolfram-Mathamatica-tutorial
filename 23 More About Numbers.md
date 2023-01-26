{
 "cells": [
  {
   "cell_type": "markdown",
   "id": "2325e347",
   "metadata": {},
   "source": [
    "# 23 More About Numbers"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "4b5fa7a5",
   "metadata": {},
   "source": [
    "23.1 Find Sqrt[2] 500-digit precision"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "7a460fbf",
   "metadata": {},
   "outputs": [],
   "source": [
    "N[Sqrt[2], 500]"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "2147ee88",
   "metadata": {},
   "source": [
    "Note:"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "20c38286",
   "metadata": {},
   "source": [
    "23.2 Generate 10 random real numbers between 0 and 1"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "a9cb79d2",
   "metadata": {},
   "outputs": [],
   "source": [
    "RandomReal[{0, 1}, 10]"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "b4d9ede1",
   "metadata": {},
   "source": [
    "Note:"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "84ed3b89",
   "metadata": {},
   "source": [
    "23.3 Make a plot of 200 points with random real x and y coordinates between 0 and 1"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "415c2ef6",
   "metadata": {},
   "outputs": [],
   "source": [
    "ListPlot[RandomReal[{0, 1}, {200, 2}]]"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "42b9c607",
   "metadata": {},
   "source": [
    "Note:"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "c3ffd058",
   "metadata": {},
   "source": [
    "23.4 Create a random walk using AnglePath and 1000 random real numbers between 0 and 2\\[Pi]"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "3c58953e",
   "metadata": {},
   "outputs": [],
   "source": [
    "Graphics[\n",
    " Line[\n",
    "  AnglePath[RandomReal[{0, 2 Pi}, 1000]]]]"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "4b6924cd",
   "metadata": {},
   "source": [
    "Note:"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "2b990728",
   "metadata": {},
   "source": [
    "23.5 Make a table of Mod[n^2,10] for n from 0 to 30."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "3eddc8d1",
   "metadata": {},
   "outputs": [],
   "source": [
    "Table[Mod[n^2, 10], {n, 0, 30}]"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "bdd7f134",
   "metadata": {},
   "source": [
    "Note:"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "3b4f9f21",
   "metadata": {},
   "source": [
    "23.6 Make a line plot of Mod[n^2,10] for n from 1 to 100"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "623936db",
   "metadata": {},
   "outputs": [],
   "source": [
    "ListLinePlot[\n",
    " Table[Mod[n^n, 10], {n, 1, 100}]]"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "9bdea380",
   "metadata": {},
   "source": [
    "Note:"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "4e16ec4c",
   "metadata": {},
   "source": [
    "23.7 Make a table of the first 10 powers of \\[Pi], rounded to integers."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "804208b3",
   "metadata": {},
   "outputs": [],
   "source": [
    "Table[Round[Pi^n], {n, 10}]"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "776ed1a8",
   "metadata": {},
   "source": [
    "Note:"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "c7bccc49",
   "metadata": {},
   "source": [
    "23.8 Make a graph by connecting n with Mod[n^2,100] for n from 0 to 99"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "eff5e374",
   "metadata": {},
   "outputs": [],
   "source": [
    "Graph[\n",
    " Table[n -> Mod[n^2, 100], {n, 0, 99}]]"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "f1217312",
   "metadata": {},
   "source": [
    "Note:"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "015295bc",
   "metadata": {},
   "source": [
    "23.9 Generate a graphics of 50 circles with random real coordinates 0 to 10, random real radii from 0 to 2, and random colors."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "230d34c6",
   "metadata": {},
   "outputs": [],
   "source": [
    "Graphics[\n",
    " Table[\n",
    "  Style[\n",
    "   Circle[\n",
    "    RandomReal[10, 2], RandomReal[2]], RandomColor[]], 50]]"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "b446dc49",
   "metadata": {},
   "source": [
    "Note:"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "f9a15850",
   "metadata": {},
   "source": [
    "23.10  Make a plot of the nth prime divided by n*log(n), for n from 2 to 1000."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "e07a128c",
   "metadata": {},
   "outputs": [],
   "source": [
    "ListPlot[Table[N[Prime[n]/(n*Log[n])], {n, 2, 1000}]]"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "84f45a94",
   "metadata": {},
   "source": [
    "Note:"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "fef45386",
   "metadata": {},
   "source": [
    "23.1 Make a line plot of the differences between successive primes up to 100"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "ad914e63",
   "metadata": {},
   "outputs": [],
   "source": [
    "a = Table[Prime[n], {n, 1, 100}];\n",
    "ListLinePlot[\n",
    " Table[\n",
    "  Abs[\n",
    "   Part[a, b] - Part[a, b + 1]], {b, 1, 99}]]"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "7e2684d1",
   "metadata": {},
   "source": [
    "Note:"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "2050a352",
   "metadata": {},
   "source": [
    "23.13 Make an array plot of Mod[i,j] for i and j up to 50"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "6d31aaf9",
   "metadata": {},
   "outputs": [],
   "source": [
    "ArrayPlot[\n",
    " Table[\n",
    "  Mod[i, j], {i, 50}, {j, 50}]]"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "a91e20c5",
   "metadata": {},
   "source": [
    "Note:"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "40870777",
   "metadata": {},
   "source": [
    "23.15 Make a list for n from 2 to 10 of array plots for x and y up to 50 x^y mod n."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "334f30a0",
   "metadata": {},
   "outputs": [],
   "source": []
  },
  {
   "cell_type": "markdown",
   "id": "5ac6728e",
   "metadata": {},
   "source": [
    "Note:"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "d0f97afd",
   "metadata": {},
   "source": [
    "23.16 Use Round to compute the fractional part of pi to 50 digits"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "c6edbbbd",
   "metadata": {},
   "outputs": [],
   "source": []
  },
  {
   "cell_type": "markdown",
   "id": "f32a9bbf",
   "metadata": {},
   "source": [
    "Note:"
   ]
  }
 ],
 "metadata": {
  "kernelspec": {
   "display_name": "Wolfram Language 13.2",
   "language": "Wolfram Language",
   "name": "wolframlanguage13.2"
  },
  "language_info": {
   "codemirror_mode": "mathematica",
   "file_extension": ".m",
   "mimetype": "application/vnd.wolfram.m",
   "name": "Wolfram Language",
   "pygments_lexer": "mathematica",
   "version": "12.0"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 5
}
