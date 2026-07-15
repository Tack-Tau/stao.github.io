---
layout: single
title: "Research"
permalink: /research/
author_profile: true
---

Our research develops computational and machine-learning methods to accelerate the discovery of novel materials. We combine first-principles calculations, crystal structure prediction algorithms, and deep learning architectures to tackle problems in materials science that are intractable with conventional approaches.

---

## Machine Learning for Materials Discovery

<img src="{{ site.baseurl }}/images/EOSnet_TOC.png" alt="EOSnet schematic" style="max-width: 100%; margin: 20px 0;">

We developed **EOSnet** (Embedded Overlap Structures for Graph Neural Networks), a graph neural network that incorporates Gaussian Overlap Matrix (GOM) fingerprints to capture many-body atomic interactions. Unlike conventional atom-feature-based GNNs, EOSnet encodes the local geometric environment of each atom through overlap integrals of Gaussian-type orbitals placed on neighboring sites, providing a physically motivated and rotationally invariant representation.

EOSnet achieves state-of-the-art accuracy in predicting bandgaps and classifying band characteristics (direct vs. indirect) across diverse crystal structures, while significantly reducing the computational cost of high-throughput screening. We successfully applied EOSnet to accelerate the search for direct-gap Si--Ge alloys via binary atomic substitution in known Si allotropes.

**Related publications:**
- S. Tao and L. Zhu, *J. Phys. Chem. Lett.* **16**, 717 (2025)
- S. Tao and L. Zhu, *Comput. Mater. Today* **9**, 100045 (2025)

---

## Symmetry-Biased Structural Optimization

<img src="{{ site.baseurl }}/images/ReformPy_PES_Bias_sketch.png" alt="ReformPy PES mixing" style="max-width: 100%; margin: 20px 0;">

Identifying the global minimum structure among a vast number of local minima on the potential energy surface (PES) is a central challenge in computational materials discovery. We developed **ReformPy**, a symmetry-biased PES framework that mixes the real PES with a fingerprint-based energy term. This mixed PES lowers the high-energy barriers that conventional relaxation methods struggle to overcome, enabling efficient escape from local minima and navigation toward the global minimum.

ReformPy has demonstrated significant improvements in both efficiency and accuracy when applied to Lennard-Jones clusters, silicon carbide, and other complex systems.

**Related publications:**
- S. Tao, X. Shao, and L. Zhu, *J. Phys. Chem. Lett.* **15**, 3185 (2024)

---

## Generative Models for Materials Screening

<img src="{{ site.baseurl }}/images/ElectrideFlow_Workflow.png" alt="ElectrideFlow workflow" style="max-width: 100%; margin: 20px 0;">

We developed **ElectrideFlow**, a generative-model-based framework for accelerated discovery of inorganic electrides -- materials where electrons serve as anions. ElectrideFlow combines crystal structure generation with hierarchical screening to efficiently identify candidate electrides from a vast chemical space, drastically reducing the computational cost compared to exhaustive first-principles searches.

**Related publications:**
- S. Tao and Q. Zhu, *PRX Intelligence* (2026, under revision) [arXiv:2601.21077]

---

## Future Directions: Large Language Model for Molecular Crystals

We are building toward a next-generation **Large Language Model for Molecular Crystals (LLM4MC)** through three interconnected research thrusts:

1. **MCGen -- Molecular Crystal Generative Model.** We plan to advance the current OXTAL architecture by replacing all-atom diffusion + Pariformer with flow matching + E(3)-equivariant GNN, and introducing fingerprint energy denoising constraints in classifier-free guidance to improve generation quality and physical validity.

2. **LMCD -- Large Molecular Crystal Database.** We will construct a high-precision, high-fidelity database by (i) generating and prescreening molecular crystals with state-of-the-art generative models (OXTAL/CLARI) followed by MLIP relaxation (GPUMD/MatterSim), and (ii) computing formation enthalpies, activation energy barriers, and phonon spectra at the DFT level to identify meta-stable material candidates.

3. **High-Accuracy MLIP for Molecular Crystals.** Building on our EOSnet framework, we aim to develop machine-learning interatomic potentials capable of million-atom molecular dynamics simulations with DFT-level accuracy, enabling the study of large-scale phenomena in molecular crystal systems.
