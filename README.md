<div align="center">
<h1><img src="assets/multiverse-logo.png" height="40px" align="top"/> Multiverse
</h1>


Xinyu Yang<sup>1\*</sup>, Yuwei An<sup>1\*</sup>, Hongyi Liu<sup>1</sup>, Tianqi Chen<sup>1,2</sup>, Beidi Chen<sup>1</sup>

Carnegie Mellon University<sup>1</sup>, Nvidia<sup>2</sup>

-----------------
</div>

<div align="center">
[<a href="https://arxiv.org/abs/2506.05333">Paper</a>] | [<a href="https://infini-ai-lab.github.io/Kinetics/">Blog</a>]
</div>
<br>

## TL;DR
<!-- TODO: ADD TL:DR -->
---

## 🎬 Demo

The following demo showcases a Multiverse model solving a reasoning problem. Observe how the model first **maps** the problem to a structured plan, then **processes** the sub-tasks in parallel (the "split" phase), and finally **reduces** the parallel results into a coherent final answer (the "merge" phase).

This demonstrates the core MapReduce paradigm of the Multiverse model in action.


<div align="center">
  <video controls src="assets/demo.mp4" width="80%">
  </video>
</div>

## 🏛️ Repository Structure

The repository is organized as follows. Each of the core directories (`data`, `train`, `inference`) contains a detailed `README.md` with further instructions.

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

- **`inference/`**: Contains the **Multiverse Engine**, a high-performance inference server based on SGLang. It features a dedicated scheduler that dynamically switches between sequential and parallel generation, allowing for the significant speedups demonstrated in our paper.

## 📝 Todo List


- [ ] Release Multiverse

## 📜 Citation

If you find our work useful for your research, please consider citing our papers.

```bibtex
@article{multiverse2025,
      title={Multiverse: Your Language Models Secretly Decide How to Parallelize and Merge Generation}, 
      author={First Author and Second Author and Other Authors},
      year={2025},
      journal={arXiv preprint arXiv:XXXX.XXXXX}
}