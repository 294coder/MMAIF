<h1 style="text-align: center;">MMAIF: Multi-task and Multi-degradation All-in-One for Image Fusion with Language Guidance</h1>




<div align="center">
  <a href=https://scholar.google.com/citations?user=pv61p_EAAAAJ&hl=en>Zihan Cao </a> |
  <a href=https://scholar.google.co.il/citations?user=UgD8AtkAAAAJ&hl=de> Yu Zhong </a> |
  <a href=https://scholar.google.de/citations?user=3mgKMScAAAAJ&hl=zh-CN> Ziqi Wang </a> |
  <a href=https://scholar.google.com/citations?user=TZs9NxkAAAAJ&hl=zh-CN> Liang-Jian Deng </>
  
  <a>University of Science and Technology of China (UESTC)</a>
</div>


paper: [![arXiv](https://img.shields.io/badge/arXiv-2503.14944-b31b1b.svg)](https://arxiv.org/abs/2503.14944)


# Quick Introduction

<div style="text-align: center;">
  <img src="assets/teaser.png" title="MMAIF Framework Overview" style="width: 400px; height: auto;" />
  <p>Fig 1: MMAIF framework overview.</p>
</div>




<div>
<strong>Abstract</strong>:
Image fusion, a fundamental low-level vision task, aims to integrate multiple image sequences into a single output while preserving as much information as possible from the input. However, existing methods face several significant limitations: 1) requiring task- or dataset-specific models; 1) neglecting real-world image degradations (e.g., noise),
which causes failure when processing degraded inputs; 3) operating in pixel space, where attention mechanisms are computationally expensive; and 4) lacking user interaction capabilities. To address these challenges, we propose a unified framework for multi-task, multi-degradation, and language-guided image fusion. Our framework includes two key components: 1) a practical degradation pipeline that simulates real-world image degradations and generates interactive prompts to guide the model; 2) an all-in-one Diffusion Transformer (DiT) operating in latent space, which fuses a clean image conditioned on both the degraded inputs and the generated prompts. Furthermore, we introduce principled modifications to the original DiT architecture to better suit the fusion task. Based on this framework, we develop two versions of the model: Regression-based and Flow Matching-based variants. Extensive qualitative and quantitative experiments demonstrate that our approach effectively addresses the aforementioned limitations and outperforms previous restoration+fusion and all-in-one pipelines.
</div>

We provide a effecient data synthesis pipeline to generate degradation pairs.

<div style="text-align: center;">
<figure style="text-align: center;">
<img src="assets/data-pipeline.png" title="Data Synthesis Pipeline Overview" style="width: 800px; height: auto;" />
<p>Fig. 2: Data synthetic pipeline overview.</p>
</figure>
</div>

<a> 

</a>


Based on the pipeline, we generate around 10k image pairs for training, including various degradation scenarios including *rain, snow, haze, motion blur, JPEG compression, and Gaussian noise, etc.*, as well as, commom image fusion tasks including multi-exposure, multi-focus, and visible-infrared image fusion.

We train two versions of models:
- Regression-based model
- Flow matching model

with **MoE** architecture and work in latent space,
which is *fast and efficient*.

Our model can suit for multiple image fusion tasks and different degradations, **only in one model**.

<div style="text-align: center;">
<figure style="text-align: center;">
<img src="assets/networks.png" title="Model comparision overview" style="width: 900px; height: auto;" />
<p>Fig. 3: Model comparision overview.</p>
</figure>
</div>

Here are some visual results of our model and restoration+fusion methods.

<div style="text-align: center;">
<figure style="text-align: center;">
<img src="assets/teaser2.png" title="Visual Comparisons" style="width: 900px; height: auto;" />
<p>Fig. 4: Visual comparisons.</p>
</figure>
</div>

## Code Will be Released Soon! Stay Tuned for Updates.
