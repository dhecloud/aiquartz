Author(s): [[Longteng Guo]], [[Jing Liu]], [[XinXin Zhu]], [[Xingjian He]], [[Jie Jiang]], [[Hanqing Lu]]
Tags: #Non-Autoregressive, #Image_Captioning, #academic_papers
Read on: [[August 24th, 2020]]
URL: https://arxiv.org/abs/2005.04690
# Main Contribution(s)
- Introduces the [[Counterfactuals-Critical MultiAgent Learning (CMAL)]] framework for training on an [[Image Captioning]] task
# Summary
- Formulates the task an an [[Multi-Agent]] [[Reinforcement Learning]] System, where positions in the target sequence are viewed as agents to maximize the quality of the whole sentence
- [[REINFORCE]] algorithm used for training the agents
- The [[Counterfactual]] baseline refers to the expected reward when marginalizing out a single agent action's while keeping other agents actions fixed.
- Used to mitigate the high variance of gradients
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2F1qLDJsFViU.png?alt=media&token=3a4be54e-886c-4dd8-8457-e807c40ad18a)
- Results
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FftzD7O-V9g.png?alt=media&token=e3d354ce-5911-497e-8854-cc555580b861)
Results on the [[MSCOCO]] dataset for image captioning
# Learning Gaps/Thoughts
-
# Simplify/Analogies
-
