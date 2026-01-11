---
layout: paper
title: "Lightweight Optimal-Transport Harmonization on Edge Devices"
authors: "Maria Larchenko, Dmitry Guskov, Alexander Lobashev, Grigory Derevyanko"
conference: "Under Review"
venue_type: preprint
year: 2025
permalink: /papers/lightweight-optimal-transport-harmonization/
abstract: "We present a lightweight optimal transport framework for image harmonization that can run efficiently on edge devices with limited computational resources. Traditional optimal transport methods for color and style harmonization require significant memory and processing power, limiting their deployment on mobile and embedded systems. Our approach introduces novel approximations and efficient algorithmic strategies that reduce computational complexity while maintaining high-quality harmonization results. We demonstrate real-time performance on smartphones and IoT devices, enabling practical applications in mobile photography, augmented reality, and edge-based creative tools. Extensive experiments show that our method achieves comparable quality to full optimal transport solvers while being 10-100× faster and requiring significantly less memory."
image: "/assets/images/modflows_results.jpg"
tags: [optimal-transport, edge-computing, mobile-ai, color-transfer, efficiency]
featured: false
# Add your links below (remove # to activate):
# arxiv: https://arxiv.org/abs/...
# openreview: https://openreview.net/forum?id=...
# github: https://github.com/...
# pdf: /assets/papers/lightweight-optimal-transport-harmonization.pdf
bibtex: |
  @article{larchenko2025lightweight,
    title={Lightweight Optimal-Transport Harmonization on Edge Devices},
    author={Larchenko, Maria and Guskov, Dmitry and Lobashev, Alexander and Derevyanko, Grigory},
    journal={arXiv preprint},
    year={2025}
  }
key_contributions:
  - "Efficient optimal transport approximations for edge devices"
  - "Real-time image harmonization on mobile and IoT platforms"
  - "10-100× speedup compared to standard optimal transport solvers"
  - "Maintains high quality while reducing memory footprint significantly"
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
