# GeoPixel <img src="assets/logo.png" height="50">: Pixel Grounding Large Multimodal Model in Remote Sensing [ICML 2025 🔥]

![](https://i.imgur.com/waxVImv.png)

[Akashah Shabbir](https://github.com/AkashahS) , [Mohammed Zumri](https://github.com/zzumri) , [Mohammed Bennamoun](https://scholar.google.com/citations?user=ylX5MEAAAAAJ&hl=en) , [Fahad Shahbaz Khan](https://scholar.google.es/citations?user=zvaeYnUAAAAJ&hl=en) , [Salman Khan](https://salman-h-khan.github.io/)

**Mohamed bin Zayed University of Artificial Intelligence, The University of Western Australia, Linköping University, Australian National University**

[![Website](https://img.shields.io/badge/Project-Website-87CEEB)](https://mbzuai-oryx.github.io/GeoPixel/)
[![paper](https://img.shields.io/badge/arXiv-Paper-<COLOR>.svg)](https://arxiv.org/abs/2501.13925)
[![HuggingFace](https://img.shields.io/badge/HuggingFace-Model-F9D371)](https://huggingface.co/collections/MBZUAI/geopixel-67b6e1e441250814d06f2043)
[![GitHub stars](https://img.shields.io/github/stars/mbzuai-oryx/GeoPixel?color=FFF359&style=flat)](https://github.com/mbzuai-oryx/GeoPixel/stargazers)
  [![GitHub license](https://img.shields.io/github/license/mbzuai-oryx/GeoPixel?color=FF8080)](https://github.com/mbzuai-oryx/GeoPixel/blob/main/LICENSE)
  
---

## 📢  Latest Updates
- **May-01-2025**: 🔥 GeoPixel is accepted at ICML 2025
- **Feb-26-2025**: 📂 GeoPixelD dataset is released on **_HuggingFace_** [MBZUAI/GeoPixelD](https://huggingface.co/datasets/MBZUAI/GeoPixelD)
- **Feb-20-2025**: 🚀 GeoPixel training and finetuning code is released. 
- **Feb-20-2025**: 🔥 Our model checkpoints are released on **_HuggingFace_** [link](https://huggingface.co/collections/MBZUAI/geopixel-67b6e1e441250814d06f2043). 
- **Jan-24-2025**: 📜 Technical Report of GeoPixel paper is released [arxiv link](https://arxiv.org/abs/2501.13925).

- 👉 [Get Started with GeoPixel](https://github.com/mbzuai-oryx/GeoPixel/blob/main/README.md#%EF%B8%8F-usage)
  
---

## <img src="assets/logo.png" height="30"> GeoPixel Overview  
GeoPixel is the first large multimodal model explicitly designed for high-resolution remote sensing (RS) image comprehension and pixel-level grounding. The model processes natural language user queries with RS imagery to generate detailed outputs, incorporating interleaved masks that adapt dynamically to the spatial resolution and complexity of the input.

<p align="center">
  <img src="assets/overview.png" width="60%">
</p>

---
## 🏆 Highlights  
- We present GeoPixel, a pixel grounding Large Multimodal Model optimized for high-resolution remote sensing image comprehension. It features adaptive image partitioning into local and global regions, enabling efficient processing of resolutions up to 4K in any aspect ratio.
- A rich annotated dataset GeoPixelD, is created that supports Remote Sensing Grounded Conversation Generation RS-GCG. This dataset combines scene-level context and object-level details through a scalable annotation pipeline that uses advanced visual prompting designed for RS imagery.
- A detailed evaluation benchmark is provided, containing 5,427 validated referring expression-mask pairs and 61,384 annotated objects. The dataset, with detailed descriptions averaging 647 characters, establishes a standard for testing the fine-grained understanding and generation capabilities of remote sensing models.

---
## ⚙️ Requirements

- python 3.10 and above
- pytorch >= 2.3.1, torchvision >= 0.18.1 are recommended
- CUDA 11.8 and above is recommended (Please follow the instructions [here](https://pytorch.org/get-started/locally/) to install both PyTorch and TorchVision dependencies)
- [flash-attention2](https://github.com/Dao-AILab/flash-attention) is required for high-resolution usage
  <br>

---

## 🛠️ Usage
Follow the guidelines below to set up and use GeoPixel efficiently:
- [GeoPixelD data](./docs/dataset.md):📌 This section provides instructions on how to access and prepare the GeoPixelD dataset
- [Installation Guidelines](./docs/install.md) :⚙️ This section includes step-by-step instructions on setting up the necessary dependencies, installing required libraries, and configuring your environment for running GeoPixel.
- [Training and Finetuning](./docs/finetune.md) :🚀 This guide explains how to train the GeoPixel model from scratch or fine-tune a pre-trained version for downstream remote sensing tasks.
- [Inference Guide](./docs/inference.md): 🔍 This section describes how to use a trained GeoPixel model for making predictions, running inference on images and generating segmentation masks.

---

<!-- Architecture -->
## 🛠️ Architecture

<p align="center">
  <img src="assets/architecture.png" alt="GeoPixel Architecture">
</p>

GeoPixel is fundamentally composed of five key blocks: (1) Adaptive Image Divider (2) Vision Encoder (3) Large Language Model (4) Grounding Vision Encoder (5) Pixel Decoder. These modules are seamlessly integrated to facilitate high-resolution visual perception, fine-grained semantic interpretation, and precise pixel-level grounding of Remote Sensing (RS) imagery.

---
## 🏷️ Annotation Pipeline

<p align="center">
  <img src="assets/annotation_pipeline.png" alt="Annotation Pipeline">
</p>

We propose a semi-automatic annotation pipeline for creating a remote sensing grounded conversation generation (RS-GCG) dataset. It employs a multi-level hierarchical strategy that includes holistic scene descriptions, individual instance annotations, and group-level semantic representations, enabling a comprehensive understanding of spatial relationships and object-level details. Advanced techniques, such as Set-of-Mark (SOM) prompting combined with spatial and categorical priors, are utilized to enhance the accuracy and granularity of object-specific annotations. 

---
## 🔍 Remote Sensing Grounded Conversation Generation (RS-GCG)

<p align="center">
  <img src="assets/rsgcg_qualitative.png" alt="rsgcg qualitative">
</p>

GeoPixel processes user queries to produce comprehensive descriptive outputs while simultaneously grounding identified objects through interleaved, pixel-level masks, demonstrating its advanced understanding and precise interpretation of high resolution remote sensing imagery.

<p align="center">
  <img src="assets/tab_rsgcg.png" alt="rsgcg qualitative">
</p>

Performance Comparison of various models on the Remote Sensing Grounded Conversation Generation (RS-GCG) task. LISA† and PixelLM† refer to pretrained models finetuned on GeoPixelD training data. GLaMM represents zero-shot performance, while GLaMM-FT denotes the pretrained model finetuned on GeoPixelD. GeoPixel demonstrates superior performance across all metrics.

---

## 🔍 Referring Remote Sensing Image Segmentation (RRSIS)

<p align="center">
  <img src="assets/rrsis_qualitative.png" alt="rrsis qualitative">
</p>

GeoPixel demonstrates a robust capability to interpret referring expressions of varying complexity and lengths to accurately generate precise segmentation masks.
<p align="center">
  <img src="assets/tab_rrsis.png" width="70%" alt="rsgcg qualitative">
</p>

Performance Comparison of GeoPixel in Referring Expression Segmentation on RRSIS-D dataset: The segmentation accuracy based on referring expressions is expressed through the Precision at IoU threshold of 0.5 (P@0.5), Overall Intersection-over-Union (oIoU) and Mean Intersection-over-Union (mIoU).

---

## 📜 Citation 

```bibtex
@inproceedings{
shabbir2025geopixel,
title={GeoPixel: Pixel Grounding Large Multimodal Model in Remote Sensing},
author={Akashah Shabbir and Mohammed Zumri and Mohammed Bennamoun and Fahad Shahbaz Khan and Salman Khan},
booktitle={Forty-second International Conference on Machine Learning},
year={2025},
articleno = {2145},
numpages = {17},
location = {Vancouver, Canada},
series = {ICML'25}
}
```

---
## 🙏 Acknowledgement 
We appreciate InternLM-XComposer (IXC), GlaMM, and LISA for making their models and code available as open-source contributions.

---

[<img src="assets/IVAL_logo.png" width="200" height="100">](https://www.ival-mbzuai.net)
[<img src="assets/Oryx_logo.png" width="100" height="100">](https://github.com/mbzuai-oryx)
[<img src="assets/MBZUAI_logo.png" width="360" height="85">](https://mbzuai.ac.ae)
