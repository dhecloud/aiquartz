Author(s): [[Leonardo F.R. Ribeiro]], [[Martin Schmitt]], [[Hinrich Schütze]], [[Iryna Gurevych]]
Tags: #academic_papers, #Graph_Neural_Networks, #transformer, #Graph_to_Text
Read on: [[January 6th 2021]]
URL: https://arxiv.org/abs/2007.08426
Code: https://github.com/UKPLab/plms-graph2text
# Main Contribution(s)
Uses large pretrained language models along with graph to achieve state of the art results.
# Summary
Uses [[BART]] and [[Text-To-Text Transfer Transformer|T5]]. Similar to [[Text-To-Text Transfer Transformer|T5]], the prefix 'translate from Graph to Text' is used before the graph input to indicate the task. ![[Pasted image 20210106233743.png]] It seems like the input to the models are a textual representation of the graphs and not an [[Adjacency Matrix]] or [[Laplacian Matrix]].

![[Pasted image 20210106233344.png]]Results on [[AMR17]], [[WebNLG]], [[AGENDA]].

These results seem to be supported by research that says that [[language model]]s are knowledge bases.
# Learning Gaps/Thoughts
The textual representation of graphs was quite new to me, thought graph inputs would usually be [[Adjacency Matrix]]s.

# Simplify/Analogies
-