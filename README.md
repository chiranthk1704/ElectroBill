# Plant Recognition Model Comparison — YOLO & ResNet (Minor Project BIS586)

**Short summary:**  
This repository contains the artifacts, figures, and documentation for a comparative study of YOLO and ResNet-9 for plant species recognition. Experimental results and implementation details are taken from the project reports included in `/docs`.

---

## Table of contents
- [Overview](#overview)
- [System architecture](#system-architecture)
- [Dataset & preprocessing](#dataset--preprocessing)
- [Models & training](#models--training)
- [Results (reported)](#results-reported)
- [How to reproduce (commands from report)](#how-to-reproduce-commands-from-report)
- [App / Demo](#app--demo)
- [File structure](#file-structure)
- [Limitations & future work](#limitations--future-work)
- [Authors & citation](#authors--citation)
- [License](#license)

---

## Overview
Automated plant recognition helps in agriculture and biodiversity monitoring. This project evaluates YOLO (real-time object detection) and ResNet-9 (deep classification) on the PlantifyDr dataset and compares them with a referenced ANN-based approach. All experimental numbers below are **reported** from the project documentation (see `/docs`).

---

## System architecture
The repository documents two main model flows:
- **YOLO:** single-pass detection + classification — optimized for inference speed.
- **ResNet-9:** residual classifier for detailed feature learning — optimized for accuracy.

<p align="center">
  <img src="images/yolo_arch.png" alt="YOLO architecture" width="640"/>
  <br/>
  <em>Figure: YOLO architecture (backbone, neck, head)</em>
</p>

<p align="center">
  <img src="images/resnet_arch.png" alt="ResNet architecture" width="640"/>
  <br/>
  <em>Figure: ResNet-9 architecture (residual blocks)</em>
</p>

---

## Dataset & preprocessing
- **Dataset:** PlantifyDr (used in evaluation as documented).  
- **Preprocessing:** images were resized, normalized and standard augmentations applied (see report for exact transformations).  

---

## Models & training
- **YOLO** — detection pipeline used for real-time identification.  
- **ResNet-9** — classification network with residual blocks.  
Training details (optimizers, learning rates, epochs, and weight checkpoints) are documented in the project report and `/docs`.

---

## Results (reported)
> Results below are taken from the project report and comparison document in `/docs`.

- **YOLO (reported)** — Average accuracy: **90.21%**  
- **ResNet (reported)** — Average accuracy: **87.74%**  
- **Reference ANN-based** — Reported accuracy: **92.48%** (from the referenced study)

**Notes:** the above numbers appear in the project report; they are reproduced here for summary and comparison only.

---

## How to reproduce (commands from report)
> These commands are taken from the project documentation and have not been re-executed in this repository.

1. Create environment:
```bash
python -m venv .venv
source .venv/bin/activate     # Linux / macOS
.venv\Scripts\activate        # Windows
pip install -r requirements.txt
