Author(s): [[Sintiani Teddy]], [[Edmun M-K Lai]], [[Chai Quek]]
Tags: #Cerebellar_Model_Articulation_Controller_(CMAC), #academic_papers
Read on: [[November 8th, 2020]]
URL: https://www.researchgate.net/publication/5797287_Hierarchically_Clustered_Adaptive_Quantization_CMAC_and_Its_Learning_Convergence
# Main Contribution(s)
- Introduces [[Hierarchical Clustering]] for [[Cerebellar Model Articulation Controller (CMAC)]] to allocate more memory cells to these regions, hence improving efficiency and generalization
# Summary
- Uniform quantization for inputs might result in suboptimal memory space utilization. Two approach to deal with this:
        1. Use multilayer CMACs of increasing resolution. Another layer is added until the error is reduced to an acceptable level
        2. Use varying quantization step-sizes. Can be done by doing competitive learning, data clustering, etc.
- Number of layers in a [[Cerebellar Model Articulation Controller (CMAC)]] is determined by the number of quantization functions
- [[Hierarchically Clustered Adaptive Quantization CMAC (HCAQ-CMAC) (Architecture)]] allocates more memory cells to the input regions where rapid fluctuations of the output values are observed, and less memory to regions with relatively unchanged output values
- Network Initialization Stage - to define the quantization function at each of the input dimension. The [[Agglomerative Hierarchical Clustering]] technique is used to identify the optimal quantization decision function in each of the input dimensions
- However is not able to automatically determine the optimal number of quantization clusters
- Network Learning Stage - to learn memory contents. The [[Widrow-Hoff]] learning rule is adopted for this
- Learning converges if and only if learning rate $$0 < \alpha < 2$$ 
- Small network size does not affect accuracy and fine-tuning capability of the [[Hierarchically Clustered Adaptive Quantization CMAC (HCAQ-CMAC) (Architecture)]]. 
- Online learning not suitable
# Learning Gaps/Thoughts
# Simplify/Analogies
