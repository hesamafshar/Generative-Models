# A Deep Dive into the AI/ML Research Landscape

**Hesam Afshar, Shaghayegh Roozmeh**  
**Course:** Generative Models, University of Tehran  
**Date:** September 2025

This is a cleaned Markdown version of the research work we prepared for the Generative Models course. The main goal was to go through a realistic paper-search process, select a paper that was both technically interesting and feasible with our computational resources, and then study the work before and after it through backward and forward citations.

## Selected paper

**Generative Sliced MMD Flows with Riesz Kernels**  
Johannes Hertrich, Christian Wald, Fabian Altekrüger, and Paul Hagemann, ICLR 2024.

We selected this paper after screening recent work from ICLR, NeurIPS, and ICML. An important part of the selection was feasibility: we checked whether code and data were available and whether the reported experiments could reasonably be studied with limited GPU resources. The selected paper was attractive because its experiments included standard image datasets such as MNIST, Fashion-MNIST, CIFAR-10, and low-resolution CelebA, and the authors reported running them on single GPUs.

The paper studies a non-adversarial approach to generative modeling based on Maximum Mean Discrepancy (MMD). Instead of using a GAN discriminator or a diffusion schedule, the method uses a Riesz/energy-distance kernel and follows an MMD gradient flow. A central idea is that, for this kernel family, the high-dimensional discrepancy can be related to sliced one-dimensional computations. In the energy-distance case, the one-dimensional computation can be performed efficiently using sorting, which makes the method practical on smaller image-generation benchmarks.

## Backward research

We traced the main ideas behind the paper rather than reading it in isolation. The main line we followed was:

1. **Energy distance and E-statistics** -- distance-based ways of comparing probability distributions.
2. **Maximum Mean Discrepancy (MMD)** -- kernel-based two-sample testing and kernel mean embeddings.
3. **Connection between energy distance and MMD** -- the equivalence between distance-based and RKHS-based statistics for suitable kernels.
4. **MMD-based neural generators** -- early work such as GMMN, which showed that generators can be trained directly with MMD but also exposed computational difficulties in high dimensions.
5. **Sliced optimal transport and Sliced Wasserstein methods** -- reducing high-dimensional distribution comparison to many one-dimensional projections.
6. **MMD gradient flows** -- treating generation as movement of samples along a probability-space gradient flow.
7. **Sliced MMD** -- bringing the slicing idea into the MMD framework.

This path helped us understand why the selected paper combines three specific ideas: a distance-based kernel, slicing, and gradient-flow training. Each of them addresses a different limitation of earlier MMD-based generative models.

## Forward research

We also looked for later work that cited or extended the selected paper. The main directions we found were:

- **Deep MMD Gradient Flow without adversarial training:** introduces noise-adaptive learned features for stronger MMD-based gradients.
- **Posterior sampling with negative-distance MMD flows:** extends the same general framework to conditional and inverse problems.
- **Smoothed distance kernels:** studies smoother versions of distance kernels to improve numerical and theoretical behavior.
- **QMC slicing for radial kernels:** replaces purely random slice directions with more structured sampling to reduce the number of slices needed for accurate computation.

These papers showed that the original idea could be extended in several ways without returning to the standard adversarial-training setup.

## What we learned from the process

A useful part of this assignment was that paper selection was treated as part of the research rather than as an afterthought. Many interesting papers were not realistic for us because their experiments depended on large multi-GPU setups. We therefore included code availability, data availability, and computational cost in the screening process.

The project also showed us that a research direction becomes much easier to understand after following both backward and forward citations. The backward search explains where the main ideas came from and which problems they were meant to solve. The forward search shows which parts of the method later researchers considered useful enough to extend.

The original screening table is included in `paper_screening.csv`.

## References

1. Hertrich, J., Wald, C., Altekrüger, F., & Hagemann, P. (2024). *Generative Sliced MMD Flows with Riesz Kernels*. ICLR 2024.
2. Székely, G. J. (2002). *E-statistics: The energy of statistical samples*.
3. Gretton, A., Borgwardt, K. M., Rasch, M., Schölkopf, B., & Smola, A. J. (2012). *A Kernel Two-Sample Test*. JMLR.
4. Sejdinovic, D., Sriperumbudur, B. K., Gretton, A., & Fukumizu, K. (2013). *Equivalence of Distance-Based and RKHS-Based Statistics in Hypothesis Testing*. Annals of Statistics.
5. Dziugaite, G. K., Roy, D. M., & Ghahramani, Z. (2015). *Training Generative Neural Networks via Maximum Mean Discrepancy Optimization*. UAI.
6. Li, C.-L., Chang, W.-C., Cheng, Y., Yang, Y., & Póczos, B. (2017). *MMD GAN: Towards Deeper Understanding of Moment Matching Network*. NeurIPS.
7. Bińkowski, M., Sutherland, D. J., Arbel, M., & Gretton, A. (2018). *Demystifying MMD GANs*. ICLR.
8. Rabin, J., Peyré, G., Delon, J., & Bernot, M. (2012). *Wasserstein Barycenter and Sliced Wasserstein Distances*.
9. Liutkus, A., Şimşekli, U., Majewski, S., Durmus, A., & Stöter, F.-R. (2019). *Sliced-Wasserstein Flows*. ICML.
10. Arbel, M., Korba, A., Salim, A., & Gretton, A. (2019). *Maximum Mean Discrepancy Gradient Flow*. NeurIPS.
11. Kolouri, S., Nadjahi, K., Simsekli, U., & Shahrampour, S. (2022). *Sliced Maximum Mean Discrepancy*. IEEE Transactions on Signal Processing.
12. Galashov, A., de Bortoli, V., & Gretton, A. (2025). *Deep MMD Gradient Flow without Adversarial Training*. ICLR.
13. Hagemann, P. et al. (2024). *Posterior Sampling Based on Gradient Flows of the MMD with Negative Distance Kernel*. ICLR.
14. Hertrich, J., Rux, N., Stein, V., & Steidl, G. (2025). *Smoothed Distance Kernels for Maximum Mean Discrepancies*.
15. Hertrich, J., Jahn, T., & Quellmalz, M. (2025). *Fast Summation of Radial Kernels via QMC Slicing*. ICLR.
