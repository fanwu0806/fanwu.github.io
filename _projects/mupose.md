---
layout: default
title: Improving Mushroom Pose Estimation with Synthetic Data Scaling and Multi-View Attention Fusion
image: /assets/img/synmu.png
order: 2
---

<div style="text-align:center; margin-top:20px; margin-bottom:30px;">
  <img src="/assets/img/synmu.png" alt="Multiview mushroom pose estimation"
       style="width:100%; max-width:950px; border-radius:14px; box-shadow:0 6px 18px rgba(0,0,0,0.12);">
</div>
<div style="text-align:center; margin-bottom:28px;">
  <h1 style="margin-bottom:10px;">Improving Mushroom Pose Estimation with Synthetic Data Scaling and Multi-View Attention Fusion</h1>
</div>


---

## Overview

<div style="background:#f8fafc; padding:22px; border-radius:12px; box-shadow:0 3px 10px rgba(0,0,0,0.06); margin-bottom:24px;">
Automating mushroom harvesting remains a key challenge due to labor-intensive phenotypic analysis, delicate handling requirements, and the difficulty of obtaining large-scale annotated datasets under low-light, high-humidity environments. This work proposes a synthetic-to-real pipeline for mushroom detection and 3D pose estimation relying on large-scale synthetic data with minimal manual annotation, enabling efficient and damage-free robotic harvesting. After generating synthetic images in blender, a domain adaption method is ultilized to bridge its gap with real images. After that, a transformer-based multiview fusion network, combining lightweight visual encoders with camera pose embeddings, predicts key geometric parameters—bottom center, top center, and maximum radius—from four top-view images. Extensive experiments using both synthetic and real-world datasets demonstrate that our approach achieves millimeter-level pose estimation accuracy, significantly outperforming conventional end-to-end baselines. The resulting system enables precise robotic grasp planning for autonomous mushroom harvesting, offering a scalable solution for data-limited agricultural environments.
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



---


## Method Pipeline

<div style="background:#f8fafc; padding:22px; border-radius:12px; box-shadow:0 3px 10px rgba(0,0,0,0.06); margin-bottom:24px;">
1. **Synthetic scene generation:** Realistic mushroom plantation scenes are created in Blender with controllable variations in shape, pose, density, and illumination.
2. **Domain adaptation:** Synthetic images are translated toward real visual appearance to narrow the sim-to-real gap.
3. **Multi-view acquisition:** Multiple top-view images and corresponding camera pose information are collected for each mushroom instance.
4. **Pose estimation:** A learning-based fusion model predicts key geometric attributes required for harvesting-oriented perception.
</div>


<div style="text-align:center; margin:26px 0;">
  <img src="/assets/img/samogeying.png" alt="MIR3D pipeline"
       style="width:100%; max-width:900px; border-radius:12px; box-shadow:0 6px 16px rgba(0,0,0,0.10);">
  <p style="color:#666; margin-top:10px;"><em>Figure: Overall pipeline of MIR3D.</em></p>
</div>


---


## Results

Preliminary experiments show that the proposed framework improves pose estimation performance compared with simpler baselines, while maintaining strong potential for robotic harvesting applications. In particular, multi-view fusion and synthetic data scaling both contribute to better robustness in real cultivation scenes. These results suggest that simulation-driven perception is a practical direction for scalable mushroom harvesting automation.
