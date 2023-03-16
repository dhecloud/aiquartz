Author(s): [[Laurens van der Maaten]], [[Geoffrey Hinton]]
Tags: #Machine_Learning, #academic_papers
Read on: [[July 6th, 2020]]
URL: http://www.cs.toronto.edu/~hinton/absps/tsne.pdf
# Main Contribution(s)
- Present a technique called [[t-SNE]] which visualizes high dimensional data in a 2 or 3 dimensional map
# Summary
- [[t-SNE]] allows for an more accurate 2/3-dimensional mapping  
# Learning Gaps
#  [[SNE]]
- Converts high dimensional Euclidean distance between datapoints into conditional probabilities that represent similarities.
- For nearby data points, $$p_{j|i}$$ is relatively high, and for widely separated data points, $$p_{j|i}$$ is almost infinitesimal (extremely small)
- There is a large cost for using widely separated map points to represent nearby data points (using small $$q_{j|i}$$ to model large $$p_{j|i}$$), but only a small cost for using nearby map points to represent widely separated data points
- Cost function is difficult to optimize
- [[Crowding Problem]]
- It is possible to have points that are mutually equidistant and this results in an incapability to model these points accurately in a two-dimensional map
- The area needed to accommodate moderately distant data points will not nearly be large enough compared with the area available to accommodate nearby data points
- Some algorithms like [[UNI-SNE]] try to solve this by adding a slight repulsion
#  [[t-SNE]]
- Uses a Student t-distribution rather than a Gaussian to compute the similarity between two points in the low dimensional space.
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FOXHh4GbuUT.png?alt=media&token=51cc11a8-5d92-4f8b-ab34-eb21dc9efa0d)
- t-SNE gradients strongly repels dissimilar points (gradients << -1)
- These repulsions do not go to infinity 
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FDj2MamPzMg.png?alt=media&token=dfecb380-25cd-4e9c-851e-bb15ec8c50e5)
# # [[t-SNE]] Weaknesses:
    - Unclear how it performs on general dimension reduction to $$d>3$$
    - **Curse of intrinsic dimensionality** - Might be less successful if it is applied on data sets with a very high intrinsic dimensionality (like images of face can be ~100d)
    -  **Non-convexity of the t-SNE cost function** - requires hyper parameter optimization
#  [[Isomap]] weaknesses:
- Susceptibility to short-circuiting
- Focuses on large geodesic distances rather than small ones
#  [[LLE]] weaknesses:
- The only thing that prevents all datapoint from collapsing onto a single point is a constraint on the covariance of the low-dimensional representation 
# Simplify/Analogies
- By using a t-distribution with standard SNE, we can better model high dimensional data using low 2-3 dimensional distributions 
