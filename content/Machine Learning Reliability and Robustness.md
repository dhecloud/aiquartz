Speaker(s): [[Besmira Nushi]] (host), [[Thomas Dietterich]], [[Ece Kamar]], [[Suchi Saria]]
Tags: #seminar
Held on: [[July 22nd, 2020]]
URL: [event page](https://www.microsoft.com/en-us/research/event/frontiers-in-machine-learning-2020/#!wednesday-july-22), [youtube](https://www.youtube.com/watch?v=JmcIE1zUDIM&feature=emb_logo)
- Talk 1: Anomaly Detection in Machine Learning and Computer Vision, by [[Thomas Dietterich]]
- Use cases
        1. Open Category Detection
        2. Novel Sub-category Detection
        3. Out of Distribution Detection
        4. Data Clearning
        5. Fraud Detection, Cyber Attacks
- Technical Approaches
        1. Density Estimation
        2. Distance Based Methods
        3. Projection Methods
        4. Robeust Estimation
- Anomaly Detection in [[Computer Vision]]
- No easy distance metrics
- High dimensions
- High degree of nuisance novelty
- Method 1: Classifiers-Based Approaches: 
- Indecision (similar to probablities models)
- Should not work as classifier should discard information that are irrelevant to classification, but it works pretty well, indicating that deep learning methods are not throwing away information
- Probabilities Models
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FkJkDOhI3de.png?alt=media&token=fd3b8f5e-f2b4-4bd8-8338-4a605ef4f2d1)
Pertubation
- Method 2: Autoencoders
- Method 3: Normalizing Flow models
- Method 4: Distance Functions
- Method 5: Auxiliary Tasks
- Concluding Remarks
- Anomaly detection is important and critical for robust AI systems
- Anomaly detection is difficult and very challenging especially for images
- Research is advancing rapidly with **little theoretical understanding**
- Talk 2: AI in the Open World, Discovering Blind Spots of AI, by [[Ece Kamar]]
- Responsible AI emerges from understanding AI limitations in the open world
- There is no silver bullet, but variety of emerging techniques
- Aligning efforts with AI development cycle is key
- Blind Spots in Data
- It is assumed that training data is representation of the real world, but that is often not the case (or not the way we want it to be)
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2Fgy-Cvgt3Rj.png?alt=media&token=b9d517db-8a1c-42d5-9cfa-ae3cfd64ca0e)
Pandora: Error Analysis for ML systems 
- Backward compatibility for AI systems
- Updates to a model can break system performance
- Need to preserve robustness, error handling, maintenance.
- Takeaways
- Reliability and safety risks carry societal implications
- Understanding AI limitations is key
- Need for algorithmic advances as well as tools, design guidelines and frameworks for empowering developers and users
- Talk 3: Implementing Safe and Reliable ML: 3 key areas of development, by [[Suchi Saria]]
- X-rays have style features that hurt robustness when we go from one site to another
- Feedback loops in predictive systems
- Practice evolves over time and naively trained ML models can behave in unexpected ways
- Engineering for reliability is critical!
- Is ML components behaving the way we expect it to behave? When is it behaving in biased ways? Stochastic nature of ML makes this challenging
- It is designed to be fair and ethical?
- How can we ensure privacy when applying ML to senstive data
- What can a malicious adversary do to a ML system?
- ML is NOT inherently biased! ML algorithms provide a representation of data
- Model validation and maintenance typically 10x+ harder than training
- Ensure Reliability via real time audits
- Panel Discussion
- [[Thomas Dietterich]]: Big mystery why when we try to introduce robustness in one direction, we introduce brittleness in some other direction
- [[Suchi Saria]]: Domain specific measures are the most important (over general metrics like AUC) as they really determine the level of accuracy. 
- [[Transportability]] which is to identify certain causal truths or premises that will be not changed (eg bacterial strain -> bacterial flu). By building algorithms around these truths, we can ensure that the algorithm is more robust.
