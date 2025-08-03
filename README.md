# Reasoning Scaling Law
Implementation for **"Do Larger Language Models Imply Better Generalization? A Pretraining Scaling Law for Implicit Reasoning"** ([paper](https://arxiv.org/abs/2504.03635)).


## Abstract

Large Language Models (LLMs) have demonstrated remarkable capabilities across a wide range of tasks requiring complex reasoning. However, the effects of scaling on their reasoning abilities remain insufficiently understood. In this paper, we introduce a synthetic multihop reasoning environment designed to closely replicate the structure and distribution of real-world large-scale knowledge graphs. Our reasoning task involves completing missing edges in the graph, which requires advanced multi-hop reasoning and mimics real-world reasoning scenarios. To evaluate this, we pretrain language models (LMs) from scratch solely on triples from the incomplete graph and assess their ability to infer the missing edges. Interestingly, we observe that overparameterization can impair reasoning performance due to excessive memorization. We investigate different factors that affect this U-shaped loss curve, including graph structure, model size, and training steps. To predict the optimal model size for a specific knowledge graph, we find an empirical scaling that linearly maps the knowledge graph search entropy to the optimal model size. This work provides new insights into the relationship between scaling and reasoning in LLMs, shedding light on possible ways to optimize their performance for reasoning tasks.


## Notebook

This interactive notebook provide code for generating synthetic graphs,
and training and evaluating language model on the generated graph. It should be 
runable directly on Colab without GPUs, except the final sweeping function for 
ploting the reasoning scaling law. This part requires training much larger language
models thus would require GPUs.

## Citation

```bibtex
@misc{wang2025reasoning,
  title={Do Larger Language Models Imply Better Generalization? A Pretraining Scaling Law for Implicit Reasoning},
  author={Xinyi Wang and Shawn Tan and Mingyu Jin and William Yang Wang and Rameswar Panda and Yikang Sheng},
  year={2025},
  eprint={2504.03635},
  archivePrefix={arXiv},
  primaryClass={cs.AI}
}
```
