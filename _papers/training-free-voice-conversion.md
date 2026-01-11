---
layout: paper
title: "Training-Free Voice Conversion with Factorized Optimal Transport"
authors: "Alexander Lobashev, Aizhan Yermekova, Maria Larchenko"
conference: "Under Review"
venue_type: preprint
year: 2025
permalink: /papers/training-free-voice-conversion/
abstract: "We introduce a novel training-free approach for voice conversion that leverages factorized optimal transport to transfer vocal characteristics between speakers without requiring parallel data or speaker-specific training. Traditional voice conversion methods rely on extensive training data and speaker-dependent models, limiting their applicability to new speakers or low-resource scenarios. Our method factorizes the optimal transport problem into separable components corresponding to different acoustic attributes (pitch, timbre, prosody), enabling fine-grained control over the conversion process. This factorization allows for zero-shot voice conversion while preserving linguistic content and natural speech quality. We demonstrate state-of-the-art performance on standard benchmarks, with particular advantages in cross-lingual scenarios and conversion to previously unseen target speakers."
image: "/assets/images/abstract_landing.png"
tags: [optimal-transport, voice-conversion, audio-processing, training-free, zero-shot]
featured: false
# Add your links below (remove # to activate):
# arxiv: https://arxiv.org/abs/...
# openreview: https://openreview.net/forum?id=...
# github: https://github.com/...
# pdf: /assets/papers/training-free-voice-conversion.pdf
bibtex: |
  @article{lobashev2025voiceconversion,
    title={Training-Free Voice Conversion with Factorized Optimal Transport},
    author={Lobashev, Alexander and Yermekova, Aizhan and Larchenko, Maria},
    journal={arXiv preprint},
    year={2025}
  }
key_contributions:
  - "Training-free voice conversion using factorized optimal transport"
  - "Zero-shot conversion to unseen target speakers"
  - "Factorized control over pitch, timbre, and prosody"
  - "State-of-the-art performance without parallel training data"
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
