Author(s): [[Bei Li]], [[Ziyang Wang]], [[Hui Liu]], [[Yufan Jiang]], [[Quan Du]], [[Tong Xiao]], [[Huizhen Wang]], [[Jingbo Zhu]]
Tags: #Neural_Machine_Translation, #academic_papers
Read on: [[December 1st, 2020]]
URL: https://arxiv.org/abs/2010.03737
# Main Contribution(s)
- Develops a [[Shallow-To-Deep (SDT) (Algorithm)]] which allows for a 54-layer encoder to be trained.
# Summary
#  Motivation
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FsYpNF4lYvp.png?alt=media&token=a5d7b69f-1f08-4583-860e-170fadfe5af1)
**a)** Similarity between each layer and the input layer decreases as it gets further from the input layer. This suggests that the model is using learning more representations (**not sure if this is the correct implication**). The similarity also does not converge for 6 and 12 layers, suggesting more layers is needed for better representation
**b)** Similarity between adjacent layers have high similarity. **Creates the possibility of initializing higher layers from lower layers**.
**c)** Representation of a position tend to be close to the global representation (mean vector of a sequence) for higher level layers. This suggests smoothing the representation over different positions indicating better robustness and sensitivity.
#  [[Shallow-To-Deep (SDT) (Algorithm)]] training algorithm
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FlkxzQprYe7.png?alt=media&token=cf35a153-b6ec-4adc-9a40-937b3ae3565c)
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2F4WAaqa7YrW.png?alt=media&token=5e52d552-1555-478d-8286-957cc79529d6)
Sparse connections are required as using dense connections between every layer creates a huge memory footprint.
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FQ3mIB-va5B.png?alt=media&token=595a8c59-e083-4a45-8aad-1f176cbe9bff)
[[Learning Rate]] restart is also required to cater to the newly stacked model and deep layers.
#  Experiments
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FmfLb30Ex11.png?alt=media&token=fb8c641c-73df-47a0-bc29-a70823b92b9a)
Results on [[WMT14 En-De]], [[WMT14 En-Fr]].
#  Ablations
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FkWlIiCxxcz.png?alt=media&token=0b775309-9dfe-4c96-82e1-7f81b118b7a2)
Using a pretrained model to build a deeper model
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FsVSRjOb34s.png?alt=media&token=a553d11f-d3ca-4d33-84d0-77ccf6cf9037)
inter-similarity and emb-similarity continue to rise and decline respectively
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FnUhlvTqys3.png?alt=media&token=01cd203d-9804-41f6-a912-ee1348bbc075)
Decreasing similarity until level 48
# Learning Gaps/Thoughts
- Felt like many experiments were interpreted; and inferences were kind of a stretch.
- Interesting paper nonetheless
# Simplify/Analogies
