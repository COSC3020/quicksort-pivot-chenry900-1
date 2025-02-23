# Quicksort Pivots

in the lectures I only briefly mentioned strategies for determining a good pivot
for quicksort. The implementation on the slides simply picks the leftmost
element in the part of the array that we consider as a pivot. I also mentioned a
few other ways of picking a good pivot, e.g. randomly.

Median-of-three is also a good way of picking a pivot -- inspect the first,
middle, and last elements of the part of the array under consideration and
choose the median value. Using the probabilities for picking a pivot in a
particular part of the array (in the same way as we did on slide 34), argue
whether this method is more or less (or equally) likely to pick a good pivot
compared to simply choosing the first element. Assume that all permutations are
equally likely, i.e. the input array is ordered randomly.

Your answer must derive probabilities for choosing a good pivot and
quantitatively reason with them.
If you take the median of three pivots you end up with 4 posibilities for those pivot choices either all good, all bad or some combination between those. we can break that down into a probability of that happening at a (1/8)+(3/8)+(3/8)+(1/8). (good, good, good) (good, good, bad) (good, bad, bad) (bad, bad, bad) if you have 2 bad numbers than the chance that they fall on opposite sides of the good number is 50%. so the probablity of getting a good pivot from each is 100%, 100%, 50%, 0%. If you multiply that together than you get (1/8 *1)+ (3/8 *1) + (3/8 *.5) + (1/8 *0) = (11/16) or 68.75% chance that a median of three numbers will get a good pivot. While the chance that you get a good pivot for a single number is about 50%.

Add your answer to this markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.
