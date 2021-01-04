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
