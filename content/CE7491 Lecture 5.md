---
---
- Date: [[September 9th, 2020]]
- [[Batch Normalization]] reduces internal covariate shift, improves optimization. Estimates Mean and Standard Deviation for each minibatch, but might not be possible during test time.
- Use running average of values during training for testing 
- Allows higher learning rates, faster convergence
- Networks becomes more robust to initialization
- Makes optimization landscape significantly smoother
- [[Switchable Normalization]] Learns to select different normalizers for different layers
- 
