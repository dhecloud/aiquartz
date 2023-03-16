Author(s): [[Tianlong Chen]], [[Jonathan Frankle]], [[Shiyu Chang]], [[Sijia Liu]], [[Yang Zhang]], [[Zhangyang Wang]], [[Michael Carbin]]
Tags: #meta-learning, #BERT, #Lottery_Ticket_Hypothesis, #academic_papers
Read on: [[July 30th, 2020]]
URL: https://arxiv.org/abs/2007.12223
Code: https://github.com/TAMU-VITA/BERT-Tickets
# Main Contribution(s)
- Find matching subnetworks between 40% and 90% sparsity in BERT models on standard [[GLUE Benchmark]] and SQuAD downstream tasks, using **pre-trained initialization**
- Show that subnetworks found using the [[Masked Language Modelling]] task are **universal **and transfer to other tasks while maintaining accuracy, unlike task-specific subnetworks which do not transfer to other tasks
# Summary
    Two key themes have emerged from the [[Lottery Ticket Hypothesis]]
- 1.  **Initialization via pre-training**
- 2. **Transfer learning**
    The authors use a mask to dictate the subnetwork. In other words, the subnetwork is the __original network__ $$\odot$$ __mask__ to set some weights to 0
    [[Iterative Magnitude Pruning]] is used to identify subnetworks
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FouAV8zF2cd.png?alt=media&token=3836d73b-25f1-4446-bf89-4ccf832c5f74) This basically determines the pruning mask by training the unpruned network to completion on a task and pruning individual weights with the **lowest magnitudes** globally
    ## Claim 1:  [IMP]([[Iterative Magnitude Pruning]]) finds winning tickets
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FrSp9CIo2_o.png?alt=media&token=dea8d819-d092-4f96-baf0-127bf5cf97ac)True. Subnetworks are able to come within one standard deviation of the original [[BERT]] performance
    ## Claim 2: [IMP]([[Iterative Magnitude Pruning]]) winning tickets are sparser than randomly pruned or initialized subnetworks.
        ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FJR6yU53c-I.png?alt=media&token=2fbf7327-a98d-41d0-b800-04277a274654)True. [IMP]([[Iterative Magnitude Pruning]]) winning tickets generally performs better even at higher sparsity.
    ## Claim 3: [[Rewinding]] improves performances
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2Fg6yVnwUcIM.png?alt=media&token=01d31b8e-8ef6-4ee1-b82c-59bb12c0842a)False. Rewinding does not notably improve performance for any downstream task
- A departure from prior work where rewinding at worst had no effect on accuracy.
- It is also important to note that rewinding was not needed in this paper, as winning tickets was found in non-trivial sparsities
    ## Claim 4: [IMP]([[Iterative Magnitude Pruning]]) subnetworks match the performance of standard pruning
- Depends on task. See table 3 above.
    ## Question 1: Do winning tickets transfer?
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FyeDxd7AKhB.png?alt=media&token=d7ac9453-8398-4695-9764-7cbd839e24d2) Generally, no. Only 3 source tasks transfer to more than two other tasks (squad, mlm, pruning). Even then, only [[Masked Language Modelling]] transfers easily to other tasks, while squad and pruning tasks only transfer to 4 other tasks.
    ## Question 2: Are there any patterns in subnetwork transferability?
- Seems to correlate with number of training examples. 
- ==**Authors do not observe any evidence that transfer is related to task type**==
    ## Question 3: Does initializing to $$\theta_0$$ lead to better transfer?
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FNceqDOpAYu.png?alt=media&token=9f50369e-a0f8-48bf-b482-a4da74471580) In nearly all cases, [[Rewinding]] to $$\theta_0$$ after finding the winning ticket leads to the same or higher performance on target tasks, and standard pruning also has little detrimental effect on transfer performance.
# Learning Gaps
- Would be interesting to compare the size of [[DistilBERT]] against the sparse network found
# Simplify/Analogies
- Remove the smallest magnitude weights until performance on a task drops to determine how sparse a subnetwork can get.
