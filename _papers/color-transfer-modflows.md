---
layout: paper
title: "Color Conditional Generation with Sliced Wasserstein Distance"
authors: "Alexander Lobashev, Dmitry Guskov, Maria Larchenko"
conference: "CVPR 2025"
permalink: /papers/color-conditional-generation/
---

## Abstract  
We propose SW-Guidance, a training-free approach for image generation conditioned on the color distribution of a reference image. While it is possible to generate an image with fixed colors by first creating an image from a text prompt and then applying a color style transfer method, this approach often results in semantically meaningless colors in the generated image. 

Our method solves this problem by modifying the sampling process of a diffusion model to incorporate the differentiable Sliced 1-Wasserstein distance between the color distribution of the generated image and the reference palette. Our method outperforms state-of-the-art techniques for color-conditional generation in terms of color similarity to the reference, producing images that not only match the reference colors but also maintain semantic coherence with the original text prompt.
