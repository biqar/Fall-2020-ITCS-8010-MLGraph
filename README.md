# Fall-2020-ITCS-8010-TopicsInCS
This repository contains the projects and assignments of course **"ITCS 8010: Machine Learning with Graphs and Large Networks"**. This course has been taken in Fall 2020 semester, as part of my PhD degree at UNC Charlotte.

## Week 1
* Discussed about the course structure
  * No single topic in the course is too hard by itself. But we will cover and touch upon many topics and this is what makes the course hard.
* Discussed about different commonly seen networks around us; and some of the applications
  * Polarization on Twitter
  * Information Diffusion
  * Information Cascades
  * Product Adoption
  * Misinformation
* Network Analysis Tools
  * NetworkX (we will mainly use this), JUNG, iGraph

## Week 2
* Discussed about the structure of the Web Graph
  * [Bow-tie Structure of the Web](https://kharshit.github.io/blog/2017/09/08/structure-of-the-web#myfootnote1)
  * Original Paper: [Broder et al.](https://kharshit.github.io/assets/graph_broder.pdf)
  * A revisit to the old thought: [Graph Structure in the Web — Revisited](http://www.quantware.ups-tlse.fr/FETNADINE/papers/P4.9.pdf)
```
We confirm the existence of a giant strongly connected component; we however find, as observed by other 
researchers [12, 5, 3], very different proportions of nodes that can reach or that can be reached from 
the giant component, suggesting that the “bow-tie structure” as described in [10] is strongly dependent 
on the crawling process, and to the best of our current knowledge is not a structural property of the web.

... the distributions of indegree, outdegree and sizes of strongly connected components are not power laws, 
contrarily to what was previously reported for much smaller crawls, although they might be heavy-tailed.
```
* Discussed about the basics of key network properties
  * Degree distribution: P(k)
    * Probability that a randomly chosen node has degree k
  * Path length: h
    * Network diameter: Longest shortest path in a graph
  * Clustering coefficient: C(i)
    * What portion of i's neighbors are connected
    * C(i) = (2 * e_i) / [k_i * (k_i - 1)]

## Week 3
Class went to asynchronous session this week. Task of this week is to watch the following YouTube video lectures by Prof. Mark Newman,

* [Mark Newman - The Connected World](https://www.youtube.com/watch?v=yAtsm5xkb5c)
  * Introduces different types of network. For example, technological network (internet), information network (www), biological network (food cycle), social network (who knows whom), etc.
  * Already covered in the week-1 class discussion.
* [Mark Newman - What Networks Can Tell us About the World](https://www.youtube.com/watch?v=lETt7IcDWLI)
  * Centrality: Which is the most important node in the network?
  * Milgram's `Small World` experiment
  * Closeness Centrality: Average distance to everyone else in the network.
    * Not a very good measure
      * Hard to calculate
      * Nearly same for everyone
  * Degree Centrality: Solves the problems of closeness centrality: easy to calculate; not same for everyone.
    * Not all people are equally important; but this can be solved by the idea of ...
  * Transitivity: 
  * Homophily: 
* [Mark Newman - Using Networks To Make Prediction](https://www.youtube.com/watch?v=rwA-y-XwjuU)

**todo:** Will add notes on this videos after finish watching it.

## Week 4
* Discussion on the last week's asynchronous materials.
* MSN Network: Key network properties
  * Degree distribution: Heavily skewed; Avg. degree = 14.4
  * Path length: 6.6
  * Clustering coefficient: 0.11
  * Observation: Constant degree; constant avg. Clustering coeff; Linear avg. path length
* Open Question: Is there any graph that have path length greater than N?
* Erdos-Renyi Random Graph: Key network properties
  * Degree distribution: Binomial distribution
  * Path length: O(n * logn)
  * Clustering coefficient: C = p = (mean of binomial distribution)/n
  * Observation: Very much different comparing with the real network (i.e. MSN Network)

## Week 5

## Week 6

## Week 7

## Week 8

## Week 9

## Week 10
