# Knowledge acquisition from Hotel reviews

Date: **28.05. (Due: 27.05.)**

Name: **Balaji Subramani**

Session: **[Knowledge Graph](https://textvis.repke.eu/index.html)**

Code: on **[GitLab](https://gitlab.hpi.de/fg-naumann/teaching/tvip19/tree/master/assignments/07_knowledgegraphs/basu)**

## Objective

This blog is focused to visualize the Knowledge Graph features. Here also, we experimented knowledge graph functionality with Trip adviser dataset.

## Data Filter

Due to the huge size of the volume, we have restricted and filtered low rated (<2) & high rated (4.8) reviews, for knowledge graph. Even from available data, we have only extracted review title instead of review content. So that we are able to gain the main intuition of review with minimal data.

## Knowledge Graph Data Set

We have split topics to cleansed tokens. Then created a combination of words with triplets. After that, finding the nouns and verb for each word in triplets. Finally forming the triplets which are having 2 nouns and one verb. Finally, stemmed the noun and the verb. Unfortunately, stemming is not did a good job. So some words are not converted properly. But sill understandable.

#### Node :

From the overall reviews topics, we are extracting all the nouns for nodes. The nodes data set is having below attributes

- ID - word

- Label - word

#### Edges :

Edges are designed based on triplets. Edge source & target nodes are select from noun and edges are considering here as a verb.

- Source - Noun 

- Target -  Noun

- Edge - Verb

All edges are considered as an indirect edge in our analysis.

# Knowledge Graph

We have used the gephi tool for knowledge graph visualization. Node and Edge data sets are given as the input for text visualization.

![Initial](uploads/b6e423729f7608bae395bd5a8315dfa2/Initial.png)

The above image shows the whole knowledge set in a graph. Here Blue nodes are acting the as a Domain and edges are acting as the relationship between nodes.

There is a lot of interconnection of nodes in the center of the graph. So we will apply the k-core filter for a better view.

![k_core_2](uploads/94745251ad03f30b849392fad393ec26/k_core_2.png)

Still, the center part is convoluted. But we will focus that part in a different graph. now focus on the outside of the graph. Here Top left, we could see a lot of relationship with **exceed** word. Also, **amaze** word is connected with *Family*, *First*, *still* and *food*.

Now move into the inner core of the graph (k=3). Also here, we applied Between centrality with node size. Here the **Best** word is acting as a major node. It also has a strong relationship with *amaze*.

![k_core_3_Between](uploads/ac62d879bb8258e2fd9c0f7748b770cc/k_core_3_Between.png)

Also, the funny part here is place and review is related to ignoring. Also, **great** is related with **busy**.

### Conclusion

 In our above analysis, we could not get much inference as we don't have proper relationship words. Still, we find the major connection and information with available data.
