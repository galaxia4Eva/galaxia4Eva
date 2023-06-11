# Lecture notes
## 1.1 Motivation of Graph ML

---

#link: https://youtu.be/JAB_plj2rbA

---

- Natural graphs
- Graphs as a representation

Arbitrary size and topology. There's no notion of spatial locality and node ordering. How to organise processing without feature engineering? Graph ML does representational learning: f: u -> R^d

- Traditional methods: Graphlets, Graph kernels;
- Methods for node  embeddings: DeepWalk, node2vec;
-  Graph Neural Networks: GCN, GraphSAGE, GAT, Theorz of GNNs
- Knowledge and graph reasoning: TransE. BetaE;
- Deep generative models for graphs;
- Applications to Biomedicine, Science , Industry.

## 1.2 Applications of Graph ML

---

#link: https://youtu.be/aBHC6xzx9YI

---

Different levels of tasks:
- node level: node classification;
- edge level: link prediction;
- community (subgraph) level: clustering
- entire graph level: graph classification, graph generation, graph evolution.

High impact applications:
- node level: protein folding to predict 3D structure of protein given a sequence of amino acids;
    - > AlphaFold by DeepMind. Spatial graph represents a protein
- edge level:
    - recommender systems;
    - drug combination side effects;
- subgraph level:
    - traffic prediction;
- graph level:
    - drug discovery;
    - novel molecules generation with given properties
    - improve properties of molecules
    - simulation of physical systems

## 1.3 Choice of Graph Representation

---

#link: https://youtu.be/P-m1Qv6-8cI

---

- objects: nodes, vertices
- interactions: links, edges
- system: network, graph

Design choices:
- Directed/Undirected;
- Node degrees, average node degree, in-degree, out-degree for directed graphs;
- Bipartite graphs;
- Folded networks: project graph onto bipartite network, project bipartite graph onto network;
- Multipartite graphs.

Representations:
- adjacency matrix — sparse;
- edge list;
- adjacency list — list of neighbours of a node;
- attributes of nodes, edges:
    - weights of edges can be represented in adjacency matrix;
    - self loops on diagonal of adjacency matrix.
- multi-graphs have multiple edges between a pair of nodes;
- connectedness:
    - weak connectivity;
    - strong connectivity:
        - strongly connected components
