Author(s): [[Ryuichiro Higashinaka]], [[Luis F. D’Haro]], [[Bayan Abu Shawar]], [[Rafael E. Banchs]], [[Kotaro Funakoshi]], [[Michimasa Inaba]], [[Yuiko Tsunomori]], [[Tetsuro Takahashi]], [[João Sedoc]]
Tags: #datasets, #survey, #Conversational_Dialogue_Systems, #academic_papers
Read on: [[June 20th, 2020]]
URL: http://workshop.colips.org/wochat/@iwsds2019/documents/dbdc4-overview-higashinaka-etal.pdf
# Main Contribution(s)
- Provides a summary of the approaches and results of the teams in the challenge
# Summary
- 4th iteration of [DBDC]([[The Dialogue Breakdown Detection Challenge - Task description, Datasets, and Evaluation Metrics]])
- More emphasis of [[Mean Squared Error]] related metrics as they were found to be more reliable 
- [[datasets]] used was the dialogue sessions made with [[IRIS dialogue system]] and also the [ConvAI2]([[Conversational Intelligence Challenge 2]]) dataset
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2Fx8vSpc0xU6.png?alt=media&token=895d97cb-ba34-4f7a-a77a-0836cc50a461)
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FarZeWc3_AF.png?alt=media&token=65213acb-8a31-4bce-9d75-5bac60a09d01)
- For English, a Random Forest Regressor and an LSTM-based method performed the best. MSE(NB,PB,B) is 0.0336 and MSE(NB+PB,B) is 0.0369
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2F8MdCZA6Qjd.png?alt=media&token=21bf93ae-7f11-44f6-bc10-d346a7e5aae0)
- For Japanese, a [[BERT]] model performed the best. MSE(NB,PB,B) is 0.0463 and MSE(NB+PB,B) is 0.0507
- It is interesting to note that BERT did not do well for the English dataset.
- Could be a fine-tuning hyperparamter issue for the english BERT model
# Learning Gaps
- The exact training procedure of each team
# Simplify/Analogies
- N/A
