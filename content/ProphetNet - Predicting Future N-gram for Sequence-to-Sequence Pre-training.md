Author(s): [[Yu Yan]], [[Weizhen Qi]], [[Yeyun Gong]], [[Dayiheng Liu]], [[Nan Duan]], [[Jiusheng Chen]], [[Ruofei Zhang]], [[Ming Zhou]]
Tags: #summarization, #academic_papers
Read on: [[June 2nd, 2020]]
URL: https://arxiv.org/abs/2001.04063
# Main Contribution(s)
- Propose ProphetNet which predicts the next n tokens based only on previous context.
# ELI5
- Using the already formed sentences, predict the next few words
# Summary
# # Rationale behind this approach
- AR-based models may prefer to focus on the latest tokens rather than capture long-term dependencies for the next token prediction
- Local correlations such as bigram combinations are stronger than long time dependenceis
- Teacher forcing does not help the model in future token planning and modelling.
# # ProphetNet
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FX_Q4J1yiqt.png?alt=media&token=7bf468c7-84e2-4e52-8a5d-11df4f18259e)
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2F9JzL3RsMWx.png?alt=media&token=8370483c-18f4-4f94-9c21-1f92dd1a5b9d)
- The authors also train on summarization, instead of translation. Not very sure why.
- The authors modify the self-attention into a N-stream self attention. The paper is not very clear on this, but it seems as though there will more than 1 input for each sample.
# Learning Gaps
- What exactly is N-stream?!
# Simplify/Analogies
- Using more than 1 streams, we can predict n-steps ahead.
