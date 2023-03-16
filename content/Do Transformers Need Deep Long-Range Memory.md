Author(s): [[Jack W. Rae]], [[Ali Razavi]]
Tags: #transformer, #language_model, #academic_papers
Read on: [[July 31st, 2020]]
URL: http://arxiv.org/abs/2007.03356
# Main Contribution(s)
- Show that long range memory is not needed at every layer of the [[Transformer-XL]], only in later layers
- Show that layer position of long range memory matters 
# Summary
    Replace long range memory of $$d = 1024$$ with short-range memory $$d = 128$$
- The number of model parameters is independent of the memory size, so number of parameters remains the same
    ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FnHDewLPzYT.png?alt=media&token=b8828cd7-8256-439d-96a8-7be1fcc92e72)There are three ways the LRMs are changed:
- 1. Interleaved with equal spacing
- 2. First layer of the network
- 3. Latter layer(s)
    ## Results
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FaE0jn2xfP-.png?alt=media&token=c91f9e22-a595-482a-beec-6ae61b3bbbdb)
- Model with 12 long range memory at the lower layers of the network is worse than a model with a single long range memory
- Position of long range memory matters
- Better not to place long range memory in shallow layers 
# Learning Gaps
- Need a refresher on [[Transformer-XL]]
# Simplify/Analogies
- Long range memory is not needed in earlier layers, but is required in the later stages
