# Reasoning Scaling Law
Implementation for **"Do Larger Language Models Generalize Better? A Scaling Law for Implicit Reasoning at Pretraining Time"** ([paper](https://arxiv.org/abs/2504.03635)).


## Abstract

Reasoning is an integral part of many tasks performed by language models (LMs). However, the effects of scaling model sizes and data on reasoning abilities at pretraining time remain understudied. To rigorously investigate this problem, we pretrain LMs from scratch on a synthetic implicit multihop reasoning environment designed to closely replicate the structure and distribution of real-world large-scale knowledge graphs. We then assess the LMs' ability to complete the missing edges in the graph, which requires multi-hop reasoning that can be viewed as a simplification of implicit reasoning during real-world pretraining. Interestingly, we observe that overparameterization can impair the implicit reasoning performance due to excessive memorization. We investigate different factors that affect the loss curve when scaling different components of the knowledge graph, model size, and training steps. To predict the optimal model size for a specific knowledge graph, we find an empirical scaling law that shows optimal-sized LMs can approximately reason over 0.008 bit information per parameter. This work shows counterintuitive effects of model size scaling and provides new insights into the relationship between scaling and reasoning in LLMs.

## Notebook

This interactive notebook provide basic/most important code for generating synthetic graphs,
and training and evaluating language model on the generated graph. It should be 
runable directly on Colab without GPUs, except the final sweeping function for 
ploting the reasoning scaling law. This part requires training much larger language
models thus would require GPUs.

You can modify the code to suit your large scale experiment settings.

## Citation

```bibtex
@article{wang2025larger,
  title={Do larger language models imply better reasoning? a pretraining scaling law for reasoning},
  author={Wang, Xinyi and Tan, Shawn and Jin, Mingyu and Wang, William Yang and Panda, Rameswar and Shen, Yikang},
  journal={arXiv preprint arXiv:2504.03635},
  year={2025}
}
```
