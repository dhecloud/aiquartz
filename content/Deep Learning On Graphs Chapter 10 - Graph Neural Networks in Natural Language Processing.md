[[Graph Neural Networks|GNN]] has been used to enchane many NLP tasks such as [[Semantic Role Labeling]], [[Question Answering]], [[Relation Extraction]], [[Neural Machine Translation]], [[Graph to Sequence]]

### [[Semantic Role Labeling]]
In (Marcheggiani and Titov, 2017), [[BiLSTM]] used as the encoder to learn context-aware word representation. The output of the encoder is used as input to the [[Graph Neural Networks|GNN]] model. Then the output of the GNN is used as the input for the linear classifier [[Feed-forward]] layer.

### [[Neural Machine Translation]]
In (Marcheggiani et al., 2018), the decoder is kept the same; an attention based model. For the encoder, the [[BiLSTM]] model is used to encode the sequence. After which, the encoder output is fed to a [[Graph Neural Networks|GNN]] which is then fed to the decoder.

### [[Relation Extraction]]
In  (Zhang et al., 2018c), it is treated as a classification problem. The input is the concatenation of the representations of the sentence, the subject entity and the object entity. The output labels are the relations. A self-loop is introduced to include the word itself during representation update. They find that including direction and edge label information does not help.
![[Pasted image 20201212190435.png]]

### [[Question Answering]]
[[WIKIHOP dataset]]
[[Entity-GCN]] is propsed to learn node representations.

### [[Graph to Sequence]] learning
Mostly encoder-decoder models. [[GraphSAGE-Filter]] is used to aggegrate and update the nodes. There are two representations for each node, the in-representation and the out-representation.

### [[Graph Filter]]s for [[Knowledge Graphs]]
[[GGNN-Filter]] is adapted to knowledge graphs.
[[Knowledge Graphs]] are transformed to [[Simple Graph]]s using a scoring function to measure the influence of an entity to another entity through a specific type of relation.