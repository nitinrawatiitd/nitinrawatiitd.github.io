---
layout: post
tags: bayesian-statistics
---

## 1. What is Bayesian Analysis?

At it's core, bayesian analysis is just this -

1) Count all the ways data can happen, according to assumptions   
2) Assumptions with more ways that are consistent with data are more plausible

A simple illustration of this process is the garden of forking data -

![garden of forking data]({{ '/assets/pics/bayesian-statistics/garden_of_forking_data.png' | relative_url }}) 
{: style="width: 20%;" class="left"}   
*Fig. 1. Garden of forking data.*   
{:.image-caption}

Suppose you are told that a given bag has 4 balls and that their colour can be either white or blue. And you take out a ball (with replacement) and observe it   
1) Your conjecture will tell you what possible permutations of white and blue balls you can have    
2) With each sampling you'll calculate the number of ways the sampling sequence can happen if a conjecture was true (counting). Scaling that to 1 gives you the probability that the underlying conjecture (plausibility)

![garden of forking data updating]({{ '/assets/pics/bayesian-statistics/garden_of_forking_data_updating.png' | relative_url }})
{: style="width: 70%;" class="left"}
*Fig. 2. Updating Garden of forking data.*
{:.image-caption}

## 2. Building a bayesian model

Consider this example. You are given a light balloon globe that you can toss around to other people. Every time another person get the globe you see where the index finger on your right hand is. If it's on water mark that observation as W else mark it L for land. You repeat the tosses multiple times

![globe tosses]({{ '/assets/pics/bayesian-statistics/globe_tosses.png' | relative_url }})
{: style="width: 70%;" class="left"}
*Fig. 3. Globe tosses.*
{:.image-caption}


Steps to build a bayesian model -
1. **Design** the model (data story) - how does the data WLWWWLWLW arise?   
   1. Some true proportion of water p
   2. Toss globe, probability p of observing W, 1-p of L
   3. Translate data story into probability statements
2. **Condition** on the data (update) - prior to posterior, optimal learning in small world   
   1. Give your model an initial information state - the prior   
   2. Condition on data to update information state - from prior to posterior   
3. **Evaluate** the model (critique)   
   1. Did the model malfunction?
   2. Does the model answer make sense?
   3. Does the question make sense?
   4. Check the sensitivity of the answer to assumptions   
4. Repeat the above 3 steps

![Steps in bayesian update]({{ '/assets/pics/bayesian-statistics/Bayesian_model_steps.png' | relative_url }})
{: style="width: 70%;" class="left"}
*Fig. 4. Steps in bayesian update.*
{:.image-caption}
