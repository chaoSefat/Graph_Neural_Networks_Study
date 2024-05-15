# Graph_Neural_Networks_Study

Graph Neural Networks (GNNs) are designed to work with data structured as graphs. Graphs are mathematical structures used to model pairwise relations between objects. The data used in GNNs typically includes:

1. **Node Features**: These are attributes or characteristics of the nodes (vertices) in the graph. For example, in a social network graph, node features might include user attributes such as age, gender, interests, etc. In a molecular graph, node features could be types of atoms, their charge, etc.

2. **Edge Features**: These are attributes or characteristics of the edges (connections) between nodes. In a social network, edge features might include the type of relationship (e.g., friends, colleagues) or the strength of the connection. In a molecular graph, edge features could represent the type of chemical bond between atoms.

3. **Graph Structure**: This is the adjacency information that defines how nodes are connected by edges. It can be represented by an adjacency matrix or an edge list. The adjacency matrix is a square matrix used to represent a finite graph, with elements indicating whether pairs of vertices are adjacent or not.

4. **Global Graph Attributes**: Sometimes, there are attributes that describe the graph as a whole, rather than individual nodes or edges. For example, in a transportation network, a global attribute might be the total number of routes.

Here is a more detailed explanation of these components:

### Node Features
- **Attributes**: Quantitative or categorical data associated with each node. For example, in a citation network, node features could include the publication date, authors, and topic of each paper.
- **Embeddings**: Learned representations that map nodes into continuous vector spaces, often used in natural language processing tasks.

### Edge Features
- **Weights**: Numerical values representing the strength or capacity of the connection between nodes. In a weighted graph, each edge has a weight, such as the distance between two locations in a road network.
- **Types**: Categorical labels indicating different kinds of relationships. For example, in a knowledge graph, edges might be labeled with different types of relations like "is a," "part of," etc.

### Graph Structure
- **Adjacency Matrix**: A \(N \times N\) matrix (where \(N\) is the number of nodes) with binary or weighted entries indicating the presence or weight of edges between pairs of nodes.
- **Edge List**: A list of pairs (or triplets if edges have weights) indicating which nodes are connected.

### Global Graph Attributes
- **Graph-level Labels**: For tasks like graph classification, where the entire graph needs to be classified into different categories, global labels are used.
- **Graph Features**: Summary statistics or attributes that describe the graph, such as the number of nodes, number of edges, average degree, etc.

### Example Applications
1. **Social Networks**: Nodes represent individuals, and edges represent friendships or interactions. Node features could include demographic information, and edge features might include interaction frequency.
2. **Molecular Graphs**: Nodes represent atoms, and edges represent chemical bonds. Node features could include atomic number and charge, while edge features could represent bond type and length.
3. **Citation Networks**: Nodes represent academic papers, and edges represent citations. Node features could include publication year and author information.
4. **Recommendation Systems**: Nodes represent users and items, and edges represent interactions like ratings or purchases. Node features might include user demographics and item descriptions, while edge features could include ratings.

GNNs leverage this structured data to perform various tasks such as node classification, link prediction, and graph classification, using the connectivity patterns and node/edge features to inform their predictions.

