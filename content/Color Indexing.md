Author(s): [[Michael J. Swain]], [[Dana H. Ballard]]
Tags: #Computer_Vision, #academic_papers
Read on: [[September 25th, 2020]]
URL: http://www.inf.ed.ac.uk/teaching/courses/av/LECTURE_NOTES/swainballard91.pdf
# Main Contribution(s)
- Proposes [[Histogram Intersection]], [[Histogram Backprojection]] to develop visual skills for robots
# Summary
#  [[Histogram Intersection]]
- $$\sum\limits_{j=1}^{n} min(I_j, M_j)$$ where I and M are a pair of histograms containing n bins
- Able to deal with: 
            1. distractions in the background of the object
            2. viewing the object from a variety of viewpoints
            3. occlusion
            4. varying image resolution
- an extra color constancy module is used to deal with varying lighting conditions.
- [[Incremental Intersection]] is an extension to index into a large database. Only the largest bins from the image and model histograms are compared, and a partial histogram intersection value is computed.
- Off-line phrase
    - 1. Assign to each bin in each model histogram a key which is the fraction of the total number of pixels in the histogram that fall in that bin
2. Group the bins by index (color). Average
3. Sort each group by key.
- Online phrase
    - 1. Sort the image histogram bins by size.
2. For the B largest image bins, starting with the largest, match the image bin to all the model bins with the same index whose key is larger. If previously unmatched model bins are matched, match them to all larger image bins.
#  [[Histogram Backprojection]]
- A ratio histogram $$R$$ is defined as $$min(\frac{M_i}{I_i}, I)$$ is used to replace values in an image.
- Sensitive to failure of color constancy
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FHa8H7mWoj0.png?alt=media&token=1438fb60-c980-49c2-8293-530da421e6cd)
# Learning Gaps/Thoughts
# Simplify/Analogies
