Author(s): [[Ahmad Rashid]], [[Alan Do-Omri]], [[Md. Akmal Haidar]], [[Qun Liu]], [[Mehdi Rezagholizadeh]]
Tags: #Neural_Machine_Translation, #Generative_Adversarial_Network_(GAN), #academic_papers
Read on: [[November 27th, 2020]]
URL: https://arxiv.org/abs/2011.05449
# Main Contribution(s)
- Proposes [[Bilingual Adversarial Text Generator (B-GAN) (Architecture)]]
# Summary
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2Fi6Yho7SAza.png?alt=media&token=e4e88277-eeba-4efe-9d91-d848abdc8107)
- Uses three types of losses
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FKmY9Y92Ati.png?alt=media&token=0d40f95c-547d-411b-9928-9f714b0dcc1a)
[[Reconstruction Loss]], standard [[Auto-Encoders]] loss
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FZBYtr2ClqA.png?alt=media&token=eff6c748-af79-491c-b186-106ba1498939)
[[Cross-Domain Loss]], which is similar to back-translation 
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2F4Gf972h0vP.png?alt=media&token=0760db47-464b-4ed6-8e45-9bee629b392b)
Hinge version of [[Adversarial Loss]]
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FEX3Iyp8t5R.png?alt=media&token=11b02fa7-3a38-4629-bb85-793803f033ff) ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FcupXmfr_5i.png?alt=media&token=9ae7d510-5b67-4f77-b3b8-1cf66ba0516e)
Results on [[Multi30k]], sampled  100000 sentences from monolinguial [[News Crawl 2007 English]], [[News Crawl 2007 French]], [[News Crawl 2010 English]], [[News Crawl 2010 French]]
# Learning Gaps/Thoughts
- Nothing much, seems to reinforce the idea that autoencoders can contain information for two languages
# Simplify/Analogies
-
