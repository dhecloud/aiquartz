Author(s): [[Yongjing Yin]], [[Fandong Meng]], [[Jinsong Su]], [[Chulun Zhou]], [[Zhengyuan Yang]], [[Jie Zhou]], [[Jiebo Luo]]
Tags: #academic_papers, #Neural_Machine_Translation, #Graph_Neural_Networks,
Read on: [[December 23rd 2020]]
URL: https://arxiv.org/abs/2007.08742
# Main Contribution(s)
Presents a way to use graphs as an input to support [[Neural Machine Translation]].
# Summary
Intuition is that visual context helps to resolve ambiguous multi-sense words. This is done by introducing a multi-modal fusion encoder.

### Graph-based Multi-modal Fusion Encoder
![[Pasted image 20201223145536.png]]The input is represented as a unified multi-modal graph. Nodes with the same modality as connected with an intra-modal edge (all text are connected to each other, all images are connected to each other). Each textual node is connected to its corresponding visual node with an inter-modal edge.
![[Pasted image 20201223145705.png]] The graph is sent to the embedding layer to initialize the node states. Each node is initialized as the sum of its word embedding and position encoding.
[[Multi-Head Self-Attention]] is used for the intra-modal fusion. For the inter-modal fusion, a cross-modal gating mechanism is used to gather the semantic information.  The decoder is same of that from the [[Transformer]].

### Experiments
![[Pasted image 20201223150210.png]] Results on the [[Multi30k]], [[WMT17 En-De]], [[MSCOCO]] datasets.
The Stanford parser is used to identify noun phrases, then a visual ground toolkit is used to detect visual objects
# Learning Gaps/Thoughts
Not very sure what is the legitmacy of this. Seems like external parses/object detection is done, which would obviously help the performance
# Simplify/Analogies