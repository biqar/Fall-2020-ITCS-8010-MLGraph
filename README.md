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

1. **[Mark Newman - The Connected World](https://www.youtube.com/watch?v=yAtsm5xkb5c)**
  * Introduces different types of network. For example, technological network (internet), information network (www), biological network (food cycle), social network (who knows whom), etc.
  * Already covered in the week-1 class discussion.
2. **[Mark Newman - What Networks Can Tell us About the World](https://www.youtube.com/watch?v=lETt7IcDWLI)**
  * Discussed about the static parts of the graph
  * Milgram's `Small World` experiment
  * **Centrality:** Which is the most important node in the network?
    * **Closeness Centrality:** Average distance to everyone else in the network.
      * Not a very good measure
        * Hard to calculate
        * Nearly same for everyone
    * **Degree Centrality:** Solves the problems of closeness centrality: easy to calculate; not same for everyone.
      * Not all people are equally important; but this can be solved by the idea of ...
  * **Transitivity:** Friend of my friend is also my friend.
    * What if friends of mine are not friends to each other?
    * This means I am more central - I have more influence to the network.
    * Example case: Friend suggestion based on the common friend in socual network.
  * **Homophily:** Based on node attributes, similar nodes may be more likely to attach to each other than dissimilar ones.
    * We can use homophily to make prediction
  * **Modularity:** Groups or communities within networks, and predicting how networks will split up.
    * Tells how much homophily we have in our network
    * The modularity score helps identifying the community in a network
3. **[Mark Newman - Using Networks To Make Prediction](https://www.youtube.com/watch?v=rwA-y-XwjuU)**
  * Discussed about the dynamic parts of the graph
  * Power-Law is everywhere
    * Very few family name are very common
    * Most cities are small; a very few cities are very big
  * The 80-20 rule: this comes from the power law distribution
    * wealthy 20% of people own 86% of the wealth
  * Where do the power laws come from?
    * Preferential attachment: rich get richer!!!
      * Can be examplified by the citation network
      * Paper cite other papers in proportion to the number of citation those others already have
      * If any paper have a early lead (published in the earlier time of the field); it will get more citation (because there is very few papers exist then). It ultimately helps getting more citation of those papers.
  * **Disease spreading network**
    * Disease spread from one node to another of the network.
    * So which is the most influential node in this network?
      * The node that have more degrees.
      * But, what's the factor it influences the network?
        * `Degree`? NO!!!
        * It's `Degree ^ 2`!
        * One simple explanation could be: that node is likely to spread the disease to `d` nodes and it have `d` more likely to be caught by the disease. Here `d` represents the degree of the node.
    * This analysis can be used to select the priority of vaccination
      * Influential nodes (hub) should be vaccinated first!
      * If we can select those nodes effectively, we can very effective in controlling the spread of the disease
    * But how can we build this network?
      * As the network does not exist, why not use the network to build the network!
      * Call a random person and instead of giving the vaccine to him/her; ask a name of his/her friend and vaccinate that friend!
      * This comes from the idea that: if a friend have 1000 friends then it have 1000 times more chance to be nominated!!!
  * **Future direction:**
    * Get better in measuring network
    * Understand how network change over time
    * Understand how changing a network can change its performance and perhaps improve it
    * Get better in predicting network phenomena
    * Predict how society will react or evolve based on social networks
    * Prevent disease before it happen
    * And many more ...

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
* Graph structure of G_np as p changes

![Image of G_np graph structure change while changing p](https://github.com/biqar/Fall-2020-ITCS-8010-TopicsInCS/blob/master/resource/w5-g_np-change.png)
* Six degrees of Kevin Bacon

![Image of publication distance between raqib and erdos](https://github.com/biqar/Fall-2020-ITCS-8010-TopicsInCS/blob/master/resource/w5-erdos-raqib-pub-distance.png)
* Small-world experiment
  * Milgram ’67 (letter experiment): Avg. chain length = 6
  * Columbia small-world study (email experiment): Avg. chain length = 4
* Should we be surprised by the concept of 6-degrees? If every person knows 100 other persons then,
  * Step 1: reach 100 people
  * Step 2: reach 100 x 100 = 10,000 people
  * Step 3: reach 100 x 100 x 100 = 1,000,000 people
  * Step 4: reach 100 x 100 x 100 x 100 = 100M people
  * In 5 steps we can reach 10 billion people; so why we should be surprised by the concept of 6-degrees?
  * This is because, in reality this would not form a tree. Meaning, there should be common between two person's known people list.
* The `diameter/clustering coefficient` "Controversy"

![The diameter/clustering coefficient Controversy](https://github.com/biqar/Fall-2020-ITCS-8010-TopicsInCS/blob/master/resource/w5-diameter_clustering-coefficient-controversy.png)
  * Low diameter => Low clustering coefficient
  * High clustering coefficient => High diameter
  * The question here is: Could a network with high clustering be at the same time a small world?
  * Probable solution

![The diameter/clustering coefficient Controversy solution](https://github.com/biqar/Fall-2020-ITCS-8010-TopicsInCS/blob/master/resource/w5-diameter_clustering-coefficient-controversy_solution.png)
* Centrality
  * Betweenness Centrality: How many pairs of individuals would have to go through you in order to reach one another within shortest distance?
  * Closeness Centrality: Reciprocal of the mean average shortest path length from node `x` to all other nodes in the graph `y`.
  * Farness centrality: Avg. shortest path length from node `x` to all other nodes.
  * **todo:** Need to make more careful understanding on the impact of Betweenness Vs. Closeness centrality
* 

## Week 6

## Week 7

## Week 8

## Week 9

## Week 10
