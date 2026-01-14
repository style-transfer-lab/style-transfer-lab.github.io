---
title: Open Source Projects
layout: page
permalink: /open-source/
---

## Our Commitment to Open Research

At Style Transfer Lab, we believe in open science and reproducible research. All our published work is accompanied by open-source implementations, enabling the research community to build upon our contributions. We actively maintain our codebases and welcome contributions from the community.

---

## Featured Projects

<div style="display: grid; gap: 30px; margin: 40px 0;">

<!-- Project 1: Hessian Geometry -->
<div style="background: white; padding: 30px; border-radius: 12px; box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08); border-left: 4px solid #2196F3;">
  <h3 style="margin-top: 0; color: #212121;">
    <a href="https://github.com/alobashev/hessian-geometry-of-diffusion-models" target="_blank" style="color: #2196F3; text-decoration: none;">
      🔬 Hessian Geometry of Diffusion Models
    </a>
  </h3>
  
  <p style="color: #757575; margin-bottom: 15px;">
    Implementation of our ICML 2025 paper on analyzing latent space geometry of generative models through Fisher information metrics. Reveals fractal phase transitions and geometric structures in diffusion model latent spaces.
  </p>
  
  <div style="display: flex; gap: 15px; margin-bottom: 15px; flex-wrap: wrap;">
    <span style="background: #E3F2FD; color: #1976D2; padding: 4px 12px; border-radius: 16px; font-size: 0.85em;">Python</span>
    <span style="background: #E3F2FD; color: #1976D2; padding: 4px 12px; border-radius: 16px; font-size: 0.85em;">PyTorch</span>
    <span style="background: #E3F2FD; color: #1976D2; padding: 4px 12px; border-radius: 16px; font-size: 0.85em;">Diffusion Models</span>
  </div>
  
  <div style="display: flex; gap: 12px; font-size: 0.9em;">
    <a href="https://github.com/alobashev/hessian-geometry-of-diffusion-models" target="_blank" style="color: #24292e; text-decoration: none;">💻 GitHub</a>
    <a href="https://arxiv.org/abs/2506.10632" target="_blank" style="color: #5E35B1; text-decoration: none;">📄 Paper</a>
  </div>
</div>

<!-- Project 2: SW-Guidance -->
<div style="background: white; padding: 30px; border-radius: 12px; box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08); border-left: 4px solid #9C27B0;">
  <h3 style="margin-top: 0; color: #212121;">
    <a href="https://github.com/alobashev/sw-guidance" target="_blank" style="color: #9C27B0; text-decoration: none;">
      🎨 SW-Guidance: Color Conditional Generation
    </a>
  </h3>
  
  <p style="color: #757575; margin-bottom: 15px;">
    Training-free color-conditional image generation using Sliced Wasserstein distance. From our NeurIPS 2025 (Spotlight) paper. Enables semantic color control in diffusion models without retraining.
  </p>
  
  <div style="display: flex; gap: 15px; margin-bottom: 15px; flex-wrap: wrap;">
    <span style="background: #F3E5F5; color: #7B1FA2; padding: 4px 12px; border-radius: 16px; font-size: 0.85em;">Python</span>
    <span style="background: #F3E5F5; color: #7B1FA2; padding: 4px 12px; border-radius: 16px; font-size: 0.85em;">Stable Diffusion</span>
    <span style="background: #F3E5F5; color: #7B1FA2; padding: 4px 12px; border-radius: 16px; font-size: 0.85em;">Optimal Transport</span>
  </div>
  
  <div style="display: flex; gap: 12px; font-size: 0.9em;">
    <a href="https://github.com/alobashev/sw-guidance" target="_blank" style="color: #24292e; text-decoration: none;">💻 GitHub</a>
    <a href="https://arxiv.org/abs/2503.19034" target="_blank" style="color: #5E35B1; text-decoration: none;">📄 Paper</a>
  </div>
</div>

<!-- Additional Projects Section -->
<div style="background: linear-gradient(135deg, rgba(33, 150, 243, 0.05) 0%, rgba(156, 39, 176, 0.05) 100%); padding: 30px; border-radius: 12px;">
  <h3 style="margin-top: 0; color: #212121;">Other Repositories</h3>
  <p style="color: #757575; margin-bottom: 20px;">
    We're continuously releasing code for our publications. Check back soon for implementations of:
  </p>
  <ul style="color: #616161; line-height: 1.8;">
    <li>ModFlows: Color Transfer with Modulated Flows (AAAI 2025)</li>
    <li>MKL-VC: Training-Free Voice Conversion (Interspeech 2025)</li>
    <li>MKL-Harmonizer: Lightweight Optimal Transport for AR (AAAI 2026)</li>
    <li>fBm-based Generative Inpainting for Biological Data</li>
  </ul>
</div>

</div>

---

## Contributing

We welcome contributions from the community! If you're interested in:
- 🐛 Reporting bugs or issues
- 💡 Suggesting new features
- 📝 Improving documentation
- 🔧 Contributing code

Please open an issue or pull request on the respective GitHub repository. We aim to respond to all contributions within a few days.

---

## Code Quality & Standards

All our repositories follow best practices:
- ✅ Clean, documented code
- ✅ Reproducible experiments with seed control
- ✅ Requirements files for easy setup
- ✅ Example scripts and Jupyter notebooks
- ✅ MIT or Apache 2.0 licensing

---

## Research Reproducibility

Each repository includes:
- **Pretrained Models**: Downloadable weights for published results
- **Configuration Files**: Exact hyperparameters used in papers
- **Evaluation Scripts**: Reproduce metrics from our publications
- **Datasets**: Links to data or scripts to generate datasets

---

## Citation

If you use our code in your research, please cite the corresponding paper. BibTeX citations are available on each [research paper page](/papers/) and in the repository README files.

---

<div style="text-align: center; margin: 60px 0; padding: 40px; background: white; border-radius: 12px; box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);">
  <h3 style="margin-top: 0;">Questions or Collaboration Ideas?</h3>
  <p style="color: #757575; margin-bottom: 25px;">
    We're always interested in discussing research ideas and potential collaborations.
  </p>
  <a href="/about/#contact" class="btn-primary">Get in Touch →</a>
</div>
