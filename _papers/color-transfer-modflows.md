---
layout: paper
title: "Color Transfer with Modulated Flows"
authors: "Maria Larchenko, Alexander Lobashev, Dmitry Guskov, Vladimir Vladimirovich Palyulin"
conference: "AAAI 2025"
venue_type: conference
year: 2025
permalink: /papers/color-transfer-modflows/
abstract: "In this work, we introduce Modulated Flows (ModFlows), a novel approach for color transfer between images based on rectified flows. The primary goal of color transfer is to adjust the colors of a target image to match the color distribution of a reference image.Our technique is based on optimal transport and executes color transfer as an invertible transformation within the RGB color space. ModFlows utilizes the bijective property of flows, enabling us to introduce a common intermediate color distribution and build a dataset of rectified flows. We train an encoder on this dataset to predict the weights of a rectified model for new images. After training on a set of optimal transport plans, our approach can generate optimal plans for new pairs of distributions without additional fine-tuning. We additionally show that the trained encoder provides an image embedding, associated only with its color style. The presented method is capable of processing 4K images and achieves state-of-the-art performance in terms of content and style similarity."
image: "/assets/images/modflows_results.jpg"
tags: [color-transfer, optimal-transport, rectified-flows, style-transfer]
featured: true
# Add your links below (remove # to activate):
# arxiv: https://arxiv.org/abs/...
# openreview: https://openreview.net/forum?id=...
# github: https://github.com/...
# pdf: /assets/papers/color-transfer-modflows.pdf
bibtex: |
  @inproceedings{larchenko2025color,
    title={Color Transfer with Modulated Flows},
    author={Larchenko, Maria and Lobashev, Alexander and Guskov, Dmitry and Palyulin, Vladimir Vladimirovich},
    booktitle={Proceedings of the AAAI Conference on Artificial Intelligence},
    volume={39},
    number={4},
    pages={4464--4472},
    year={2025}
  }
key_contributions:
  - "Novel approach based on rectified flows for color transfer with invertible transformations"
  - "Trained encoder predicts optimal transport plans without fine-tuning"
  - "Processes 4K images with state-of-the-art performance in content and style similarity"
  - "Provides color style embeddings independent of image content"
related_papers:
  - color-conditional-generation
---

## Abstract  
In this work, we introduce Modulated Flows (ModFlows), a novel approach for color transfer between images based on rectified flows. The primary goal of color transfer is to adjust the colors of a target image to match the color distribution of a reference image. 

Our technique is based on optimal transport and executes color transfer as an invertible transformation within the RGB color space. ModFlows utilizes the bijective property of flows, enabling us to introduce a common intermediate color distribution and build a dataset of rectified flows. We train an encoder on this dataset to predict the weights of a rectified model for new images. 

After training on a set of optimal transport plans, our approach can generate optimal plans for new pairs of distributions without additional fine-tuning. We additionally show that the trained encoder provides an image embedding, associated only with its color style. The presented method is capable of processing 4K images and achieves state-of-the-art performance in terms of content and style similarity.
