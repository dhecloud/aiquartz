Author(s): [[Dorin Comaniciu]], [[Peter Meer]]
Tags: #academic_papers
Read on: [[September 24th, 2020]]
URL: https://ieeexplore.ieee.org/document/790416/
# Main Contribution(s)
- Proposes to use the [[Mean Shift Estimate]] of the gradient to perform processing in the spatial-range domain: filtering, and segmentation
# Summary
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2F0NNByUGLcM.png?alt=media&token=f37d7836-8364-45cc-bc0a-fc2ba08dabac)
The sample mean shift
- Always points to the direction of the maximum increase in density, hence can define a path leading to a local density maximum.
- The Mean Shift procedure which is a loop of i) computation of the mean shift vector  $$M_h(x)$$, and ii) the translation of the window $$S_h(x)$$ by $$M_h(x)$$, ==is guaranteed to converge==
#  [[Mean Shift Filtering]]
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FiL1XZIuje1.png?alt=media&token=8cca45ac-885b-455c-a4c6-1c51610f5da9)
- Arithmetic complexity: $$k_c(2\lfloor \sigma_s \rfloor +1)^2$$ flops per image pixel
- $$\sigma$$ is the range of color resolution
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FMnA1bhs4JI.png?alt=media&token=6d7b0e56-8a5d-4337-9bed-26020fd16453)
# # Comparison to [[Bilateral Filtering]]
- [[Bilateral Filtering]] uses a static window in the two domains, which mean shift window is dynamic.
- Stopping criterion is needed for [[Bilateral Filtering]], but not for [[Mean Shift Filtering]], since convergence is ensured.
#  [[Mean Shift Segmentation]]
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FOLhtB8IVn7.png?alt=media&token=8f6fbe41-dafe-4ff7-b3a1-4aa5e4f256f6)
- Arithmetic complexity: similar to [[Mean Shift Filtering]] ie $$k_c(2\lfloor \sigma_s \rfloor +1)^2$$ flops per image pixel. First step is the most computationally expensive
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FyocqqTblMV.png?alt=media&token=8463240f-4b3e-478c-9b3e-887cc0647638)
# # Comparison with [[Attraction Force Field]] and [[Edge Flow Propagation]]
- [[Mean Shift Segmentation]] has strong statistical foundations
- [[Attraction Force Field]] computes at each pixel a vector sum of pairwise affinities between current pixel and all other pixels. ==No theoretical evidence of the existence of such a force field is given==
- [[Edge Flow Propagation]] is  the magnitude of the gradient of a smooth image at each location for a given set of directions. Quantization might introduce artifacts
# Learning Gaps/Thoughts
-
# Simplify/Analogies
-
