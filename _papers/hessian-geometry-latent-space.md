---
layout: paper
title: "Hessian Geometry of Latent Space in Generative Models"
authors: "Alexander Lobashev, Dmitry Guskov, Maria Larchenko, Mikhail Tamm"
conference: "ICML 2025"
venue_type: conference
year: 2025
permalink: /papers/hessian-geometry-latent-space/
abstract: "This paper presents a novel method for analyzing the latent space geometry of generative models, including statistical physics models and diffusion models, by reconstructing the Fisher information metric. The method approximates the posterior distribution of latent variables given generated samples and uses this to learn the log-partition function, which defines the Fisher metric for exponential families. Theoretical convergence guarantees are provided, and the method is validated on the Ising and TASEP models, outperforming existing baselines in reconstructing thermodynamic quantities. Applied to diffusion models, the method reveals a fractal structure of phase transitions in the latent space, characterized by abrupt changes in the Fisher metric. We demonstrate that while geodesic interpolations are approximately linear within individual phases, this linearity breaks down at phase boundaries, where the diffusion model exhibits a divergent Lipschitz constant with respect to the latent space. These findings provide new insights into the complex structure of diffusion model latent spaces and their connection to phenomena like phase transitions."
image: "/assets/images/hessian_geometry_result.png"
tags: [latent-space-geometry, diffusion-models, fisher-information, statistical-physics, theoretical-foundations]
featured: true
arxiv: https://arxiv.org/abs/2506.10632
github: https://github.com/alobashev/hessian-geometry-of-diffusion-models
# openreview: https://openreview.net/forum?id=...
# pdf: /assets/papers/hessian-geometry-latent-space.pdf
bibtex: |
  @article{lobashev2025hessian,
    title={Hessian Geometry of Latent Space in Generative Models},
    author={Lobashev, Alexander and Guskov, Dmitry and Larchenko, Maria and Tamm, Mikhail},
    journal={arXiv preprint arXiv:2506.10632},
    year={2025}
  }
key_contributions:
  - "Novel method for analyzing latent space geometry via Fisher information metric"
  - "Reveals fractal structure of phase transitions in diffusion model latent spaces"
  - "Demonstrates breakdown of linear interpolation at phase boundaries"
  - "Provides theoretical convergence guarantees with validation on physics models"
related_papers:
  - fbm-generative-inpainting
---

## Abstract  
This paper presents a novel method for analyzing the latent space geometry of generative models, including statistical physics models and diffusion models, by reconstructing the Fisher information metric. The method approximates the posterior distribution of latent variables given generated samples and uses this to learn the log-partition function, which defines the Fisher metric for exponential families. 

Theoretical convergence guarantees are provided, and the method is validated on the Ising and TASEP models, outperforming existing baselines in reconstructing thermodynamic quantities. Applied to diffusion models, the method reveals a fractal structure of phase transitions in the latent space, characterized by abrupt changes in the Fisher metric. 

We demonstrate that while geodesic interpolations are approximately linear within individual phases, this linearity breaks down at phase boundaries, where the diffusion model exhibits a divergent Lipschitz constant with respect to the latent space. These findings provide new insights into the complex structure of diffusion model latent spaces and their connection to phenomena like phase transitions.
