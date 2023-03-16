Author(s): [[Alexei A. Efros]], [[Thomas K. Leung]]
Tags: #Computer_Vision, #Texture_Synthesis, #academic_papers
Read on: [[September 24th, 2020]]
URL: https://www2.eecs.berkeley.edu/Research/Projects/CS/vision/papers/efros-iccv99.pdf
# Main Contribution(s)
- Introduces a non-parametric method for texture synthesis 
# Summary
- Applies the idea of n-gram from text to texture.
- Texture is modelled as a [[Markov Random Field]], and assume that the probability distribution of brightness values for a pixel given the brightness values of its spatial neighbourhood is independent of the rest of the images.
- The window size which determines the neighborhood is a hyperparameter. 
#  Synthesizing one pixel
- For a sample image, $$I_{smp}$$, which is extracted from a real image $$I_{real}$$, we want to synthesize a new image $$I$$. Pixel $$p \in I$$ and width $$w(p) \subset I$$ whereby a square image patch of width $$w$$ is centered at $$p$$.
We want to find a similar $$w(p)$$ in $$I_{smp}$$. We can do this using a heuristic
- $$d_{SSD}$$Normalized sum of squared differences. but this gives the same weight to any mismatched pixel. We would like to weigh heavier the areas closer to the pixel
- Therefore we apply a gaussian kernel $$G x d_{SSD}$$
#  Synthesizing texture
- Considering joint probabilities of pixels is intractable for large images
- Use a Shannon-inspired heuristic where the texture is grown in layers outwards from a 3x3 seed taken randomly from $$I_{smp}$$
- For any point $$p$$ to be synthesized, only some of the pixel values in $$w(p)$$ need to be known.
- Match known values in $$w(p)$$ and normalize the error by the total number of known pixels when computing the conditional pdf for $$p$$. Does not guarantee that the pdf for p will stay valid, but seems to be a good approximation in practice.
#  Results
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2F_vdBlvH9ei.png?alt=media&token=71b4bd5f-66e8-4d17-8272-688f3b8e6431)
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2F2laNtNY7wJ.png?alt=media&token=9fb364e7-a574-45b8-b615-c90808882a7d)
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FZRcbYhm0eL.png?alt=media&token=cb786bc2-f8db-4fda-93d8-fcca754dccbd) 
[[Image Inpainting]]
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2Fo3MAnejtH6.png?alt=media&token=548712cc-d470-4f4c-8bfc-da35edf8bb97)
Failure Cases
- Tendency to slip into a wrong part of the search space and start growing garbage, or get locked onto one place and produce verbatim copies of the original
    - Happens when texture sample contains too many different types of texels or same texels with different illumination.
   - Can be alleviated by using a bigger sample image.
# Learning Gaps/Thoughts
# Simplify/Analogies
