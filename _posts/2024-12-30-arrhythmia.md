---
title: Arrhythmia Detection and ECG Explainability
author: Guangyao Zheng
tags:
  - Personalized Healthcare
  - Multi-label Classification
  - Wearable Device
  - Cardiovascular Health
  - Explainability
  - Interpretability

---

This project addresses the critical challenges of arrhythmia detection and classification, particularly in the context of wearable electrocardiogram (ECG) monitoring devices. Unlike clinically controlled environments, wearable devices operate in noisy, real-world conditions, which complicates the accurate identification of arrhythmias. Additionally, the inherent imbalance in the ratio of normal heartbeats to arrhythmic ones, along with the diverse combinations of arrhythmia types, further compounds the difficulty of the task.

To tackle these challenges, we developed a novel hierarchical deep learning model that combines Convolutional Neural Networks (CNN), Bidirectional Long Short-Term Memory networks (BiLSTM), and an Attention mechanism. Our framework consists of two key modules:

1. A binary classification module to distinguish normal heartbeats from arrhythmic ones.
2. A multi-label classification module to categorize arrhythmia events across combinations of beat and rhythm types.
The model was trained and evaluated on a proprietary dataset, achieving state-of-the-art performance metrics:

*Binary Classification: Accuracy: 95%, F1-score: 0.838, AUC: 0.906.
*Multi-label Classification: Accuracy: 88%, F1-score: 0.736, AUC: 0.875.
We benchmarked our framework against strong baselines, including CNN+BiGRU with Attention, ConViT, EfficientNet, and ResNet, as well as previous state-of-the-art methods, demonstrating its superior performance.

Our model offers a promising solution for real-world arrhythmia detection and classification, providing:

*Enhanced diagnostic efficiency by reducing the workload on cardiologists.
*Personalized treatment options by enabling accurate, continuous monitoring.
*Emergency intervention capabilities through real-time arrhythmia monitoring on wearable devices.
This framework has the potential to revolutionize arrhythmia management, improving patient outcomes and advancing the integration of AI in healthcare. Paper published in *Digital Health*: [Hierarchical Deep Learning for Autonomous Multi-label Arrhythmia Detection and Classification on Real-world Wearable ECG Data](https://journals.sagepub.com/doi/full/10.1177/20552076241278942)


Additionally, the lack of transparent justifications for decisions made by deep learning models poses challenges for real-world applications.

In this project, we utilized signals from a portable single-lead ECG device to classify eight arrhythmia classes using convolutional neural networks (CNN), achieving 79.91% accuracy on a single heartbeat. To enhance model interpretability, we incorporated Layer-Wise Relevance Propagation (LRP), an explainable artificial intelligence (XAI) algorithm, to analyze the distinctive features of each arrhythmia.

The XAI analysis revealed that for ventricular premature contraction (VPC), the model demonstrated strong activations in the QRS complex and T-wave regions. This aligns with medical interpretations that a wide QRS complex and an oppositely directed T-wave are characteristic of VPC. Such findings emphasize the potential for deep learning models to offer not only accurate predictions but also insights that align with clinical knowledge, supporting biomarker discovery for arrhythmia classification.


This research contributes to interpretable deep learning for arrhythmia diagnosis by:

*Enhancing decision support systems with transparent and interpretable predictions.
*Facilitating biomarker discovery for arrhythmia management.
*Improving trust in AI systems through alignment with clinical knowledge.
These advancements pave the way for more explainable, reliable, and effective deep learning models in healthcare. Paper published in *International Conference on Artificial Intelligence in Medicine* (AIME) 2024: [Exploring the Possibility of Arrhythmia Interpretation of Time Domain ECG Using XAI: A Preliminary Study](https://link.springer.com/chapter/10.1007/978-3-031-66535-6_31)
