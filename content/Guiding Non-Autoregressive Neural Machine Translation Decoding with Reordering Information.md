Author(s): [[Qiu Ran]], [[Yankai Lin]], [[Peng Li]], [[Jie Zhou]]
Tags: #Non-Autoregressive, #Neural_Machine_Translation, #academic_papers
Read on: [[May 23rd, 2020]]
Reread on: [[August 25th, 2020]]
URL: https://arxiv.org/abs/1911.02215
- ### Main Contributions
- Proposes the **ReorderNAT** to model the reordering information in the decoding procedure
- Introduce a deterministic and non-deterministic decoding strategy
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FAGwzUIF_4s.png?alt=media&token=20d8fa98-612f-4c93-88ca-46c8e6311c35)
- Basically they used a smaller decoder for the reordering module, and a main decoder for the final decoder module
- The deterministic guiding decoding (DGD) is simply greedy argmax, while the non-deterministic guiding decoding (NDGD) is simply using the probability distribution.
- Results
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FqJG0GCMfiu.png?alt=media&token=f0ad8f77-d31f-41a1-a2a4-5fd9a0d2046a)
Trained on [[WMT14 En-De]], [[WMT14 De-En]], [[IWSLT16 En-De]], [[IWSLT16 De-En]], 
validate on [[newstest2013 De-En]], [[newstest2013 En-De]], [[newsdev2016 En-Ro]], [[newsdev2016 Ro-En]]
test on [[newstest2014 En-De]] [[newstest2014 De-En]], [[newstest2016 En-Ro]], [[newstest2016 Ro-En]] [[IWSLT16 En-De]]
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FWMSjd6mJlH.png?alt=media&token=b0b083dd-df8c-40fc-a389-4b8c755da82e)
validate on [[NIST02]]
test on [[NIST03]], [[NIST04]], [[NIST05]], [[NIST05]], [[NIST06]], [[NIST08]] 
- ### Thoughts
- Using multiple encoder/decoders seems to be becoming more popular?
