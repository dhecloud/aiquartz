Author(s): [[Yuma Koizumi]], [[Ryo Masumura]], [[Kyosuke Nishida]], [[Masahiro Yasuda]], [[Shoichiro Saito]]
Tags: #academic_papers, #Automated_Audio_Captioning 
Read on: [[February 9th 2021]]
URL: https://arxiv.org/abs/2007.00222
# Main Contribution(s)
Proposes [[TRACKE]], a [[Transformer]] based audio captioning model with keyword estimation
# Summary
One of the problems in [[Automated Audio Captioning|AAC]] is the existence of many possible captions that corresponds to an input. Authors decompose [[Automated Audio Captioning|AAC]] into two subtasks:
1. Caption Generation
2. Keyword Estimation.

![[TRACKE#A Transformer-based Audio Captioning Model with Keyword Estimation]]

![[Pasted image 20210209180840.png]]
[[BLEU]] on [[Clotho dataset]].

### Analysis
[[TRACKE]] achieved highest score without given keywords. With given keywords from the oracle, it is even higher.
Keyword estimation performance only 48.1%.
# Learning Gaps/Thoughts
There is no backpropagation from decoding to keyword estimation due to non-differentiable operations.
If the transformer decoder performed better with ground truth keyword provided, it simply attests to the training proficiency of the transformer decoder and not the usefulness of the keyword estimation?
# Simplify/Analogies
Uses a keyword estimation, sort of a [[Scaffolding]] technique to improve generation.