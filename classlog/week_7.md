## Week 7
* Signed Network: Network with positive and negative relationship.
* Graph is **balanced** if every connected triple of nodes has:
  * All 3 edges labeled +
  * or, Exactly 1 edge labeled +
* If all triangles are balanced, then either:
  * The network contains only positive edges, or
  * Nodes can be split into 2 sets where negative edges only point between the sets
* We can find two different views in the signed network:
  * Local view: Fill in the missing edges to achieve balance
  * Global view: Divide the graph into two coalitions
* Graph is balanced if and only if it contains no cycle with an odd number of negative edges
  * How to compute this?
    * Find connected components on + edges
      * If we find a component of nodes on + edges that contains a – edge => the graph is unbalanced
    * For each component create a super-node
      * Connect components A and B if there is a negative edge between the members
    * Using BFS assign each super-node a side (i.e. left and right)
      * Graph is unbalanced if any two connected super-nodes are assigned the same side
