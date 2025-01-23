# GeoPixel <img src="assets/logo.png" height="50">: Pixel Grounding Large Multimodal Model in Remote Sensing

![](https://i.imgur.com/waxVImv.png)

[Akashah Shabbir](https://github.com/AkashahS) , [Mohammed Zumri](https://github.com/zzumri) , [Mohammed Bennamoun](https://scholar.google.com/citations?user=ylX5MEAAAAAJ&hl=en) , [Fahad Shahbaz Khan](https://scholar.google.es/citations?user=zvaeYnUAAAAJ&hl=en) , [Salman Khan](https://salman-h-khan.github.io/)

**Mohamed bin Zayed University of Artificial Intelligence, The University of Western Australia, Linköping University, Australian National University**

[![Website](https://img.shields.io/badge/Project-Website-87CEEB)](https://mbzuai-oryx.github.io/GeoPixel/)
[![paper](https://img.shields.io/badge/arXiv-Paper-<COLOR>.svg)](https://arxiv.org/)

---

## 📢 Latest Updates
- 📦 Code, Model checkpoints and dataset will be released soon.
- **Jan-24-2025**: Technical Report of GeoPixel paper is released [arxiv link]. 🔥🔥
---

## <img src="assets/logo.png" height="25">  GeoPixel Overview
GeoPixel is a first large multimodal model explicitly designed for high-resolution remote sensing (RS) image comprehension and pixel-level grounding. The model processes natural language user queries with RS imagery to generate detailed outputs, incorporating interleaved masks that adapt dynamically to the spatial resolution and complexity of the input.

<p align="center">
  <img src="assets/overview.png" width="60%">
</p>

---
## 🏆 Highlights
1. We present GeoPixel, a pixel grounding Large Multimodal Model optimized for high-resolution remote sensing image comprehension. It features adaptive image partitioning into local and global regions, enabling efficient processing of resolutions up to 4K in any aspect ratio.
2. A rich annotated dataset GeoPixelD, is created that supports Remote Sensing Grounded Conversation Generation RS-GCG. This dataset combines scene-level context and object-level details through a scalable annotation pipeline that uses advanced visual prompting designed for RS imagery.
3. A detailed evaluation benchmark is provided, containing 5,427 validated referring expression-mask pairs and 61,384 annotated objects. The dataset, with detailed descriptions averaging 647 characters, establishes a standard for testing the fine-grained understanding and generation capabilities of remote sensing models.

---
<!-- Architecture -->
## Architecture

<p align="center">
  <img src="assets/architecture.png" alt="GeoPixel Architecture">
</p>

GeoPixel is fundamentally composed of five key blocks: (1) Adaptive Image Divider (2) Vision Encoder (3) Large Language Model (4) Grounding Vision Encoder (5) Pixel Decoder. These modules are seamlessly integrated to facilitate high-resolution visual perception, fine-grained semantic interpretation, and precise pixel-level grounding of Remote Sensing (RS) imagery.

---
## Annotation Pipeline

<p align="center">
  <img src="assets/annotation_pipeline.png" alt="Annotation Pipeline">
</p>

We propose a semi-automatic annotation pipeline for creating a remote sensing grounded conversation generation (RS-GCG) dataset. It employs a multi-level hierarchical strategy that includes holistic scene descriptions, individual instance annotations, and group-level semantic representations, enabling a comprehensive understanding of spatial relationships and object-level details. Advanced techniques, such as Set-of-Mark (SOM) prompting combined with spatial and categorical priors, are utilized to enhance the accuracy and granularity of object-specific annotations. 


---
## Remote Sensing Grounded Conversation Generation (RS-GCG) 🔍

<p align="center">
  <img src="assets/rsgcg_qualitative.png" alt="rsgcg qualitative">
</p>

GeoPixel processes user queries to produce comprehensive descriptive outputs while simultaneously grounding identified objects through interleaved, pixel-level masks, demonstrating its advanced understanding and precise interpretation of high resolution remote sensing imagery.

<p align="center">
  <img src="assets/tab_rsgcg.png" alt="rsgcg qualitative">
</p>

Performance Comparison of various models on the Remote Sensing Grounded Conversation Generation (RS-GCG) task. LISA† and PixelLM† refer to pretrained models finetuned on GeoPixelD training data. GLaMM represents zero-shot performance, while GLaMM-FT denotes the pretrained model finetuned on GeoPixelD. GeoPixel demonstrates superior performance across all metrics.

---

## Referring Remote Sensing Image Segmentation (RRSIS) 🔍

<p align="center">
  <img src="assets/rrsis_qualitative.png" alt="rrsis qualitative">
</p>

GeoPixel demonstrates a robust capability to interpret referring expressions of varying complexity and lengths to accurately generate precise segmentation masks.
<p align="center">
  <img src="assets/tab_rrsis.png" width="70%" alt="rsgcg qualitative">
</p>

Performance Comparison of GeoPixel in Referring Expression Segmentation on RRSIS-D dataset: The segmentation accuracy based on referring expressions is expressed through the Precision at IoU threshold of 0.5 (P@0.5), Overall Intersection-over-Union (oIoU) and Mean Intersection-over-Union (mIoU).

---

## Citation 📜

```bibtex
@article{shabbir2025geopixel,
  title={GeoPixel : Pixel Grounding Large Multimodal Models in Remote Sensing}, 
  author={Akashah Shabbir, Mohammed Zumri, Mohammed Bennamoun, Fahad S. Khan, Salman Khan},
  journal={ArXiv},
  year={2025},
  url={https://arxiv.org/}
}
```

---

[<img src="assets/IVAL_logo.png" width="200" height="100">](https://www.ival-mbzuai.com)
[<img src="assets/Oryx_logo.png" width="100" height="100">](https://github.com/mbzuai-oryx)
[<img src="assets/MBZUAI_logo.png" width="360" height="85">](https://mbzuai.ac.ae)
