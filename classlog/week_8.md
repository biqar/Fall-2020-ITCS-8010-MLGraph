## Week 8
* Real-world dataset of large signed networks
  * Epinions: Trust/Distrust
  * Wikipedia: Support/Oppose
  * Slashdot: Friend/Foe
* In general, it is hard for any real-world signed graph to be balanced!
  * An alternate way to confirm whether a graph structurally hold the balance:
    * Compare frequencies of signed triads in real and “shuffled” signs
* Embeddedness of link (A,B): Number of shared neighbors
* Status in a network
  * A (+)⟶ B :: B has higher status than A
  * A (-)⟶ B :: B has lower status than A
* Transitively in status
  * Can replace `A (-)⟶ B` with `A (+)⟵ B`
* Status Vs. Balance
  * Status ⇒ Hierarchy
    * All-positive directed network should be approximately acyclic
  * Balance ⇒ Coalitions
    * Balance ignores directions and implies that subgraph of negative edges should be approximately bipartite
* todo: will add the rest of the class note later ... (i.e. how sign of an edge can be predicted w.r.t. context; surprise; etc.)
