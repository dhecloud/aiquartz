Author(s): [[Shucong Zhang]], [[Erfan Loweimi]], [[Peter Bell]], [[Steve Renals]]
Tags: #critique, #speech_recognition, #transformer, #academic_papers
Read on: [[May 29th, 2020]]
URL: https://arxiv.org/abs/2005.13895
# Main Contribution(s)
- Show that in speech recognition, changing the upper self attention layers to feed forward layers leads to no performance drop
# ELI5
- Self attention layers typically focus on many single parts of a sequence, but we do not need to zoom in onto the sequence at every single layer.
# Summary
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FTfm6PQSEdt.png?alt=media&token=c644fae4-99ee-46c5-9b75-efdebdcdc201)
- Acoustic events are assumed to often happen within a small time span from left to right.
- If lower layers have encoded a sufficiently large span of context, then it is unnecessary for upper layers to continue to encode more information about the acoustic events (monotonically decreasing efficiency?)
- If that happens, using feedforward layers instead of self attention layers should not impact the performance
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2F8mJcMsjmAE.png?alt=media&token=fb70d0f7-f35d-4d06-a367-97aed5d42660)
- Results on the [[WSJ]] dataset
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2F5i7iNHLad2.png?alt=media&token=b16c1fe9-ef78-418c-9f17-3de8e4ee1063)
- Results on the [[eval 2000 SWBD]] dataset
- Performance remains comparable and stable when changing the first 4 layers, then it progressively drops in performance.
- However, i feel it is inconclusive that this approach is good as it is missing the analysis on inference time. If there isn't an improvement, why is there a need for the speedup anyway?
# Learning Gaps
- Speech recognition datasets
# Simplify/Analogies
- Changing the up to the last 4 layers to feedforward layers did maintain performance.
