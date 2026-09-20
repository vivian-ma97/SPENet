# SPENet
# SPENet: A Spectral Estimation-Enhanced Framework for Low-Light Crack Segmentation in Architectural Heritage Surfaces

<p align="center">
  <img src="./figures/framework.png" width="90%">
</p>


## Overview

This repository provides the official implementation of:

**"A Spectral Estimation-Enhanced Framework for Low-Light Crack Segmentation in Architectural Heritage Surfaces"**

The proposed framework, termed **SPENet**, is designed for robust crack segmentation under challenging low-light conditions encountered in architectural heritage surface inspection.

Unlike conventional low-light crack segmentation methods that mainly rely on image enhancement or spatial feature extraction, SPENet introduces a **Spectral Estimation Module (SEM)** to explicitly model spectral and directional characteristics of crack structures.

The proposed SEM captures:

- spectral energy distribution;
- directional responses;
- directional coherence;
- orientation-related information;

to improve crack representation under weak illumination, low contrast, and complex surface textures.


---

## Method Overview

The overall framework consists of three major components:

1. **Low-light degradation simulation**

A controlled illumination degradation strategy is designed to simulate challenging low-light conditions, including:

- illumination attenuation;
- contrast degradation;
- noise amplification;
- shadow compression.

2. **Spectral Estimation Module (SEM)**

SEM extracts task-oriented spectral representations by jointly modeling:

- spectral energy;
- directional filtering responses;
- coherence characteristics;
- crack orientation information.

3. **Crack segmentation network**

The extracted spectral representations are integrated with spatial features for final pixel-level crack prediction.


<p align="center">
  <img src="./figures/SEM.png" width="80%">
</p>


---

# Installation

## Environment

The experiments were conducted with:

- Python 3.10
- PyTorch 2.0.0
- CUDA 11.8

Install dependencies:

```bash
conda create -n spenet python=3.10
conda activate spenet

pip install -r requirements.txt
