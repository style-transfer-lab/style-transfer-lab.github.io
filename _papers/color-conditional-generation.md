---
layout: paper
title: "Color Conditional Generation with Sliced Wasserstein Guidance"
authors: "Alexander Lobashev, Maria Larchenko, Dmitry Guskov"
conference: "NeurIPS 2025 (Spotlight)"
venue_type: conference
year: 2025
permalink: /papers/color-conditional-generation/
abstract: "We propose SW-Guidance, a training-free approach for image generation conditioned on the color distribution of a reference image. While it is possible to generate an image with fixed colors by first creating an image from a text prompt and then applying a color style transfer method, this approach often results in semantically meaningless colors in the generated image. Our method solves this problem by modifying the sampling process of a diffusion model to incorporate the differentiable Sliced 1-Wasserstein distance between the color distribution of the generated image and the reference palette. Our method outperforms state-of-the-art techniques for color-conditional generation in terms of color similarity to the reference, producing images that not only match the reference colors but also maintain semantic coherence with the original text prompt."
image: "/assets/images/sw-guidance-results.png"
tags: [color-transfer, diffusion-models, generative-models, wasserstein-distance, training-free]
featured: true
arxiv: https://arxiv.org/abs/2503.19034
github: https://github.com/alobashev/sw-guidance
# openreview: https://openreview.net/forum?id=...
# pdf: /assets/papers/color-conditional-generation.pdf
bibtex: |
  @article{lobashev2025color,
    title={Color Conditional Generation with Sliced Wasserstein Guidance},
    author={Lobashev, Alexander and Larchenko, Maria and Guskov, Dmitry},
    journal={arXiv preprint arXiv:2503.19034},
    year={2025}
  }
key_contributions:
  - "Training-free approach for color-conditioned image generation using diffusion models"
  - "Incorporates differentiable Sliced 1-Wasserstein distance during sampling process"
  - "Achieves state-of-the-art color similarity while maintaining semantic coherence"
related_papers:
  - color-transfer-modflows
---

## Abstract  
We propose SW-Guidance, a training-free approach for image generation conditioned on the color distribution of a reference image. While it is possible to generate an image with fixed colors by first creating an image from a text prompt and then applying a color style transfer method, this approach often results in semantically meaningless colors in the generated image. 

Our method solves this problem by modifying the sampling process of a diffusion model to incorporate the differentiable Sliced 1-Wasserstein distance between the color distribution of the generated image and the reference palette. Our method outperforms state-of-the-art techniques for color-conditional generation in terms of color similarity to the reference, producing images that not only match the reference colors but also maintain semantic coherence with the original text prompt.
