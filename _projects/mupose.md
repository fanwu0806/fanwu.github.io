---
layout: default
title: Improving Mushroom Pose Estimation with Synthetic Data Scaling and Multi-View Attention Fusion
image: /assets/img/synmu2.png
order: 2
---

<div style="text-align:center; margin-top:20px; margin-bottom:30px;">
  <img src="/assets/img/synmu2.png" alt="Multiview mushroom pose estimation"
       style="width:100%; max-width:950px; border-radius:14px; box-shadow:0 6px 18px rgba(0,0,0,0.12);">
</div>
<div style="text-align:center; margin-bottom:28px;">
  <h1 style="margin-bottom:10px;">Improving Mushroom Pose Estimation with Synthetic Data Scaling and Multi-View Attention Fusion</h1>
</div>


---

## Overview

<div style="background:#f8fafc; padding:22px; border-radius:12px; box-shadow:0 3px 10px rgba(0,0,0,0.06); margin-bottom:24px;">
Automating mushroom harvesting remains a key challenge due to labor-intensive phenotypic analysis, delicate handling requirements, and the difficulty of obtaining large-scale annotated datasets under low-light, high-humidity environments. This work presents a synthetic-to-real pipeline for mushroom detection and 3D pose estimation using scalable synthetic data with minimal manual annotation. After generating synthetic images in Blender, a domain adaptation strategy is applied to reduce the visual gap between synthetic and real cultivation scenes. A transformer-based multi-view fusion network then combines lightweight visual features with camera pose embeddings to estimate key geometric parameters, including bottom center, top center, and maximum radius, from four top-view images. The system is designed to support precise robotic grasp planning for autonomous mushroom harvesting in data-limited agricultural environments.
</div>

---

## Key Highlights

<div style="display:grid; grid-template-columns:repeat(auto-fit, minmax(220px, 1fr)); gap:16px; margin-bottom:28px;">

  <div style="background:white; border:1px solid #e5e7eb; border-radius:12px; padding:18px; box-shadow:0 3px 8px rgba(0,0,0,0.04);">
    <h4>Synthetic-to-Real Learning</h4>
    <p style="margin-bottom:0;">Build scalable training data in simulation and transfer it to real mushroom cultivation scenes with reduced annotation effort.</p>
  </div>

  <div style="background:white; border:1px solid #e5e7eb; border-radius:12px; padding:18px; box-shadow:0 3px 8px rgba(0,0,0,0.04);">
    <h4>Multi-View Geometry Estimation</h4>
    <p style="margin-bottom:0;">Fuse multiple top-view observations and camera poses to estimate grasp-oriented mushroom geometry under occlusion and dense growth.</p>
  </div>

  <div style="background:white; border:1px solid #e5e7eb; border-radius:12px; padding:18px; box-shadow:0 3px 8px rgba(0,0,0,0.04);">
    <h4>Robotic Harvesting Interface</h4>
    <p style="margin-bottom:0;">Provide pose-related outputs that can support downstream grasp planning and autonomous harvesting with robotic systems.</p>
  </div>

</div>

---

## Method Pipeline

<div style="background:#f8fafc; padding:22px; border-radius:12px; box-shadow:0 3px 10px rgba(0,0,0,0.06); margin-bottom:24px;">
  <ol style="margin:0; padding-left:20px;">
    <li><strong>Synthetic scene generation:</strong> Realistic mushroom plantation scenes are created in Blender with controllable variations in shape, pose, density, and illumination.</li>
    <li><strong>Domain adaptation:</strong> Synthetic images are translated toward real visual appearance to narrow the sim-to-real gap.</li>
    <li><strong>Multi-view acquisition:</strong> Multiple top-view images and corresponding camera pose information are collected for each mushroom instance.</li>
    <li><strong>Pose estimation:</strong> A learning-based fusion model predicts key geometric attributes required for harvesting-oriented perception.</li>
  </ol>
</div>

<div style="text-align:center; margin:26px 0;">
  <img src="/assets/img/samogeying2.png" alt="samogeying"
       style="width:80%; max-width:900px; border-radius:12px; box-shadow:0 6px 16px rgba(0,0,0,0.10);">
  <p style="color:#666; margin-top:10px;"><em>Figure1: Overview of the robotic multi-view imaging platform used for mushroom data acquisition. The system integrates a UR5e robotic arm, multi-view RGB cameras, Raspberry Pi control unit, and LED illumination to capture structured observations of mushroom cultivation scenes.</em></p>
</div>


<div style="text-align:center; margin:26px 0;">
  <img src="/assets/img/samogedata.png" alt="samogedata"
       style="width:80%; max-width:900px; border-radius:12px; box-shadow:0 6px 16px rgba(0,0,0,0.10);">
  <p style="color:#666; margin-top:10px;"><em>Figure2: Analysis of the synthetic-to-real training pipeline. Top: training error convergence and error decomposition across different pose parameters. Bottom: feature distribution visualization using t-SNE and PCA density alignment, illustrating the relationship between synthetic and real domains. </em></p>
</div>


---

## Results

Preliminary experiments show that the proposed framework improves pose estimation performance over simpler baselines while maintaining strong potential for robotic harvesting applications. In particular, multi-view fusion and synthetic data scaling contribute to better robustness in real cultivation scenes. These results suggest that simulation-driven perception is a practical direction for scalable mushroom harvesting automation.

