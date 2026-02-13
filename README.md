# Generative AI — Synthetic Satellite Imagery with Variational Autoencoders

## Project Description

This project implements a generative deep learning system that models and synthesizes Earth-observation satellite imagery using a convolutional β-Variational Autoencoder (VAE). The model learns a compact latent representation of terrain textures and generates plausible synthetic satellite images. The workflow emphasizes generative modeling, latent structure learning, and qualitative evaluation rather than raw image realism.

Dataset used: *EuroSAT Satellite Land Use Dataset*  
https://www.kaggle.com/datasets/apollo2506/eurosat-dataset

The project can be interpreted as a prototype simulation module for autonomous aerospace sensing systems, where synthetic imagery supports robustness testing and scenario exploration.

---

## What I Built

I implemented a full generative modeling pipeline that includes:

- Filesystem validation and dataset inspection  
- Custom PyTorch dataset loader for satellite imagery  
- Image preprocessing and normalization  
- Convolutional β-VAE architecture  
- Stable training with early stopping and checkpointing  
- Loss curve diagnostics and validation monitoring  
- Reconstruction and synthetic image generation  
- Latent space interpolation analysis  
- A reproducible notebook that runs top-to-bottom  

The notebook demonstrates practical deep generative modeling suitable for remote sensing and aerospace simulation workflows.

---

## Model Implemented

The project uses a **β-Variational Autoencoder** with:

- Convolutional encoder/decoder architecture  
- 128-dimensional latent space  
- Mean squared error reconstruction loss  
- Reduced KL regularization (β = 0.1)  
- Early stopping based on validation loss  
- Best-model checkpoint saving  

This design balances reconstruction fidelity with structured latent sampling.

---

## How to Run generative_ai.ipynb

### Install dependencies

```bash
pip install -r requirements.txt
```
---
The requirements file was generated using:

pip freeze > requirements.txt

---
## Run the notebook

1. Clone or download this repository

2. Open generative_ai.ipynb in Jupyter Notebook or Google Colab

3. Run all cells from top to bottom

The notebook executes without hidden state and reproduces the full generative pipeline.

Optional (Google Colab):

If running with Google Drive storage, uncomment the Drive mounting cell at the top.

---
## Reproducibility

This project emphasizes reproducible generative modeling:

* Deterministic dataset splitting with fixed seeds

* Explicit architecture and optimizer configuration

* Saved best-model checkpoint (best_vae_eurosat.pt)

* Loss curve diagnostics

* Captured software environment via requirements.txt

* Version-controlled workflow via Git

Another user can recreate the environment and regenerate results using only repository contents.

---

## Bias Awareness

Satellite datasets reflect geographic and land-use sampling biases. If certain terrain classes are overrepresented, the generative model may implicitly encode skewed assumptions about real-world distributions. Synthetic imagery produced by the model should not be interpreted as statistically representative of global geography.

Responsible use requires transparency about dataset composition and clear separation between simulated and real observational data.

---

## Reflection: Generative Modeling Insights

The VAE successfully captures coarse terrain statistics and produces stable synthetic textures. Reconstructions preserve global structure but blur fine details, a known property of pixel-level VAE objectives. Latent interpolation demonstrates a smooth, continuous generative manifold, confirming meaningful latent representation learning.

This illustrates the tradeoff between reconstruction sharpness and probabilistic structure inherent to VAEs.

---
## Reflection: Future Extensions

Potential improvements include:

* Higher-resolution satellite imagery

* Conditional generation by terrain class

* Perceptual or adversarial loss functions

* Multi-band spectral inputs

* Hybrid VAE–GAN architectures

* Physics-informed generative constraints

* These extensions could increase realism while preserving generative stability.
* 
---
## Reflection: Autonomous Aerospace Simulation

This project can be interpreted as a simulation component of an autonomous aerospace monitoring system. A production pipeline could generate synthetic satellite scenes to stress-test perception models, evaluate anomaly detection systems, or augment limited remote sensing datasets. The modular design supports integration into larger AI-driven aerospace analytics frameworks.
---

## Repository Structure
📓 generative_ai.ipynb
📄 Generative_AI_Analysis_Report.pdf
📄 requirements.txt
📦 best_vae_eurosat.pt
📘 README.md


This repository demonstrates a complete, professional deep generative modeling workflow suitable for advanced AI portfolios and aerospace simulation research.
