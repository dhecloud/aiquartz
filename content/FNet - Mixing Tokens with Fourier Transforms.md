Author(s): [[James Lee-Thorp]], [[Joshua Ainslie]], [[Ilya Eckstein]], [[Santiago Ontanon]]
Tags: #academic_papers, #transformer 
Read on: [[01-Jun-2021]]
URL: [\[2105.03824\] FNet: Mixing Tokens with Fourier Transforms (arxiv.org)](https://arxiv.org/abs/2105.03824)
# Main Contribution(s)
Problem: Although the [[self-attention]] mechanism is found to be potentially limited to the effectiveness, the general finding it that it does flexibly capture diverse and syntactic semantic relationships
Solution: Investigate if simpler mixing mechanisms can replace complicated attention layers
# Summary
![[Pasted image 20210601014642.png]] Replaces the [[self-attention]] layer in the [[transformer]] encoder with a [[Fourier Transform]]. This architecture is called the [[FNet]].
Only the real part of the [[Fourier Transform]] is extracted, and the imaginery part is ignored. 
![[Pasted image 20210601014736.png]]
7x faster training and inference, while retaining 92% of performance.

Showed that simple, linear token “mixing” transformations, along with the nonlinearities in feed-forward layers, are sufficient to model diverse semantic relationships in text.

# Learning Gaps/Thoughts
Interesting research
# Simplify/Analogies