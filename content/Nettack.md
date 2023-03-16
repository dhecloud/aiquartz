[[Gray-box attack]] which aims to generate adversarial graphs for the node classifcation task. A single node is selected to be the target. The goal is to modify the structure or features of this nodes or its surrounding nodes to influence the prediction.
Two constraints are included:
1. degree distribution of the attacked graph should be close to the original
2. Distribution of the feature occurences should be close to the original


A surrogate model is first trained on the original clean graph data. Then, [[GCN-Filter]]s are used to create an attacking model, which is trained on attacking the surrogate model.