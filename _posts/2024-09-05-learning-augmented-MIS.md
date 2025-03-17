---
title: Learning-augmented Maximum Independent Set
author: Chen Wang
tags:
  - Foundations of Machine Learning
  - Algorithm Design
  - Graph Mining
  - Theoretical Machine Learning
  - Beyong Worst-case Analysis
---

We investigated algorithms for the Maximum Independent Set (MIS) problem in the presence of a learning-augmented *membership* oracle. 
Given a graph $G=(V,E)$, the Maximum Independent Set asks to find the maximum subset of vertices $I^\star \subseteq V$ such that for any pair of vertice $u,v \in I^\star$, $(u,v)\not\in E$, i.e., they are not neighbors.
It is known that the MIS problem is NP-hard and it is NP-hard to approximation for a factor of $n^{1-\delta}$ for any constant $\delta>0$.

In the context of modern machine learning applications, we asked whether the computational complexity barrier could be overcome with the presence of a learning-augmented *membership* oracle. 
Let $I^\star$ be a fixed maximum independent set, a membership oracle $\mathcal{O}$ returns whether a vertex $v \in I^\star$ upon a query on $v$. 
In the context of learning-augmented algorithms, the oracle $\mathcal{O}$ returns the correct answer with probability $\frac{1}{2}+\Omega(1)$ and returns an *arbitrary* (potentially adversarial) answer with probability $\frac{1}{2}-\Omega(1)$.
These assumptions capture the power (e.g., accuracy) and limitations (e.g., adversarial behavior during failure) of modern ML algorithms.

Our main results include:
- For the *persistent noise* setting, where the randomness is drawn exactly once, we obtain an algorithm that achieves $O(\sqrt{\Delta})$ approximation for MIS in O(m) time, where $m$ is the number of edges in the graph. Here, $\Delta$ is the *maximum degree* of the input graph $G$.
- For the *none-persistent noise* setting, where we could query the same vertex $v$ multiple times using fresh randomness, we obtain an algorithm that achieves $O(1)$-approximation for MIS in $O(m \log{n})$ time and $O(n)$ *total* queries.

These results are in contrast with the strong negative results in the classical setting, which shows the power of machine learning-based models in algorithm design.

The research was partially by the Naval Research (ONR) grant N00014-23-1-2737 and NSF-CNS 2333887 award. The paper was published at the 2024 International Conference on Approximation Algorithms for Combinatorial Optimization Problems (APPROX 2024).
Arxiv link: https://arxiv.org/abs/2407.11364.
