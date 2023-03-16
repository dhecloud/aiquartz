Author(s): [[Matthew A. Turk]], [[Alex P. Pentland]]
Tags: #Face_Recognition, #Computer_Vision, #academic_papers
Read on: [[September 25th, 2020]]
URL: https://ieeexplore.ieee.org/document/139758
# Main Contribution(s)
- Use [[Eigenvector]]s of face images to perform classification
# Summary
- Decompose  the training set into its set of [[Eigenvalue]]s which are termed eigenfaces here. This is the face space
- To perform inference on new image,
- calculate a set of weights based on the input image and the M eigenfaces by projecting the input image onto each of the eigenfaces.
- Determine if image is a face by checking if the image is close enough to the face space using the [[Euclidean Distance]]/Distance
- If it is a face, classify the weight pattern.
- If a face is unknown and seen several time, calculate its characteristic weight pattern and incorporate into the known faces.
- Of 2500 images, 96% correct classification averaged over lighting variation, 85% correct averaged over orientation variation, and 64% correct averaged over size variation.
- Does not work well for other views (non-frontal)
# Learning Gaps/Thoughts
-
# Simplify/Analogies
- classical machine learning on computer visions
