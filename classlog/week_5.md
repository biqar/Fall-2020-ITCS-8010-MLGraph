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
