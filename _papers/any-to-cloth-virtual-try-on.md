---
layout: paper
title: "Creative Any-to-Cloth Generation with Virtual Try-On Pipelines"
authors: "Alexander Lobashev, Maria Larchenko, Dmitry Guskov"
conference: "Multimodal AI TTIC 2024"
venue_type: workshop
year: 2024
permalink: /papers/any-to-cloth-virtual-try-on/
abstract: "Virtual try-on (VITON) technology changes the way we shop by allowing customers to see how clothes look on them using augmented reality and artificial intelligence. This technology is important for online shopping but has several challenges, such as dealing with different body shapes, sizes, and poses, and maintaining the details of clothes intact. Though recent methods demonstrate good results with high-quality images and standard body shapes, they still face challenges in working as a complete solution for the VITON problem. However, we can still leverage existing VITON models along with Vision-Language models to build pipelines aimed at creative clothing design and fast prototyping. Here, we introduce an Any-to-Cloth pipeline that allows realistic virtual try-ons in various poses without the need for manual prompts. It allows the use of any image as a reference for new garments, and in contrast to diffusion-based models, it produces meaningfully looking clothes without complicated prompt engineering. This way, our pipeline is able to generate unexpected yet realistic designs, providing a creative tool for the fashion industry."
image: "/assets/images/any_to_cloth_results.png"
tags: [virtual-try-on, fashion-ai, vision-language-models, generative-models]
featured: true
# Add your links below (remove # to activate):
# arxiv: https://arxiv.org/abs/...
# openreview: https://openreview.net/forum?id=...
# github: https://github.com/...
# pdf: /assets/papers/any-to-cloth-virtual-try-on.pdf
bibtex: |
  @inproceedings{lobashev2024anytocloth,
    title={Creative Any-to-Cloth Generation with Virtual Try-On Pipelines},
    author={Lobashev, Alexander and Larchenko, Maria and Guskov, Dmitry},
    booktitle={Multimodal AI Workshop at TTIC},
    year={2024}
  }
key_contributions:
  - "Introduces Any-to-Cloth pipeline for creative clothing design without manual prompts"
  - "Leverages existing VITON models with Vision-Language models for fast prototyping"
  - "Generates realistic designs from any reference image without prompt engineering"
related_papers:
  - color-conditional-generation
---

## Abstract  

Virtual try-on (VITON) technology changes the way we shop by allowing customers to see how clothes look on them using augmented reality and artificial intelligence. This technology is important for online shopping but has several challenges, such as dealing with different body shapes, sizes, and poses, and maintaining the details of clothes intact. Though recent methods demonstrate good results with high-quality images and standard body shapes, they still face challenges in working as a complete solution for the VITON problem. However, we can still leverage existing VITON models along with Vision-Language models to build pipelines aimed at creative clothing design and fast prototyping. Here, we introduce an Any-to-Cloth pipeline that allows realistic virtual try-ons in various poses without the need for manual prompts. It allows the use of any image as a reference for new garments, and in contrast to diffusion-based models, it produces meaningfully looking clothes without complicated prompt engineering. This way, our pipeline is able to generate unexpected yet realistic designs, providing a creative tool for the fashion industry.
