Author(s): [[Alexei Baevski]], [[Steffen Schneider]], [[Michael Auli]]
Tags: #academic_papers, #self_supervised_learning, #speech_representations
Read on: [[April 30th 2021]]
URL: https://arxiv.org/abs/1910.05453
# Main Contribution(s)
Problem: Well performing NLP algorithms cannot be applied to speech data because of the continuous nature of speech data
Solution: Discretize speech representations using 
# Summary
![[Pasted image 20210501152249.png]] 
### 1st way: [[Gumbel-Softmax]]
Input vector is passed to a linear layer which quantizes the vector, then passed to the [[Gumbel-Softmax]], which allows selecting discrete codebook in a fully differentiable way. 

### 2nd way: [[K-means clustering]]
Quantizes the vector by finding the closest variable to the input features $z$ in terms of the Euclidean distance.  

### 3rd way: Vector Quantization with multiple variable groups
Prone to mode collapse as some codewords are reused or only a few codewords are used. This is mitigated by independently quantizing partitions of z similar to [[Product Quantization]]. The feature vector organized into multiple groups, then the 1st or 2nd way is applied on each group.

### [[BERT]] pretraining
The discrete inputs are then passed to BERT which is then pretrained as usual. Spans of consecutive tokens are masked instead of single tokens.

### Experimental results
![[Pasted image 20210501154706.png]] Results on [[LibriSpeech]] in terms of [[Letter Error Rate]] and [[Word Error Rate (WER)]]

# Learning Gaps/Thoughts
# Simplify/Analogies