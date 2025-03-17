---
title: Automatic Active Lesion Tracking in Multiple Sclerosis Using Unsupervised Machine Learning
author: Jason Uwaeze
tags:
  - Diagnositic Imaging
  - Unsupervised Learning
  - Multiple Sclerosis
  - Brain MRI
---

This study uses Non-linear Dimensionality Reduction (NLDR) techniques to identify active lesions in magnetic resonance imaging (MRI). We applied Locally Linear Embedding (LLE) and Isometric Feature Mapping (Isomap) to MRI data from 40 multiple sclerosis patients, achieving median Dice scores of 0.74 and 0.78 for active lesion segmentation, respectively.

{%
  include figure.html
  image="images/ADFLL_Concept_Figure.png"
  caption="Illustration of asynchronous decentralized federated lifelong learning (ADFLL)
  set up for cross-modality 3D localization of spleen. The blue, orange, and green
  boxes represent different agents in the setup. Each agent sequentially encounters
  two different imaging modalities for along with experiences shared by the other
  nodes, enabling them to learn to localize the spleen across all four modalities (as
  opposed to just the two they encountered)."
  width="1000px"
%}


To further enhance the efficiency of the ADFLL framework, we integrate a reward distribution-preserving coreset compression technique for selective experience replay buffers. This method compresses stored experiences, reducing computational overhead while maintaining the model’s ability to mitigate catastrophic forgetting. Evaluated on tasks such as ventricle localization in the BRATS dataset and landmark localization in whole-body MRI, the compressed lifelong learning models demonstrated competitive performance with minimal impact on accuracy. For instance, the 10x compressed models achieved mean pixel distances close to conventional lifelong learning models, highlighting the viability of coreset compression in resource-constrained settings. This addition reinforces ADFLL’s scalability and adaptability to real-world applications. Paper published in *Medical Imaging with Deep Learning* (MIDL) 2023, [Selective experience replay compression using coresets for lifelong deep reinforcement learning in medical imaging](https://proceedings.mlr.press/v227/zheng24a.html).

To further address the challenges of deploying the ADFLL framework on low-compute edge devices in rapidly evolving imaging environments, we developed three image coreset algorithms for compressing and denoising medical images in selective experience replay. These include neighborhood averaging, neighborhood sensitivity-based sampling, and maximum entropy coresets, which achieve 27x compression while maintaining strong performance in localizing anatomical landmarks on DIXON water and fat MRI images. Notably, the maximum entropy coreset outperformed conventional lifelong learning models with an average distance error of 11.97±12.02 compared to 19.24±50.77, showcasing its potential to enhance efficiency and adaptability in real-world medical imaging applications. Paper on arXiv: [A framework for dynamically training and adapting deep reinforcement learning models to different, low-compute, and continuously changing radiology deployment environments](https://arxiv.org/abs/2306.05310).

This project is funded by DARPA, part of the Shared Experience Lifelong Learning ([ShELL](https://intelligencecommunitynews.com/darpa-launches-shell-program/)) program. Collectively, we have published a paper on *Nature Machine Intelligence*, [A collective AI via lifelong learning and sharing at the edge](https://rdcu.be/dB9zt).
