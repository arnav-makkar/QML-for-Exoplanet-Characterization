# QML for Exoplanet Characterization
Early Experiments for EXXA GSoC '25 @ ML4SCI

This repository documents initial experiments conducted to explore the feasibility of Quantum Machine Learning (QML) methods for scientific data modeling.  
The goal is to build familiarity with Qiskit, TorchConnector, quantum circuit design, and training hybrid quantum-classical models ahead of the main project work.

➡️ [GSoC Proposal Link](https://drive.google.com/file/d/1dO6XMyig0qGGis_iXVehzV9MI89aAuGf/view?usp=sharing)  
➡️ [EXXA Evaluation Tests](https://github.com/arnav-makkar/EXXA-Evaluation-Test)  
➡️ [Official Project Description](https://ml4sci.org/gsoc/2025/proposal_EXXA5.html)

---

## Summary of Experiments

### Quantum Autoencoder (QAE)
- **Phase 1**: Learned to compress random 2D points via a 2-qubit circuit
- **Phase 2**: Applied QAE to downsampled MNIST (16×16), successfully reconstructed digits from quantum-compressed latent representations

### Quantum GAN (QGAN)
- **Phase 1**: Generated sine wave samples using a 2-qubit generator vs real continuous data
- **Phase 2**: Trained QGAN on PCA-reduced MNIST vectors, then reconstructed images via inverse PCA (FID ≈ 0.65)

### Quantum Regression (QNN)
- **Phase 1**: Regressed on toy functions (noisy bell curve, piecewise step) with 1-qubit QNN + MLP
- **Phase 2**: Applied 4-qubit QNN to the diabetes progression dataset, achieving R² ≈ 0.57

---

## Stack & Tools
- **Quantum ML**: Qiskit, EstimatorQNN, TorchConnector  
- **Classical ML**: PyTorch, PCA, scikit-learn  
- **Data**: MNIST, diabetes dataset, synthetic math functions

---

## Purpose

These prototype models are stepping stones toward the main GSoC goal:  
> **Using QAE and QGAN architectures to model, compress, and generate latent representations of exoplanet transmission spectra.**

They validate that:
- Quantum circuits can learn useful latent structures
- Hybrid models can generalize to real data
- The proposed techniques are viable and reproducible with limited qubit counts

---

> ✅ All results are visualized, explained, and reproducible.  
> ✅ Demonstrate core concepts required for the full GSoC project.