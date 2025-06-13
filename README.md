<div align="center">
<h1><img src="assets/multiverse-logo.png" height="40px" align="top"/> Multiverse
</h1>


Xinyu Yang<sup>1\*</sup>, Yuwei An<sup>1\*</sup>, Hongyi Liu<sup>1</sup>, Tianqi Chen<sup>1,2</sup>, Beidi Chen<sup>1</sup>

Carnegie Mellon University<sup>1</sup>, Nvidia<sup>2</sup>

-----------------
</div>

<div align="center">
[<a href="https://arxiv.org/abs/2506.09991">Paper</a>] | [<a href="https://multiverse4fm.github.io/">Blog</a>]
</div>
<br>

<!-- ## TL;DR

--- -->

## 🎬 Demo

The following demo showcases a Multiverse model solving a reasoning problem. Observe how the model first **maps** the problem to a structured plan, then **processes** the sub-tasks in parallel (the "split" phase), and finally **reduces** the parallel results into a coherent final answer (the "merge" phase).

This demonstrates the core MapReduce paradigm of the Multiverse model in action.


![Demo of Multiverse reasoning inference](assets/demo.gif)

## 🏛️ Repository Structure

This repository provides the complete, end-to-end workflow for the **Multiverse model**. Our structure is organized as a sequential pipeline to guide you through every step:

**🗂️ `data`** → **📈 `train`** → **🚀 `inference`**

Each of these core directories represents a key stage in the machine learning lifecycle and contains its own detailed `README.md` with further instructions.

```
Multiverse
├── data/
│   └── src
|   └── run
|   └── README.md
│
├── train
│   └── README.md
│
├── inference/
│   └── engine
|   └── eval
|   └── README.md
│
└── README.md
```
- **`data/`**: Contains all scripts and tools for data processing, including the code to generate our **Multiverse-1K** dataset. This involves an LLM-assisted pipeline that converts standard sequential reasoning datasets into the structured, parallel format required for training.

- **`training/`**: Contains the code for fine-tuning a base Large Language Model into a Multiverse model. This directory implements the **Multiverse Attention** algorithm, enabling the model to learn how to split, process, and merge tasks.

- **`inference/`**: Contains the **Multiverse Engine**, a high-performance inference server based on SGLang. It features a dedicated scheduler that dynamically switches between sequential and parallel generation, allowing for the significant speedups demonstrated in our paper. Despite the engine, we also import the lighteval code for evaluation.

<!-- ## 📝 Todo List


- [ ] Release Multiverse
- [ ] f -->

## 📜 Citation

If you find our work useful for your research, please consider citing our papers.

```bibtex
@article{multiverse2025,
      title={Multiverse: Your Language Models Secretly Decide How to Parallelize and Merge Generation}, 
      author={First Author and Second Author and Other Authors},
      year={2025},
      journal={arXiv preprint arXiv:XXXX.XXXXX}
}
```