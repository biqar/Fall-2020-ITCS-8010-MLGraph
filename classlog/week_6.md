## Week 6
* User-User Evaluation Network: Many on-line settings where one person expresses an opinion about another (or about another’s content).
  * We are considering a case where `evaluator A` evaluate/vote `target B`
* Evaluation Network: Issues
  * What factors drive one’s evaluations?
    * How do properties of evaluator A and target B affect A’s vote?
      * Status: Level of recognition/reputation in the community (i.e. Stack Overflow: # answers)
        * B's reputation may make an impact on the probability that B receives a positive evaluation
      * Similarity: Overlapping topical interests of A and B (i.e. in Stack Overflow, similarity of users evaluated)
        * Relationship between the characteristics of A and B may impact on the probability that B receives a positive evaluation
  * How do we create a composite description that accurately reflects cumulative opinion of the community?

<table>
  <tr>
    <td>
       <img align="left" src="https://github.com/biqar/Fall-2020-ITCS-8010-TopicsInCS/blob/master/resource/w6-evaluation_on_status.png" alt="evaluation_on_status" title="Figure 1.1: # of Iterations 1"/>
    </td>
    <td><img align="left" src="https://github.com/biqar/Fall-2020-ITCS-8010-TopicsInCS/blob/master/resource/w6-evaluation_on_similarity.png" alt="mutex_vs_spin_compare_it_1000" title="Figure 1.2: # of Iterations 1,000"/>
    </td>
    <td><img align="left" src="https://github.com/biqar/Fall-2020-ITCS-8010-TopicsInCS/blob/master/resource/w6-evaluation_on_status_and_similarity.png" alt="evaluation_on_status_and_similarity" title="Figure 1.3: # of Iterations 1,000,000"/>
    </td>
    <td><img align="left" src="https://github.com/biqar/Fall-2020-ITCS-8010-TopicsInCS/blob/master/resource/w6-relation_status_and_similarity.png" alt="relation_status_and_similarity" title="Figure 1.3: # of Iterations 1,000,000"/>
    </td>
  </tr>
  <tr>
    <td>Observation:<br/>
     1. Probability of positive evaluation P(+) doesn’t depend on B’s status<br/>
    </td>
    <td>Observation:<br/>
     1. Prior interaction/similarity boosts positive evaluations<br/>
    </td>
    <td>Observation:<br/>
     1. Status is a proxy for quality when evaluator does not know the target<br/>
    </td>
    <td>Observation:<br/>
     1. Elite evaluators vote on targets in their area of expertise<br/>
    </td>
  </tr>
  <tr>
    <td align="middle">Figure I: Effect of status on evaluation</td>
    <td align="middle">Figure II: Effect of similarity on evaluation</td>
    <td align="middle">Figure III: Combined effect of status and similarity on evaluation</td>
    <td align="middle">Figure IV: Relationship between status and similarity</td>
  </tr>
  <tr>
    <td colspan="4" align="middle">Figure: How do properties of evaluator A and target B affect A’s vote?<br/>Evaluator A evaluate/vote Target B<br/>Delta = Status_of_A - Status_of_B</td>
  </tr>
</table>

* Evaluation Network: Setting
  * Direct: User to user
  * Indirect: User to user's content
* Evaluation Network: Dataset
  * Wikipedia adminship elections
  * Stack Overflow Q&A community
  * Epinions product reviews
* Ballot-blind: Prediction
  * Task: Predict Wikipedia adminship election results without seeing the votes
    * Observe identities of the first k (=5) people voting (but not how they voted)
* Ballot-blind: The Model
  * Task: Want to model the probability user A votes (+) in election of user B
  * Model: P(A = +|B) = P_A + d(S_A-S_B, sim(A, B))
    * P_A => empirical fraction of +votes of A
    * d(status,similarity) => avg. deviation in fraction of +votes
  * Based on only who showed to vote predict the outcome of the election

Number of voters seen | Accuracy | Other methods | Accuracy
--|--|--|--
5 | 71.4% | Guessing | 52%
10 | 75.0% | Logistic Regression on status and similarity features | 67%
All | 75.6% | If we see the first k=5 votes | 85% (gold standard)
