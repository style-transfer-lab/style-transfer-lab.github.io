---
layout: paper
title: "Lightweight Optimal-Transport Harmonization on Edge Devices"
authors: "Maria Larchenko, Dmitry Guskov, Alexander Lobashev, Georgy Derevyanko"
conference: "AAAI 2026 (Oral)"
venue_type: conference
year: 2026
permalink: /papers/lightweight-optimal-transport-harmonization/
abstract: "Color harmonization adjusts the colors of an inserted object so that it perceptually matches the surrounding image, resulting in a seamless composite. The harmonization problem naturally arises in augmented reality (AR), yet harmonization algorithms are not currently integrated into AR pipelines because real-time solutions are scarce. In this work, we address color harmonization for AR by proposing a lightweight approach that supports on-device inference. For this, we leverage classical optimal transport theory by training a compact encoder to predict the Monge-Kantorovich transport map. We benchmark our MKL-Harmonizer algorithm against state-of-the-art methods and demonstrate that for real composite AR images our method achieves the best aggregated score. We release our dedicated AR dataset of composite images with pixel-accurate masks and data-gathering toolkit to support further data acquisition by researchers."
image: "/assets/images/modflows_results.jpg"
tags: [optimal-transport, edge-computing, mobile-ai, color-transfer, efficiency]
featured: false
arxiv: https://arxiv.org/abs/2511.12785
# openreview: https://openreview.net/forum?id=...
# github: https://github.com/...
# pdf: /assets/papers/lightweight-optimal-transport-harmonization.pdf
bibtex: |
  @article{larchenko2025lightweight,
    title={Lightweight Optimal-Transport Harmonization on Edge Devices},
    author={Larchenko, Maria and Guskov, Dmitry and Lobashev, Alexander and Derevyanko, Georgy},
    journal={arXiv preprint arXiv:2511.12785},
    year={2025}
  }
key_contributions:
  - "Lightweight approach for AR color harmonization with on-device inference"
  - "Leverages Monge-Kantorovich transport map via compact encoder"
  - "Best aggregated score on real composite AR images"
  - "Includes dedicated AR dataset with pixel-accurate masks and toolkit"
related_papers:
  - color-transfer-modflows
---

## Abstract  

We present a lightweight optimal transport framework for image harmonization that can run efficiently on edge devices with limited computational resources. Traditional optimal transport methods for color and style harmonization require significant memory and processing power, limiting their deployment on mobile and embedded systems. 

Our approach introduces novel approximations and efficient algorithmic strategies that reduce computational complexity while maintaining high-quality harmonization results. Key innovations include:
- Adaptive spatial downsampling based on local complexity
- Fast approximate solvers for the optimal transport problem
- Memory-efficient data structures for real-time processing
- GPU acceleration strategies optimized for mobile architectures

We demonstrate real-time performance on smartphones and IoT devices, enabling practical applications in mobile photography, augmented reality, and edge-based creative tools. Extensive experiments show that our method achieves comparable quality to full optimal transport solvers while being 10-100× faster and requiring significantly less memory, making high-quality image harmonization accessible on resource-constrained devices.
