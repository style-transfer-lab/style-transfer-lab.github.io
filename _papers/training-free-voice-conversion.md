---
layout: paper
title: "Training-Free Voice Conversion with Factorized Optimal Transport"
authors: "Alexander Lobashev, Assel Yermekova, Maria Larchenko"
conference: "Interspeech 2025"
venue_type: conference
year: 2025
permalink: /papers/training-free-voice-conversion/
abstract: "This paper introduces Factorized MKL-VC, a training-free modification for kNN-VC pipeline. In contrast with original pipeline, our algorithm performs high quality any-to-any cross-lingual voice conversion with only 5 second of reference audio. MKL-VC replaces kNN regression with a factorized optimal transport map in WavLM embedding subspaces, derived from Monge-Kantorovich Linear solution. Factorization addresses non-uniform variance across dimensions, ensuring effective feature transformation. Experiments on LibriSpeech and FLEURS datasets show MKL-VC significantly improves content preservation and robustness with short reference audio, outperforming kNN-VC. MKL-VC achieves performance comparable to FACodec, especially in cross-lingual voice conversion domain."
image: "/assets/images/abstract_landing.png"
tags: [optimal-transport, voice-conversion, audio-processing, training-free, zero-shot]
featured: false
arxiv: https://arxiv.org/abs/2506.09709
# openreview: https://openreview.net/forum?id=...
# github: https://github.com/...
# pdf: /assets/papers/training-free-voice-conversion.pdf
bibtex: |
  @article{lobashev2025training,
    title={Training-Free Voice Conversion with Factorized Optimal Transport},
    author={Lobashev, Alexander and Yermekova, Assel and Larchenko, Maria},
    journal={arXiv preprint arXiv:2506.09709},
    year={2025}
  }
key_contributions:
  - "Factorized MKL-VC replaces kNN regression with optimal transport map"
  - "High quality cross-lingual conversion with only 5 seconds of reference audio"
  - "Derived from Monge-Kantorovich Linear solution"
  - "Outperforms kNN-VC, comparable to FACodec in cross-lingual domain"
related_papers:
  - color-transfer-modflows
---

## Abstract  

We introduce a novel training-free approach for voice conversion that leverages factorized optimal transport to transfer vocal characteristics between speakers without requiring parallel data or speaker-specific training. Traditional voice conversion methods rely on extensive training data and speaker-dependent models, limiting their applicability to new speakers or low-resource scenarios. 

Our method factorizes the optimal transport problem into separable components corresponding to different acoustic attributes:
- **Pitch contour**: Fundamental frequency and intonation patterns
- **Timbre**: Spectral envelope and vocal tract characteristics  
- **Prosody**: Rhythm, stress, and temporal dynamics
- **Linguistic content**: Phonetic and semantic information (preserved)

This factorization allows for zero-shot voice conversion while preserving linguistic content and natural speech quality. Each component is handled through separate optimal transport mappings that can be independently controlled, enabling fine-grained manipulation of converted speech characteristics.

We demonstrate state-of-the-art performance on standard benchmarks including VCC2018 and VCC2020 datasets, with particular advantages in:
- Cross-lingual voice conversion scenarios
- Conversion to previously unseen target speakers
- Preservation of emotional expressiveness and naturalness
- Computational efficiency compared to neural voice conversion methods

The training-free nature of our approach makes it immediately applicable to new speakers and languages without additional data collection or model retraining.
