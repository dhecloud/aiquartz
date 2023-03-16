### [[Graph-to-Sequence Neural Machine Translation]]
![[Pasted image 20210104233240.png]]
There are three levels for the subgraph order
1. High order, which uses [[Multi-Head Self-Attention]]
2. Middle order, which uses two groups of [[Multi-Head Self-Attention]]
3. Low order, which does not contain any [[Multi-Head Self-Attention]], and uses a [[Feed-forward]] layer instead.

After which, weights are learnt via gating mechanism to weigh different groups and merge them:
$$w = \text{Sigmoid}(i_h, + i_m + i_l)$$$$r_f = (i_h + i_m)w + i_l(1-w)$$
However, there is no inherent mechanism that will make the model think that "high order" graphs are "high" and not "low" or "middle" and vice versa.