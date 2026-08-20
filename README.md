# Generative Models

This repository collects the main work I did for the Generative Models course at the University of Tehran.

The course work had two parts. In the first part, I implemented and compared several types of generative models on MNIST, including NADE, VAE, NICE, GAN, and two energy-based model settings. These experiments were useful for seeing the differences between autoregressive, latent-variable, flow-based, adversarial, and energy-based approaches on the same dataset.

The second part was more research-oriented. Shaghayegh Roozmeh and I searched recent papers from ICLR, NeurIPS, and ICML, filtered them based on code/data availability and computational cost, and then followed backward and forward citations for the selected paper. We finally focused on **Generative Sliced MMD Flows with Riesz Kernels** and prepared a technical report on its background and later related work.

## Repository structure

- `research/Research_Report.md` -- a cleaned version of our course research report
- `research/paper_screening.csv` -- the paper-screening table used during paper selection
- `experiments/README.md` -- summary of the MNIST generative-model experiments

## MNIST experiments

The experiment folders kept in my original course files include:

- NADE
- VAE
- NICE
- GAN
- Energy-Based Model with learned mapping
- Energy-Based Model with PCA

The original Drive folders also contain training logs and checkpoints. I have not copied those large files here because they are not useful for reviewing the project. The repository is intended to keep the research material and source-level experiment files in a cleaner form.

## Research part

For paper selection, we first screened recent work in generative modeling and related bioinformatics areas. We considered whether the code and data were available and whether the experiments were realistic with limited computational resources. After selecting the MMD-flow paper, we traced the ideas leading to it and also reviewed later work that cited and extended it.

This was a course project, so the goal was not to claim a new research contribution. The main value for me was learning the process of searching papers, narrowing a research direction, reading related work, and connecting that process to implementation work.
