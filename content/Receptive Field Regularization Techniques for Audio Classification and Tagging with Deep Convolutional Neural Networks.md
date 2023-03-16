Author(s): [[Khaled Koutini]], [[Hamid Eghbal-zadeh]], [[Gerhard Widmer]]
Tags: #academic_papers
Read on: [[01-Jun-2021]]
URL: [\[2105.12395\] Receptive Field Regularization Techniques for Audio Classification and Tagging with Deep Convolutional Neural Networks (arxiv.org)](https://arxiv.org/abs/2105.12395)
# Main Contribution(s)
Problem: Deep [[Convolution Neural Network|CNN]] for [[Computer Vision]] often have a large [[Receptive Field]], not suitable for audio processing
Solution: provides generic and systematic methods for controlling the [[Receptive Field]] of a [[Convolution Neural Network|CNN]] architecture, which includes [[Filter Damping]] to improve generalization of the network
# Summary
Provides metric to measure [[Maximum Receptive Field]] of a [[Convolution Neural Network|CNN]], and the [[Effective Receptive Field]] of a trained [[Convolution Neural Network|CNN]].

![[Pasted image 20210601021154.png]]
Changes the 3x3 filter to 1x1 filters, based on the $p$ value. if layer $k>p$, then the filter will be 1x1.
![[Pasted image 20210601021604.png]] Results on [[TAU Urban Acoustic Scenes 2018]]. Out of the range of [[Maximum Receptive Field]] of 100-200, the performance degrades
![[Pasted image 20210601021833.png]]
Even though performance on training data drops slightly, it performs better on unseen data, alluding to better generalization capablities.

![[Filter Damping#Receptive Field Regularization Techniques for Audio Classification and Tagging with Deep Convolutional Neural Networks]]
[[Filter Damping]] is applied on both time and frequency dimensions, and on each separately. 

![[Pasted image 20210601022505.png]] ![[Pasted image 20210601023301.png]]Damping helps to restricts the [[Effective Receptive Field]], and helps to improve generalization on dcase18. no results shown for dcase19.
# Learning Gaps/Thoughts
Got some vibes of nitpicking test data. dcase18/19 data not shown consistently.
however very interesting paper
# Simplify/Analogies