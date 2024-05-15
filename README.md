# GNN Study Notes

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

The Cora dataset is a commonly used benchmark dataset in the field of machine learning and network analysis, particularly for tasks involving graph neural networks (GNNs). It is a citation network dataset that represents scientific publications and their citation relationships. Here are the key components and characteristics of the Cora dataset:

### Key Components

1. **Nodes**: Each node in the Cora dataset represents a scientific publication.

2. **Edges**: An edge between two nodes represents a citation, meaning that one publication has cited the other.

3. **Node Features**: Each node (publication) is described by a set of attributes. In the Cora dataset, these attributes are typically binary word vectors indicating the presence or absence of specific words in the publication's title or abstract. For example, a feature vector might have a dimension corresponding to each word in a predefined vocabulary, with a value of 1 if the word is present in the document and 0 otherwise.

4. **Node Labels**: Each node is assigned a label representing the topic of the publication. The Cora dataset has seven classes, each corresponding to a different topic:
    - Case-Based
    - Genetic Algorithms
    - Neural Networks
    - Probabilistic Methods
    - Reinforcement Learning
    - Rule Learning
    - Theory

### Dataset Statistics
- **Number of Nodes (Publications)**: 2,708
- **Number of Edges (Citations)**: 5,429
- **Number of Features**: 1,433 unique words in the dictionary used for feature vectors
- **Number of Classes**: 7

### Data Format
The dataset is usually provided in a specific format, with separate files or structures for the node features, edge list, and labels. Here’s a typical structure:

- **Content File**: This file contains the node features and labels. Each line corresponds to a publication and includes the node ID, binary word vector, and the publication's class label.
- **Cites File**: This file lists the citation relationships. Each line represents a directed edge (citation) from one publication to another, indicating a citation relationship.

### Example Use Cases
- **Node Classification**: Predict the topic of a publication based on its word vector and the structure of the citation network.
- **Link Prediction**: Predict whether a citation link exists or should exist between two publications.
- **Graph Clustering**: Group publications into clusters based on their citation relationships and content similarity.

### Importance in Research
The Cora dataset is widely used in research for testing and benchmarking graph-based machine learning algorithms, including GNNs. Its structured yet relatively simple nature makes it an ideal starting point for developing and evaluating new algorithms in areas like node classification, link prediction, and graph representation learning.

### Example Analysis Workflow
1. **Preprocessing**: Prepare the dataset by loading the node features, edge list, and labels. Normalize the feature vectors if necessary.
2. **Model Selection**: Choose a suitable GNN model, such as Graph Convolutional Networks (GCNs), Graph Attention Networks (GATs), or others.
3. **Training**: Split the data into training, validation, and test sets. Train the model on the training set while tuning hyperparameters using the validation set.
4. **Evaluation**: Evaluate the model’s performance on the test set using appropriate metrics, such as accuracy for node classification tasks.

By providing a rich yet manageable dataset, Cora serves as a valuable resource for developing and testing graph-based machine learning methods.

