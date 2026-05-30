# Reasoning Scaling Law
Simplified implementation for ICML 2026 paper **"Finding the Minimal Parameter Budget for Implicit Reasoning: A Data Complexity Driven Scaling Law for Language Models"** ([paper](https://openreview.net/forum?id=iuIPAhZpxz)).


## Abstract

Reasoning is a core capability of language models (LMs), yet it remains unclear how much model capacity is necessary to support reasoning during pretraining. In this work, we study the minimal parameter budget required for implicit reasoning, defined as the ability to infer new facts from learned knowledge without explicit chain-of-thought supervision. To isolate this phenomenon, we pretrain LMs from scratch in a controlled synthetic environment that mimics the structure and distribution of real-world knowledge graphs, and evaluate their ability to complete missing edges via multi-hop inference. From both a theoretical and an empirical perspective, we identify a scaling law linking this optimal parameter budget to a graph search entropy measure. Across a wide range of model sizes, training steps, and graph complexities, we show that an optimally sized language model can reliably reason over approximately 0.008 bits of information per parameter at most. Our results characterize the minimal sufficient capacity for implicit reasoning during pretraining. Our findings provide principled guidance for matching model size to data complexity and offer new insights into the scaling behavior of reasoning in large language models.

## Notebook

This interactive notebook provide basic/most important code for generating synthetic graphs,
and training and evaluating language model on the generated graph. It should be 
runable directly on Colab without GPUs, except the final sweeping function for 
ploting the reasoning scaling law. This part requires training much larger language
models thus would require GPUs.

You can modify the code to suit your large scale experiment settings.

## Citation

```bibtex
@inproceedings{wang2025larger,
title={Finding the Minimal Parameter Budget for Implicit Reasoning: A Data Complexity Driven Scaling Law for Language Models},
author={Wang, Xinyi and Tan, Shawn and Xu, Shenbo and Jin, Mingyu and Wang, William Yang and Panda, Rameswar and Shen, Yikang},
booktitle={Forty-third International Conference on Machine Learning},
year={2026},
url={https://openreview.net/forum?id=iuIPAhZpxz}
}
```
