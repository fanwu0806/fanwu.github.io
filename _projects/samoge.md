---
layout: default
title: Monocular infrared imaging for high-throughput time-series phenotyping and instance-level growth modeling of mushrooms
image: /assets/img/mir3d.png
order: 1
---

<div style="text-align:center; margin-bottom:28px;">
  <h1 style="margin-bottom:10px;">Monocular infrared imaging for high-throughput time-series phenotyping and instance-level growth modeling of mushrooms</h1>
</div>


---

## Overview

<div style="background:#f8fafc; padding:22px; border-radius:12px; box-shadow:0 3px 10px rgba(0,0,0,0.06); margin-bottom:24px;">
Understanding mushroom growth dynamics is essential for precision cultivation and automated harvesting. However, monitoring mushroom phenotypes in real farms remains challenging due to extremely low-light environments, dense growth patterns, and the lack of large-scale annotated datasets for 3D geometry reconstruction. 

This project presents a monocular infrared-based pipeline for mushroom growth modeling using segmentation and geometry estimation. First, mushroom instances are segmented from infrared images using a YOLO-assisted SAM2 framework to obtain precise object boundaries under dense canopy conditions. Then, an optimized MoGe2 model is applied to estimate dense depth maps from monocular infrared observations. By combining segmentation masks with geometry estimation, the system reconstructs key 3D phenotypic attributes of each mushroom, including height, projected area, and geometric structure. 

The framework further analyzes time-series observations to model mushroom growth dynamics and extract biologically meaningful growth curves. Experimental results demonstrate that the proposed approach enables reliable phenotyping and geometry estimation for mushrooms under challenging dark cultivation environments, providing a scalable solution for automated mushroom monitoring.
</div>


---

## Key Highlights

<div style="display:grid; grid-template-columns:repeat(auto-fit, minmax(220px, 1fr)); gap:16px; margin-bottom:28px;">

  <div style="background:white; border:1px solid #e5e7eb; border-radius:12px; padding:18px; box-shadow:0 3px 8px rgba(0,0,0,0.04);">
    <h4>Infrared Mushroom Monitoring</h4>
    <p style="margin-bottom:0;">A monocular infrared imaging system enables reliable mushroom observation in completely dark and humid cultivation environments.</p>
  </div>

  <div style="background:white; border:1px solid #e5e7eb; border-radius:12px; padding:18px; box-shadow:0 3px 8px rgba(0,0,0,0.04);">
    <h4>SAM2-Based Instance Segmentation</h4>
    <p style="margin-bottom:0;">A YOLO-assisted SAM2 framework provides accurate instance segmentation for dense mushroom clusters with precise boundary refinement.</p>
  </div>

  <div style="background:white; border:1px solid #e5e7eb; border-radius:12px; padding:18px; box-shadow:0 3px 8px rgba(0,0,0,0.04);">
    <h4>Monocular Geometry Estimation</h4>
    <p style="margin-bottom:0;">An optimized MoGe2 model reconstructs dense depth maps from monocular infrared images, enabling 3D mushroom geometry estimation without multi-view sensors.</p>
  </div>

  <div style="background:white; border:1px solid #e5e7eb; border-radius:12px; padding:18px; box-shadow:0 3px 8px rgba(0,0,0,0.04);">
    <h4>Time-Series Growth Modeling</h4>
    <p style="margin-bottom:0;">Continuous time-lapse observations allow quantitative analysis of mushroom growth dynamics, including height evolution and canopy expansion.</p>
  </div>

</div>

---

## Method Pipeline

<div style="background:#f8fafc; padding:22px; border-radius:12px; box-shadow:0 3px 10px rgba(0,0,0,0.06); margin-bottom:24px;">
  <ol style="margin:0; padding-left:20px;">
    <li><strong>Infrared image acquisition:</strong> Time-lapse infrared images are captured from a fixed top-view camera in a mushroom cultivation environment.</li>
    <li><strong>Mushroom instance segmentation:</strong> YOLO detection provides coarse localization, while SAM2 refines segmentation masks to extract accurate mushroom boundaries.</li>
    <li><strong>Monocular depth estimation:</strong> An optimized MoGe2 model predicts dense depth maps from infrared images to recover geometric structure.</li>
    <li><strong>3D phenotype extraction:</strong> Segmentation masks and depth maps are fused to compute mushroom geometric attributes such as height and projected area.</li>
    <li><strong>Growth curve modeling:</strong> Time-series observations are analyzed to construct mushroom growth curves and quantify developmental patterns.</li>
  </ol>
</div>



<h3 style="margin-top:36px;">Time-Series Segmentation and Depth Estimation</h3>

<div style="text-align:center; margin:26px 0;">
  <img src="/assets/img/mushroom_time_series_seg_depth.png" 
       alt="Time-Series Segmentation and Depth Estimation"
       style="width:92%; max-width:1200px; border-radius:12px; box-shadow:0 6px 16px rgba(0,0,0,0.10);">
  <p style="color:#666; margin-top:10px; line-height:1.6;">
    <em>Figure 1: Time-series visualization of mushroom growth, instance segmentation, and depth estimation under infrared imaging. From top to bottom: raw infrared observations, segmentation results, and estimated depth maps across different growth stages.</em>
  </p>
</div>


<h3 style="margin-top:36px;">Imaging Conditions Comparison</h3>

<div style="text-align:center; margin:26px 0;">
  <img src="/assets/img/imaging_condition_comparison.png" 
       alt="Imaging Conditions Comparison"
       style="width:92%; max-width:1400px; border-radius:12px; box-shadow:0 6px 16px rgba(0,0,0,0.10);">
  <p style="color:#666; margin-top:10px; line-height:1.6;">
    <em>Figure 2: Comparison of mushroom imaging under different lighting conditions, including normal RGB illumination, dark-environment RGB, infrared imaging with 20% IR intensity, and infrared imaging with 100% IR intensity.</em>
  </p>
</div>

<h3 style="margin-top:36px;">Single-Mushroom Growth Curve</h3>

<div style="text-align:center; margin:26px 0;">
  <img src="/assets/img/single_mushroom_growth_curve.png" 
       alt="Single-Mushroom Growth Curve"
       style="width:64%; max-width:1100px; border-radius:12px; box-shadow:0 6px 16px rgba(0,0,0,0.10);">
  <p style="color:#666; margin-top:10px; line-height:1.6;">
    <em>Figure 3: Time-series growth analysis of a single mushroom, showing the evolution of projected area, cap surface area, and height across developmental stages.</em>
  </p>
</div>


<h3 style="margin-top:36px;">3D Reconstruction of Mushroom Cultivation Scene</h3>

<div style="text-align:center; margin:26px 0;">
  <img src="/assets/img/mushroom_scene_3d_reconstruction.png" 
       alt="3D Reconstruction of Mushroom Cultivation Scene"
       style="width:92%; max-width:1200px; border-radius:12px; box-shadow:0 6px 16px rgba(0,0,0,0.10);">
  <p style="color:#666; margin-top:10px; line-height:1.6;">
    <em>Figure 4: Visualization of 3D reconstruction results for a mushroom cultivation scene across different growth stages. Colored mushroom surfaces indicate individual segmented instances reconstructed from monocular infrared geometry estimation.</em>
  </p>
</div>



---

## Results

Preliminary experiments demonstrate that the proposed framework enables reliable mushroom phenotyping in dark cultivation environments using monocular infrared imaging. The YOLO-assisted SAM2 segmentation framework produces precise instance masks for densely clustered mushrooms, while the optimized MoGe2 model provides accurate depth estimation from single-view infrared images. 

By integrating segmentation and geometry estimation, the system can automatically extract mushroom height and canopy expansion over time, enabling quantitative analysis of growth dynamics. The results suggest that monocular infrared geometry estimation offers a practical and scalable approach for automated mushroom monitoring in real-world agricultural environments.

