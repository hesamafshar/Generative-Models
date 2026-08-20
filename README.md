# Generative Models

This repository collects the main work from our Generative Models course at the University of Tehran.

The course work had two parts. In the first part, we implemented and compared several types of generative models on MNIST, including autoregressive models, VAE, NICE, GAN, energy-based models, and diffusion models. Using the same dataset made it easier to compare how the different approaches behave in practice.

The second part was more research-oriented. We searched recent papers from ICLR, NeurIPS, and ICML, narrowed them based on code/data availability and computational cost, and then followed backward and forward citations for the selected paper. We finally focused on **Generative Sliced MMD Flows with Riesz Kernels** and prepared a technical report on the related work around it.

## Repository structure

- `experiments/` — implementation notebooks and model comparisons on MNIST
- `research/Research_Report.md` — our course research report
- `research/paper_screening.csv` — the paper-screening table used during paper selection

## Experiment notebooks

- `Autoregressive_NADE_FVSBN.ipynb` — NADE and FVSBN
- `VAE.ipynb` — VAE
- `GMM_NADE_VAE_Comparison.ipynb` — GMM, NADE, and VAE comparison
- `NICE_GAN_EBM_Comparison.ipynb` — NICE, GAN, and EBM comparison
- `DDPM_Distillation.ipynb` — diffusion model and distillation experiments

The large checkpoint and log folders from the original Colab runs are not included here. The notebooks keep the code and the useful saved outputs from the experiments.
