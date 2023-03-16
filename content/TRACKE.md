### [[A Transformer-based Audio Captioning Model with Keyword Estimation]]

![[Pasted image 20210209175637.png]]
The bottleneck feature of [[VGGish]] is used for audio embedding, and [[FastText]] for caption-word and keyword embedding.

The Keyword estimation branch aims to predict keyword labels by estimating the posterior, and aggregating these posteriors. Then the most likely K keywords are selected. There is no backpropagation here as top k selection and sorting is not differentiable

The ground truth keyword labels are extracted from the ground truth target sequences, and converted to their lemmas. 

Two cost functions are minimized simultaneously: the basic [[cross entropy]] loss for captions, and a weighted [[cross entropy]] loss for keyword estimation. 