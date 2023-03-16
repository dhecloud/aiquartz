Author(s): [[Daniel Adiwardana]], [[Minh-Thang Luong]], [[David R. So]], [[Jamie Hall]], [[Noah Fiedel]], [[Romal Thoppilan]], [[Zi Yang]], [[Apoorv Kulshreshtha]], [[Gaurav Nemade]], [[Yifeng Lu]], [[Quoc V. Le]]
Tags: #Evaluation_Metric, #Conversational_Dialogue_Systems, #academic_papers
Read on: [[June 25th, 2020]]
URL: https://arxiv.org/abs/2001.09977
# Main Contribution(s)
- Present [[Meena]], a 2.6B parameter neural network
- Propose a human evaluation metric called [[Sensible and Specificity Average (SSA)]] which has strong correlation between perplexity and SSA
# Summary
#  [[Sensible and Specificity Average (SSA)]]
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FjYfwoCWEP8.png?alt=media&token=6126b153-b9e9-40cb-89d1-f213693e9a4d) ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FZCOjGdFjXq.png?alt=media&token=39eed76f-3def-47a2-a825-b04781123256)
- 2 dimensions: sensibleness (make sense) and specificity (not giving generic answer)
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2Fs4aIprq1Ey.png?alt=media&token=8cd5862f-32f8-4822-91ab-b37cd7df023c)Perplexity as an automatic evaluation correlates with [[Sensible and Specificity Average (SSA)]]
- A few tricks were used to improve the interactive SSA score.
- Automatically remove candidates that are detected as repetitions across turn
- Sample and Rank {{[[embed]]: ((QooEn-D6i))}}
- Also create a [[Mini-Turning Benchmark (MTB)]] by compiling single-turn contexts from multiple sources for static evaluation
#  [[Meena]] chatbot
- Trained on 341GB of text, 40B words. In comparison, GPT-2 has 40B text
- Architecture is a 2.6B parameter Evolved [Transformer]([[transformer]]) which scored 10.2 perplexity. 2560 hidden size, 32 attention heads, maximum length of 128
- Vanilla [[Transformer]] scored 10.7
- [[GPT-2]] has 1.5B parameters
- [[DialogGPT]] has 762M parameters
- [[Sample-and-Rank]] is introduced. Sample N independent candidates (not top-k) from whole distribution, then select the candidate response with the highest probability.
- Used in conjunction with temperature. In the experiments, N=20 and T=0.88
# Learning Gaps
- The other two chatbots, [[Mitsuku]]
# Simplify/Analogies
- Follow GPT style of using more data and throwing more compute to achieve a better chatbot.
- SSA is a metric with 2 dimensions which correlates with human judgements
- However, 2 dimensions might be too little, could be a coincidence.  
