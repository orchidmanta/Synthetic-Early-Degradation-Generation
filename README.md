# 20261R0136COSE362 — Synthetic Early Degradation Generation

###cEach student should create a personal GitHub account and upload the project code to a public repository using the following format:
아흐마드 나우팔 : https://github.com/naufalasro/20261R0136COSE362
하짐: https://github.com/hazimxm04/20261R0136COSE362\
Feras: https://github.com/FerasM07/20261R0136COSE362
마랄마: https://github.com/Renenny/20261R0136COSE362
-
## Team I4 — AI + Logistics Supply Chain

**Course**: COSE362 Machine Learning | Korea University | 2026 Spring

---

## Project Overview

This project explores synthetic early bearing fault data generation 
using GAN-based models on the CWRU bearing dataset.

We train only on **Normal (α=0.00)** and **Ball021 (α=0.21)** signals,
then generate **unseen intermediate severity Ball007 (α=0.07)** — 
without ever seeing real Ball007 during training.

The best model (WGAN-GP, λ=10) achieves **96.84% downstream classifier 
accuracy** — only **3.16% gap from the real data baseline**.

---

## Repository Structure

├── mahirah/                  # Individual member notebooks

├── TeamI4_final_submission.ipynb  ← FINAL SUBMISSION

└── README.md


## Final Submission

**`TeamI4_final_submission.ipynb`** is the official final submission for Team I4.

It contains the full pipeline:
- Data loading and preprocessing (CWRU dataset)
- Window size selection experiment
- GAN family training (E1–E9 experiments + F1 2D)
- Evaluation metrics (classifier accuracy, ACF, PSD, envelope similarity)
- Results comparison and analysis

---

## Model Weights

Pre-trained model checkpoints are stored on Google Drive.
*https://drive.google.com/drive/folders/1NylCk_K50v5zTm0PiUd2SSQ87efR3Ldn?usp=sharing*

---

## Team Members

| Name | Student ID |
|------|------------|
마랄마 
ABDULLAH FERAS MOHAMMED HASSAN 
마히라 소피아 
하짐 
아흐마드 나우팔 
---

## Key Results

| Model | Classifier Acc | Ball007 Acc | Gap |
|-------|---------------|-------------|-----|
| Real Ball007 (baseline) | 100.00% | 100.00% | — |
| **WGAN-GP (λ=10)** | **96.84%** | **90.53%** | **3.16%** |
| FiLM-Simple WGAN-GP | 93.00% | 80.00% | 7.00% |
| CGAN | 82.78% | — | 17.22% |
| GAN | 66.61% | — | 33.39% |
