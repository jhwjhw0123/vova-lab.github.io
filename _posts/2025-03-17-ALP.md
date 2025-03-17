---
title: Automatic Active Lesion Tracking in Multiple Sclerosis Using Unsupervised Machine Learning
author: Jason Uwaeze
tags:
  - Diagnositic Imaging
  - Unsupervised Learning
  - Multiple Sclerosis
  - Brain MRI
---

This study uses Non-linear Dimensionality Reduction (NLDR) techniques to identify active lesions in magnetic resonance imaging (MRI). We applied Locally Linear Embedding (LLE) and Isometric Feature Mapping (Isomap) to MRI data from 40 multiple sclerosis patients, achieving median Dice scores of 0.74 and 0.78 for active lesion segmentation, respectively [[Paper](https://www.mdpi.com/2075-4418/14/6/632)][[Code](https://github.com/Wazhee/Automatic-Multiple-Sclerosis-Lesion-Tracking)].

{%
  include figure.html
  image="images/active_lesion_tracking.png"
  caption="The Isomap algorithm can be summarized in four steps: (1) select a nearest neighbor algorithm, 
  (2) calculate geodesic distances for all data points (3) apply multidimensional scaling to geodesic distance matrix, 
  (4) output single embedded image."
  width="1000px"
%}

The objective of this study was to demonstrate that unsupervised NLDR methods outperform supervised machine learning methods in identifying active lesions. To accomplish this, we introduce key differences between LDR and NLDR. Subsequently, we establish the motivation behind applying NLDR to brain MRI data. Then, we provide details for the MR imaging dataset and performance evaluation metrics used in this work. Furthermore, we compare NLDR methods to current state-of-the-art methods for active MS lesion identification. Lastly, we discuss the potential limitations of this work. Paper published in *Multidisciplinary Digital Publishing Institute* (MDPI) 2024, [Automatic Active Lesion Tracking in Multiple Sclerosis Using Unsupervised Machine Learning](https://www.mdpi.com/2075-4418/14/6/632).

This project is funded by the Defense Advanced Research Projects Agency [[DARPA](https://intelligencecommunitynews.com/darpa-launches-shell-program/)], Navy, the National GEM consortium [[DARPA](https://www.gemfellowship.org/)] and University of Texas Health Science Center Houston, UT-Health Endowed Chair in Biomedical Engineering for Michael A. Jacobs, PhD.

