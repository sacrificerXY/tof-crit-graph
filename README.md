A simple interactive graph showing the likelihood of getting different CRIT values after advancing gloves/boots 5 times.

*FUN FACT: The chance of getting the highest possible crit, without using data repeaters, is `1 in 174,576,393,478,176,768`.*

## Some Info
### Calculation assumptions
1. All possible crit stat rolls are equally likely (i.e. uniformly distributed)
2. The crit stat rolls are only in whole numbers, no decimals/fractions.

### How the data is calculated
I'm not a pro statistician/mathematician so I just basically turned it into a counting problem. I made a `python+numpy` program to count all of the possible ways a certain gear will roll. There are `1169 - 468 + 1 = 1002` possible values per roll. You also have to consider the chance of actually rolling into the crit substat (1 in 4 without using data repeaters).

All in all, it's just trying combining the 5 identical uniform discrete distributions and the 5 biased coin flips of rolling into crit. In theory, these are just a bunch of discrete convolution operations but the conditional coin flips makes it a bit harder to visualize/understand (at least for me). I might add the program later.

I tested my results with a basic gear rolling simulation and both of them gave practically the same distribution.
