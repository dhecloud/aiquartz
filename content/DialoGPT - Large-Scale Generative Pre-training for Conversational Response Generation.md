Author(s): [[Yizhe Zhang]], [[Siqi Sun]], [[Michel Galley]], [[Yen-Chun Chen]], [[Chris Brockett]], [[Xiang Gao]], [[Jianfeng Gao]], [[Jingjing Liu]], [[Bill Dolan]]
Tags: #language_model, #Dialogue_Modelling, #transformer, #Conversational_Dialogue_Systems, #academic_papers
Read on: [[July 18th, 2020]]
URL: http://arxiv.org/abs/1911.00536
# Main Contribution(s)
- Provides [[DialoGPT]], which is [[GPT-2]] trained on 147M conversation-like exchanges
# Summary
    Architecture is copied from [[GPT-2]]; 117M (768d), 345M (1024d), 762M (1280d) 
    A [[Maximum Mutual Information (MMI)]] scoring function is used to prevent bland, uninformative samples.
- Pretrained backward models used to predict source sentences from given responses.
    ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2Fimvp8wHXe5.png?alt=media&token=104a526f-f805-45f4-bf4a-4e2a11a97696)
- Medium sized model comes very close to human performance in many automatic metrics
    Retains the potential to generate output that may trigger offense
# Learning Gaps
-
# Simplify/Analogies
- GPT finetuned on dialog data
