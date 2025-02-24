---
title: Exploring Uncertainty-Based On-device LLM Routing From Benchmarking to Generalization
author: Yu-Neng (Allen) Chuang
tags:
  - On-device LLM Routing
  - Uncertainty Quantification
  - Efficient LLM Inference
  - wearable-device
---

Large language models (LLMs) are increasingly deployed and democratized on edge devices. To improve the efficiency of on-device deployment, small language models (SLMs) are often adopted due to their efficient decoding latency and reduced energy consumption. However, these SLMs often generate inaccurate responses when handling complex queries. One promising solution is uncertainty-based SLM routing, offloading high-stakes queries to stronger LLMs when resulting in low-confidence responses on SLM. This follows the principle of "If you lack confidence, seek stronger support" to enhance reliability. Relying on more powerful LLMs is yet effective but increases invocation costs. Therefore, striking a routing balance between efficiency and efficacy remains a critical challenge. Additionally, efficiently generalizing the routing strategy to new datasets remains under-explored. In this paper, we conduct a comprehensive investigation into benchmarking and generalization of uncertainty-driven routing strategies from SLMs to LLMs over 1500+ settings. 

:books: This work offers an accessible and reproducible pipeline for uncertainty-based routing from benchmarking to generalization. Our main contributions are summarized as follows:
- **Comprehensive benchmarking and detailed analysis:** This benchmark evaluates $8$ UQ methods across $14$ datasets to examine the alignment between uncertainty and correctness in routing tasks. We incorporate $8$ SLMs and $2$ LLMs to emulate real-world deployment scenarios. We then delve into key observations from the extensive results and conclude the insights for developing uncertainty-based SLM routing.
- **Calibration data for generalization to new data:** Building on our benchmarking pipeline, we introduce a calibration data construction pipeline designed to improve routing generalization in new downstream scenarios. Empirical results show that this calibration data generalizes effectively to new datasets \textit{without relying on any new downstream data}.

:books: Please check our full version paper: https://arxiv.org/pdf/2502.04428

:star2: Please check our source code in our Github repo: https://github.com/ThunderbornSakana/quodlibeta