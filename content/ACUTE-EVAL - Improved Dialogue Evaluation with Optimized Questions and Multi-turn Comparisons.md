Author(s): [[Margaret Li]], [[Jason Weston]], [[Stephen Roller]]
Tags: #Evaluation_Metric, #Conversational_Dialogue_Systems, #academic_papers
Read on: [[June 24th, 2020]]
URL: http://arxiv.org/abs/1909.03087
# Main Contribution(s)
- Presents a new evaluation method with a clear mechanism that provides fast, cheap iteration
- Compares the currently best performing retrieval and generation models on [[PersonaChat]] and [[Wizard of Wikipedia]]
# Summary
- Single-turn pairwise evaluation fail to take into account the multi-turn aspect
- Multi-turn [[Likert Scores]] require annotator to have a multi-turn conversation and then provide an integer score; but scores suffers from variance and bias from annotators
#  [ACUTE-EVAL]([[ACUTE-EVAL - Improved Dialogue Evaluation with Optimized Questions and Multi-turn Comparisons]]) evaluation metric
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FgbwnMIyLz4.png?alt=media&token=4c0b8a87-e4ac-427c-8c5c-7c515dc1403f)
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FPO9cNmFTLq.png?alt=media&token=57f6cb0d-1687-4748-b7fb-7a9d8dee8429)
- Ask annotators to make ==binary judgements== between sampled pairs from the logs, and then collate results
#  Experiments/Findings
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2F8OF9SYkfJ5.png?alt=media&token=0810d94a-2591-4061-8c68-4e4da5c9544f)
- Compare 2 state of the art models, one Polyencoder, another by HuggingFace 
- Find that retrieval models outperform generative models for both [[PersonaChat]] and [[Wizard of Wikipedia]]
- Find that ACUTE-EVAL can be a more sensitive test, which more often yield significance.
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FQnWuk7bC-y.png?alt=media&token=f27c888a-2103-403d-b88c-ecfeb3d5315c)Self-chat ACUTE-EVAL also requires less person-hours for evaluation while achieving significance.
# Learning Gaps
- [[Likert Scores]]
# Simplify/Analogies
