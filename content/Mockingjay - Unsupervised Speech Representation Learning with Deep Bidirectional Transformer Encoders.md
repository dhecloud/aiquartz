Author(s): [[Andy T. Liu]], [[Shu-wen Yang]], [[Po-Han Chi]], [[Po-chun Hsu]], [[Hung-yi Lee]]
Tags: #academic_papers
Read on: [[May 11th 2021]]
URL:
# Main Contribution(s)
Problem: Previous speech representation condition on past frames and predict information about future frames
Solution: [[Mockingjay]] is designed to predict current frame through jointly conditioning on both past and future contexts.
# Summary
![[Pasted image 20210511140939.png]]
Inspired by [[Masked Language Modelling]], the authors proposed [[Masked Acoustic Modelling]], where 15% of input frames are masked and the model has to predict the masked frames. [[Manhattan Distance|L1 norm]] is used to minimize the reconstruction error
# Learning Gaps/Thoughts
# Simplify/Analogies