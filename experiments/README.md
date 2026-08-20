# MNIST Generative-Model Experiments

These notebooks are from the implementation part of my Generative Models course work. I used MNIST as a common dataset to implement and compare several types of generative models.

The notebooks are organized by model rather than assignment number:

- `Autoregressive_NADE_FVSBN.ipynb` — NADE and FVSBN autoregressive models
- `VAE.ipynb` — VAE training, generation, latent-space visualization, and interpolation
- `GMM_NADE_VAE_Comparison.ipynb` — GMM baseline with NADE/VAE training and comparison
- `NICE_GAN_EBM_Comparison.ipynb` — NICE, GAN, and EBM implementations with generation and sample-quality comparisons
- `DDPM_Distillation.ipynb` — diffusion training, sampling, evaluation, and a distillation experiment

I did not include the large checkpoint/log folders from the original Colab runs. The notebooks themselves keep the useful saved outputs from the experiments.
