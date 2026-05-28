<div align="center">
  <h1 align="center">LoMo: Local Modality Substitution for Deeper Vision-Language Fusion</h1>

  <p>
    Feng Han<sup>1,2</sup>, Zhixiong Zhang<sup>2,3</sup>, Zheming Liang<sup>2,4</sup>, Yibin Wang<sup>1,2</sup>, Jiaqi Wang<sup>2,5,*</sup>
  </p>

  <p>
    <sup>1</sup>Fudan University, <sup>2</sup>Shanghai Innovation Institute, <sup>3</sup>Shanghai Jiao Tong University<br>
    <sup>4</sup>University of Science and Technology of China, <sup>5</sup>JD.COM
  </p>

  <p>
    <a href="./LoMo-Technical-Report.pdf"><img src="https://img.shields.io/badge/Paper-PDF-blue" alt="Paper PDF"></a>
    <a href="https://maplebb.github.io/LoMo/"><img src="https://img.shields.io/badge/Website-project%20page-orange" alt="Project Page"></a>
    <a href="https://huggingface.co/maplebb/LoMo-Checkpoints"><img src="https://img.shields.io/badge/%F0%9F%A4%97%20Hugging%20Face-Checkpoints-yellow" alt="Checkpoints"></a>
  </p>
</div>

## 🔥 News

- [2026/05/29] 🔥🔥 We release the technical report, project page, and checkpoints for **LoMo**.

## 🌱 Introduction

Vision-Language Models still show **carrier sensitivity**: changing a textual question into a rendered-image question can sharply reduce accuracy even when the semantics stay unchanged. **LoMo** addresses this gap by locally replacing part of a single-modal prompt with its rendered visual counterpart, encouraging VLMs to fuse equivalent information across text and image carriers.

<p align="center">
  <img src="page/static/images/fig_carrier_sensitivity.png" alt="Carrier sensitivity and cross-modal alignment" width="900">
</p>
<p align="center"><em>Rendered questions reduce accuracy. Larger representation gaps cause larger drops. LoMo pulls equivalent text/image carriers closer.</em></p>

### ✨ Highlights:

LoMo is a lightweight, architecture-agnostic data curation recipe for standard SFT. It localizes a coherent text span, renders it as an image, and substitutes it back into the original context to form a `text -> visual carrier -> text` sequence. This local substitution requires no additional annotations, architectural changes, or inference-time overhead, and can be plugged into existing multimodal SFT pipelines.

<p align="center">
  <img src="page/static/images/fig_lomo_overview.png" alt="LoMo overview" width="900">
</p>

<p align="center">
  <img src="page/static/images/fig_benchmark_gains.png" alt="Benchmark gains across two backbones" width="900">
</p>

## ✨ Evaluation

We run inference with the [Hugging Face backend](https://github.com/huggingface/transformers) for LLaVA-OneVision-1.5 and [vLLM](https://github.com/vllm-project/vllm) for Qwen3.5.
We use [ModelScope](https://github.com/modelscope/evalscope) as the evaluation framework.

## 👨‍💻 Todo

- [ ] Release the LoMo data construction code
- [ ] Release the training and evaluation scripts
- [x] Release the LoMo checkpoints

## 📧 Contact

For questions or suggestions, please open an issue in this repository.

## ⭐ Citation

```bibtex

```
