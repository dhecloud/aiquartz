Author(s): [[Yi-Te Hsu]], [[Sarthak Garg]], [[Yi-Hsiu Liao]], [[Ilya Chatsviorkin]]

Tags: #academic_papers
Read on: [[December 3rd 2020]]
URL: https://arxiv.org/abs/2010.02416
# Main Contribution(s)
Proproses a deep encoder and shallow decoder architecture which can achieve up to 109% and 84% speedup on CPU and GPU respectively and reduce the number of parameters by 25% while maintaining the same translation quality in terms of [[BLEU]].
# Summary
![[Pasted image 20201203203747.png]]
Sequence level [[Knowledge Distillation]] is used to train the model. 

![[Pasted image 20201203205033.png]]
The [[self-attention]] is replaced with recurrent units like the [[Average Attention Network (AAN)]], the [[Simple Recurrent Unit (SRU)]], and the [[Simpler Simple Recurrent Unit (SSRU)]].

The [[Feed-forward]] can be removed entirely from the decoder without hurting the translation quality with our implementation of [[Simpler Simple Recurrent Unit (SSRU)]] 
![[Pasted image 20201203205101.png]]
Using 12 encoder layers and 1 decoder layer gives a signficant speedup without losing translation quality. 

![[Pasted image 20201203205117.png]]
Redundant attention heads are pruned by applying [[L0 regularization]]. However, it is non-differentiable. Hence it is modeled as a random variable sampled from a [[Hard Concrete Distribution]]


# Learning Gaps/Thoughts
They did not talk about [[Non-Autoregressive]] methods in their literature review.
# Simplify/Analogies
Maximize encoder and minimize decoder.