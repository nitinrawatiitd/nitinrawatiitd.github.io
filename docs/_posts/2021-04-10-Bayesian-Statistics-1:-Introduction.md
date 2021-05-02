---
layout: post
tags: bayesian-statistics
---

## 1. What is Bayesian Analysis?

At it's core, bayesian analysis is just this -

1. Count all the ways data can happen, according to assumptions   
2. Assumptions with more ways that are consistent with data are more plausible

A simple illustration of this process is the garden of forking data -

<img src="/assets/pics/bayesian-statistics/garden_of_forking_data.png" width="600" alt="garden of forking data" class="left">    
*Fig. 1. Garden of forking data.*   
{:.image-caption}

Suppose you are told that a given bag has 4 balls and that their colour can be either white or blue. And you take out a ball (with replacement) and observe it   
1. Your conjecture will tell you what possible permutations of white and blue balls you can have    
2. With each sampling you'll calculate the number of ways the sampling sequence can happen if a conjecture was true (counting). Scaling that to 1 gives you the probability that the underlying conjecture (plausibility)

<img src="/assets/pics/bayesian-statistics/garden_of_forking_data_updating.png" width="600" alt="garden of forking data updating" class="left">    
*Fig. 2. Updating Garden of forking data.*
{:.image-caption}

## 2. Building a bayesian model

Consider this example. You are given a light balloon globe that you can toss around to other people. Every time another person gets the globe, you see where the index finger on your right hand is. If it's on water, record that observation as W for Water, else record it as L for Land. Repeat the tosses multiple times.

<img src="/assets/pics/bayesian-statistics/globe_tosses.png" width="600" alt="globe tosses" class="left">   
*Fig. 3. Globe tosses.*
{:.image-caption}


2 Steps to building a bayesian model -
1. **Design** Data story motivates the model - how does the data WLWWWLWLW arise?   
   1. Some true proportion of water, p
   2. Toss globe, probability p of observing W, 1-p of L
   3. Each toss is independent of other tosses
2. **Condition** Bayesian updating defines optimal learning in the small world, converts prior to posterior 
   1. Give your model an initial information state - the prior   
   2. Condition on data to update information state - from prior to posterior   

If we follow the above steps for the globe tossing problem, this how it plays out -
<img src="/assets/pics/bayesian-statistics/Bayesian_model_steps.png" width="600" alt="Steps in bayesian update" class="left">  
*Fig. 4. Steps in bayesian update.*
{:.image-caption}

We start with a flat prior where we have equal probability assigned to each proportion of water p, from 0 to 1. So, it could be anything, equally. With each toss of globe i.e, sampling, we update the probability distribution of p. With each step, we narrow down the distribution to the momst probable value of p

Note:
* The data order is irrelevant, because the model assumes order irrelevant. All-at-once, one-at-a-time. shuffled order - all give the same posterior
* Every posterior is the prior for the next observation
* Sample size automatically embodied in the posterior

But how do these probability distributions shape change in each step. We'll come to that later

## Contruct the model

