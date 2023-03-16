Author(s): [[Mahdi Namazifar]], [[Alexandros Papangelis]], [[Gokhan Tur]], [[Dilek Hakkani-Tür]]
Tags: #language_model, #Question-Answering_Dialogue_Systems, #Natural_Langauge_Understanding, #academic_papers
Read on: [[December 1st 2020]]
URL: https://arxiv.org/abs/2011.03023
# Main Contribution(s)
Maps [[Natural Langauge Understanding]] problems to [[Question Answering]] problems in low data regimes using [[Transfer Learning]]
# Summary
![[Pasted image 20201201215251.png]]
- Frames the [[Slot Detection]] and [[Intent Detection]] task as a [[Question Answering]] task. 
- Trained on the [[ATIS]] and [[Restaurants-8k]] dataset.
- ![[Pasted image 20201201215629.png]]Transfer learning is done training pretraining on [[ATIS]] and then finetuning on samples from [[Restaurants-8k]]


# Learning Gaps/Thoughts
- Seems like another [[Transfer Learning]] task. The idea of standaring different tasks as a [[Question Answering]] task is not novel and has been raised in [[Text-To-Text Transfer Transformer]]
# Simplify/Analogies
-	