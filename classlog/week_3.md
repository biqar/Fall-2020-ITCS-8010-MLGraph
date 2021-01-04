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
