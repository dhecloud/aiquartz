---
aliases: [MaMa]
---

# [[LANGUAGE MODELS ARE OPEN KNOWLEDGE GRAPHS]]
![[Pasted image 20201221225601.png]]!Consists of two stages:
1. **Match**: Generates a set of candidate facts from a textual corpus. Each fact is represented as a triplet (head, relation, tail)
2. **Map**: ![[Pasted image 20201221225611.png]] produces [[Knowledge Graphs]], which is either following a fixed schema, like from the [[Wikidata]], or an open schema. This is done via a searching problem like [[Beam Search]]

Some constraints are introduced to the beam search to achieve a better search quality
1. Matching degree of $(h,r,t)$ is above a threshold
2. Distinct frequency of $r$ is above a threshold
3. Realtion $r$ is a contiguous sequence in the sentence.
