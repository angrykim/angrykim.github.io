---
layout: post
title:  "Basic graph analytics (5)"
categories: [Network graph analysis]
---

## K-means clustering for figuring out a shape of community 

When analyzing a graph, It is required to divide the network into community units as i explained in the previous post [here](https://angrykim.github.io/network%20graph%20analysis/2018/07/06/Basic-graph-analytics-(4).html)

When figuring out a marketing fruad case in a specific period, 

One of my favorite ways to analyze network graphs is to conduct analysis on a community basis.

For instance, we normally analyze the data by user ID or log event. 

As for community based analysis, It is based on community classes, not the user IDs or event IDs.

As you can see the following graph, It is an example network graph for a week data set. 

<center><img src="/static/img/community_basis_network_1.png" width="85%"></center>

The left picture is the network graph and the right is the same one with Modularity applied. 


   - `The number of communities: 1,499` 

   - `Modularity: 0.991`


Once we compute the modularity, What's the next step is to check the ratio of the events that the node has, with the following information, you should check whether it is a fraud or not.

#### - Checkpoint

1. Determine what kinds of event(pay, deposit, transfer, and etc) history we can find in the community like

   - `Transfer ratio` 
   
        - The percentage of how many transfer events occurred in the community over the same period.
  
  
   - `Withdraw ratio` 
   
        - The percentage of how many withdraw events occurred in the community over the same period.
  
  
   - `Deposit ratio` 
   
        - The percentage of how many deposit events occurred in the community over the same period.
   
   
   - `Payment ratio` 
   
        - The percentage of how many payment events occurred in the community over the same period.
   
   
   - `User Grade` 
   
        - According to period of use, we can classify users into groups like "Light", "Midieum", and "Heavy". 
   
   
2. Whether or not the nodes has same event sequence


If you have those information, I'm sure that you will be able to detect not only the community that 

carried out **"marketing fraud"**, but also set rules to enable automatic detection.**




