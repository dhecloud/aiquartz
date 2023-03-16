Author(s): [[Sintiani Teddy]], [[Chai Quek]], [[Edmun M-K Lai]]
Tags: #Cerebellar_Model_Articulation_Controller_(CMAC), #academic_papers
Read on: [[November 9th, 2020]]
URL: https://ieeexplore.ieee.org/abstract/document/4469949/
# Main Contribution(s)
- proposes the [[Pseudo-Self Evolving CMAC (PSECMAC) (Architecture)]] that non uniformly allocates its computing cells
# Summary
- The [[Pseudo-Self Evolving CMAC (PSECMAC) (Architecture)]] is a single layered self-organizing multiresolution computation model of the cerebellum. The memory quantization step sizes are adapted based on the computed information distribution of the training data
- Two phased learning process - structural learning and parameter tuning.
- Memory allocation and nonuniform quantization process
- The PSEC algorithm is a density-based cluster algorithm which couples the advantages of incremental learning and the learning vector quantization. This algorithm computes the data density clusters
- Memory allocation is done according to the computed density cluster
- Quantization step size increases in response to a lower density of the observed training data
-  Computational process
- Weighted Gaussian neighborhood output (WGNO) to minimize the influence of the input quantization error. A set of neighborhood bounded computing cells will be activated to derive the network output response to the given input stimulus.
- Learning process
- Combines the [[Widrow-Hoff]] training algorithm with the Gaussian weighting function.
- Learning convergence
- Converge if the learning constant $$0 < \alpha \leq 2$$
# Learning Gaps/Thoughts
# Simplify/Analogies
