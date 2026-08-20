# Generative Models

This repository contains the main implementation and research work I completed for the Generative Models course at the University of Tehran.

The implementation part uses MNIST as a common benchmark to work with different families of generative models, including autoregressive models, VAEs, normalizing flows, GANs, energy-based models, and diffusion models. I kept the notebooks with their original experiment outputs so the training behavior and comparisons can be reviewed directly.

The research part was done with Shaghayegh Roozmeh. We screened recent papers from major ML conferences based on topic, code/data availability, and computational cost. After selecting **Generative Sliced MMD Flows with Riesz Kernels**, we followed its backward and forward citations and prepared a technical report on the line of work around it.

## Repository structure

- `experiments/` — implementation notebooks and model comparisons on MNIST
- `research/Research_Report.md` — course research report
- `research/paper_screening.csv` — paper-screening table used during topic and paper selection

## Main experiment notebooks

- `Autoregressive_NADE_FVSBN.ipynb` — NADE and FVSBN autoregressive models
- `VAE.ipynb` — variational autoencoder experiments
- `GMM_NADE_VAE_Comparison.ipynb` — comparison of GMM, NADE, and VAE
- `NICE_GAN_EBM_Comparison.ipynb` — NICE, GAN, and energy-based model experiments
- `DDPM_Distillation.ipynb` — lightweight diffusion model, generation/evaluation, and distillation experiments

The large checkpoint and log folders from the original Colab runs are not included here. The notebooks keep the code and useful saved outputs needed to review the experiments.
