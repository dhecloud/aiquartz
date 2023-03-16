Author(s): [[JinYeong Bak]], [[Alice Oh]]
Tags: #Evaluation_Metric, #Conversational_Dialogue_Systems, #academic_papers
Read on: [[June 15th, 2020]]
URL: https://arxiv.org/abs/2006.07015
# Main Contribution(s)
- Propose an automatic evaluation model to judge generated conversations
# ELI5
- SSREM uses speaker sensitive samples to output a score for generated conversational dialogue 
# Summary
- Speaker utterances are categorized into: 1. `Random`, 2. `Same Speaker`, 3. `Same Partner`, 4. `Same Conversation`
- These utterances are converted into vectors using [[GloVe Twitter 200d]]
-  The model is trained on the [[Twitter Conversation Corpus (Bak and Oh, 2019)]]
- [[Amazon Mechanical Turk]] is also used to generate human scores of responses to compare against SSREM and other evaluation metrics
- [[BLEU]], [[ROUGE]], [[EMB]], [[RUBER]]
#  Experiment 1 - Comparing with Human Scores
- SSREM uses the sentence mover's similarity as the function for computation.
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2F5NGhO46mRi.png?alt=media&token=403f905d-2cca-49a0-81d3-4a896dc1282d)
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2F3O-SU96YlB.png?alt=media&token=cc709ee1-b892-4266-8207-1408088fad2e)
- SSREM shows higher correlation for the other automatic metrics.
#  Experiment 2 - Identifying True and False Responses
- `True` - ground truth responses, `False` - any of the 4 speaker utterance categories mentioned in above
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FVXdHUW6vJ6.png?alt=media&token=692ed3ed-98d9-4958-827f-8fbeb3f972de)
- SSREM consistently grades the ground truth responses significantly over the other false labels
#  Experiment 3 - Applying New Corpus
- Test on [[Movie Scripts (Danescu-Niculescu-Mizil and Lee, 2011)]]
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2F7gvupEn10d.png?alt=media&token=73280044-5186-4ca2-83ed-b3c29d8149ce)
- Even though the correlation matrix is significantly lower, there is a clear correlation with human scores over the other automatic metrics
- Shows some potential for cross domain usage without fine-tuning 
# Learning Gaps
- Not familiar with this literature, so not sure what to look out for. 
- I guess Twitter conversations are typically shorter, making it easier
# Simplify/Analogies
- Authors find a way to find dissimilar utterances (speaker sensitive samples) to train the model with.
