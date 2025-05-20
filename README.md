# MVAR: Visual Autoregressive Modeling with Scale and Spatial Markovian Conditioning
code is coming soon...
> Essential to visual generation is efficient modeling of visual data priors.
Conventional next-token prediction methods define the process as learning the conditional probability distribution of successive tokens.
Recently, next-scale prediction methods redefine the process to learn the distribution over multi-scale representations, significantly reducing generation latency.
However, these methods condition each scale on all previous scales and require each token to consider all preceding tokens, exhibiting scale and spatial redundancy.
To better model the distribution by mitigating redundancy, we propose Markovian Visual AutoRegressive modeling (MVAR), a novel autoregressive framework that introduces scale and spatial Markov assumptions to reduce the complexity of conditional probability modeling.
Specifically, we introduce a scale-Markov trajectory that only takes as input the features of adjacent preceding scale for next-scale prediction, enabling the adoption of a parallel training strategy that significantly reduces GPU memory consumption.
Furthermore, we propose spatial-Markov attention, which restricts the attention of each token to a localized neighborhood of size k at corresponding positions on adjacent scales, 
rather than attending to every token across these scales, for the pursuit of reduced modeling complexity.
Building on these improvements, we reduce the computational complexity of attention calculation from O(N^2) to O(Nk), enabling training with just eight NVIDIA RTX 4090 GPUs and eliminating the need for KV cache during inference.
Extensive experiments on ImageNet demonstrate that MVAR achieves comparable or superior performance with both small model trained from scratch and large fine-tuned models, while reducing the average GPU memory footprint by 3.0x.

---

[MVAR: Visual Autoregressive Modeling with Scale and Spatial Markovian Conditioning](https://arxiv.org/abs/2505.12742)  

[Jinhua Zhang](https://scholar.google.com/citations?user=tyYxiXoAAAAJ),  [Wei Long](https://scholar.google.com/citations?user=CsVTBJoAAAAJ),  [Minghao Han](),  [Weiyi You](https://scholar.google.com/citations?user=q4uALoAAAAAJ),  [Shuhang Gu](https://scholar.google.com/citations?user=-kSTt40AAAAJ)

[![arXiv](https://img.shields.io/badge/arXiv-2505.12742-b31b1b.svg)](https://arxiv.org/abs/2505.12742)
[![GitHub Stars](https://img.shields.io/github/stars/LabShuHangGU/MVAR?style=social)](https://github.com/LabShuHangGU/MVAR)

 

