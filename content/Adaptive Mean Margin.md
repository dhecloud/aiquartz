### [[Spoken Moments - Learning Joint Audio-Visual Representations from Video Descriptions]]
$$M_{xy} = \alpha(S(x_i,y_i) - \frac{1}{B-1}\sum_{j=1}^B I_{i\neq j}S(x_i,y_j))$$
where $\alpha$ is a dampening parameter to weigh the strength of the margin. In practice 0.5 is used.