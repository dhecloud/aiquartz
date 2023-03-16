Author(s): [[Abdelrhman Saleh]], [[Tovly Deutsch]], [[Stephen Casper]], [[Yonatan Belinkov]], [[Stuart Shieber]]
Tags: #critique, #Conversational_Dialogue_Systems, #academic_papers
Read on: [[June 16th, 2020]]
URL: https://arxiv.org/abs/2006.08331
Code: https://github.com/AbdulSaleh/dialog-probing
- [[ParlAI]] used for building system
# Main Contribution(s)
- Analyze open-domain Dialog systems and **evaluate the quality of these representations**
- Meaning they do not evaluate the text itself, but the encodings
- Find that the dyadic turn-taking nature of dialog is not fully leveraged by these models 
# ELI5
- Models encode information in their parameters. This paper checks if this information is sufficient for neural conversational dialogue
# Summary
#  Objectives
- 1. Do neural dialog effectively encode information about conversation history?
- 2. Do neural dialog models learn basic conversational skills through end-to-end training?
- 3. To what extent do neural dialog models leverage the dyadic, turn-taking structure of dialog to learn these skills
- The authors carry out perturbation (probing) experiments to test if models fully exploit dialog structure
- 3 Architectures are used for testing
- 1. [[Recurrent Neural Networks]]
- 2. [[Recurrent Neural Networks]] with Attention
- 3. [[Transformer]]s
- Small models are trained from scratch on the [[DailyDialog]] dataset and larger models are pretrained on [[WikiText-103]] and then fine-tuned on [[DailyDialog]]
- [[GloVe]] is also used as a simple baseline.
- The assumption here is that if a model learns certain conversational skills, then ==knowledge of these skills should be reflected in its internal representations== 
#  Perturbation Experiments
- There are 8 probing tasks
- 1. [[TREC]] - probe for question answering using the TREC question classification dataset
- 2. [[DialogueNLI]] - Authors change the second utterance in a pair to simulate and mimic a second speaker.
- 3. [[MultiWOZ 2.1]] - Probe for NLU.
- 4. [[Schema-Guided Dialog (SGD)]] - to track user intent over multi turns
- 5. [[Winograd NLI]] - Check for commonsense reasoning
- 6. [[SNIPS]] - Intent classification 
- 7. [[ScenarioSA]] - Sentiment classification probing task
- 8. [[DailyDialog]] - Inferring topic of conversation
#  Results
# # Quality of Encoder Representations
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FalOAwXj7z4.png?alt=media&token=7428b7cc-9013-4e67-a993-19db173928c9)
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FPhV6S_OSAI.png?alt=media&token=3722e130-9389-4ce5-97bb-7b57b5c6f086)
- Multiple models still fail to effectively encode information about the conversation history
# # Probing Conversational Understanding
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FTJr7sb2JI2.png?alt=media&token=cf3b59b3-1380-4f8b-860e-506681a9e77d)
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FL6QfyzpGde.png?alt=media&token=1f075091-cd51-49da-a1ea-b0b6f25e4bf0)
    - GloVe baseline outperforms the small recurrent models 
    - GloVe perform as well as large pre-trained models
   - Large pre-trained models do not seem to master basic conversational skills either; no advantage over GloVe
# # Effect of Dialog Structure
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FPeEjRYMuS0.png?alt=media&token=6346b795-2f04-4bdc-92b5-df65d83c1bee)
    - Dialogue structure is important due to the ==dyadic, turn-taking nature of conversations==
    - Models trained on ordered data outperformed models trained on shuffled data
   - This difference in performance is most obvious in transformers
- These observations are ==**only indicative of the encoder representations**==. As good as the representations might be, the actual generated dialogue might differ in quality because of limitations in the decoder.
# Learning Gaps
- Not much, but i fail to see a strong rationale for this paper. Encodings are already hard to decipher as it is, and trying to explain using hindsight is quite a slippery slope
# Simplify/Analogies
- Authors probe encoders to check for semblance of NLU using 8 tasks. 
- They find that small models in particular do not effectively encode information about conversation history, basic conversational skills, and fail to leverage the dyadic turn-taking structure of dialogue.
- Larger models are less affected but still severe.
