---
layout: post
tags: bayesian-statistics
---

## Bayesian Data Analysis

At it's core, bayesian analysis is just this -

1) Count all the ways data can happen, according to assumptions   
2) Assumptions with more ways that are consistent with data are more plausible

A simple illustration of this process is the garden of forking data -

![garden of forking data]({{ '/assets/pics/bayesian-statistics/garden_of_forking_data.png' | relative_url }}){: style="width: 30%;" class="left"}
*Fig. 1. Garden of forking data.*
{:.image-caption}

Suppose you are told that a given bag has 4 balls and that their colour can be either white or blue. And you take out a ball (with replacement) and observe it
1) Your conjecture will tell you what possible permutations of white and blue balls you can have    
2) With each sampling you'll calculate the number of ways the sampling sequence can happen if a conjecture was true (counting). Scaling that to 1 gives you the probability that the underlying conjecture (plausibility)

![garden of forking data updating]({{ '/assets/pics/bayesian-statistics/garden_of_forking_data_updating.png' | relative_url }}){: style="width: 30%;" class="left"}
*Fig. 2. Updating Garden of forking data.*
{:.image-caption}
