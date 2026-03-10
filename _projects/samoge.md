---
layout: default
title: MIR3D for Autonomous Robotic Mushroom Harvesting
image: /assets/img/mir3d.png
order: 1
excerpt: Monocular infrared geometry estimation for robotic mushroom harvesting in dark environments.
---

<div style="text-align:center; margin-top:20px; margin-bottom:30px;">
  <img src="/assets/img/mir3d.png" alt="MIR3D preview"
       style="width:100%; max-width:950px; border-radius:14px; box-shadow:0 6px 18px rgba(0,0,0,0.12);">
</div>

<div style="text-align:center; margin-bottom:28px;">
  <h1 style="margin-bottom:10px;">MIR3D for Autonomous Robotic Mushroom Harvesting</h1>
  <p style="font-size:1.08rem; color:#555; max-width:850px; margin:0 auto;">
    A monocular infrared geometry estimation framework for perception-driven robotic mushroom harvesting
    in dark cultivation environments.
  </p>
</div>

<div style="text-align:center; margin-bottom:36px;">
  <a href="#" target="_blank"
     style="display:inline-block; margin:6px; padding:10px 20px; border-radius:8px; background:#2c5f8a; color:white; text-decoration:none; font-weight:600;">
     Paper
  </a>
  <a href="#" target="_blank"
     style="display:inline-block; margin:6px; padding:10px 20px; border-radius:8px; background:#2aa198; color:white; text-decoration:none; font-weight:600;">
     Code
  </a>
  <a href="#" target="_blank"
     style="display:inline-block; margin:6px; padding:10px 20px; border-radius:8px; background:#6c757d; color:white; text-decoration:none; font-weight:600;">
     Slides
  </a>
</div>

---

## Overview

<div style="background:#f8fafc; padding:22px; border-radius:12px; box-shadow:0 3px 10px rgba(0,0,0,0.06); margin-bottom:24px;">
MIR3D is designed for robotic mushroom harvesting in extremely low-light or no-light cultivation environments.
Instead of relying on conventional RGB sensing, the framework uses monocular infrared imagery to recover geometry,
estimate grasp-related structures, and support downstream motion planning for a UR5e robotic harvester.
</div>

## Key Highlights

<div style="display:grid; grid-template-columns:repeat(auto-fit, minmax(220px, 1fr)); gap:16px; margin-bottom:28px;">

<div style="background:white; border:1px solid #e5e7eb; border-radius:12px; padding:18px; box-shadow:0 3px 8px rgba(0,0,0,0.04);">
  <h4>Infrared Perception</h4>
  <p style="margin-bottom:0;">Robust perception under dark cultivation conditions without visible illumination.</p>
</div>

<div style="background:white; border:1px solid #e5e7eb; border-radius:12px; padding:18px; box-shadow:0 3px 8px rgba(0,0,0,0.04);">
  <h4>Geometry Estimation</h4>
  <p style="margin-bottom:0;">Recover mushroom geometry from a single infrared image for harvesting-oriented analysis.</p>
</div>

<div style="background:white; border:1px solid #e5e7eb; border-radius:12px; padding:18px; box-shadow:0 3px 8px rgba(0,0,0,0.04);">
  <h4>Robotic Integration</h4>
  <p style="margin-bottom:0;">Predict grasp points and support motion planning for UR5e-based autonomous harvesting.</p>
</div>

</div>

## Method Pipeline

<div style="background:#ffffff; padding:22px; border-radius:12px; border:1px solid #e5e7eb; box-shadow:0 3px 10px rgba(0,0,0,0.05); margin-bottom:24px;">
<ol style="margin-bottom:0;">
  <li>Monocular infrared image acquisition in dark environments</li>
  <li>Geometry-aware perception and structure estimation</li>
  <li>Grasp point prediction for harvesting targets</li>
  <li>Motion planning for UR5e robotic execution</li>
</ol>
</div>

<div style="text-align:center; margin:26px 0;">
  <img src="/assets/img/mir3d_pipeline.png" alt="MIR3D pipeline"
       style="width:100%; max-width:900px; border-radius:12px; box-shadow:0 6px 16px rgba(0,0,0,0.10);">
  <p style="color:#666; margin-top:10px;"><em>Figure: Overall pipeline of MIR3D.</em></p>
</div>

## Results

<div style="background:#f8fafc; padding:22px; border-radius:12px; box-shadow:0 3px 10px rgba(0,0,0,0.06); margin-bottom:24px;">
This section can present qualitative reconstruction examples, robotic grasping cases,
quantitative evaluation tables, and harvesting demonstrations.
</div>

<div style="display:grid; grid-template-columns:repeat(auto-fit, minmax(260px, 1fr)); gap:18px; margin-bottom:28px;">
  <img src="/assets/img/result1.png" style="width:100%; border-radius:12px; box-shadow:0 4px 12px rgba(0,0,0,0.08);">
  <img src="/assets/img/result2.png" style="width:100%; border-radius:12px; box-shadow:0 4px 12px rgba(0,0,0,0.08);">
</div>

## Demo Video

<div style="text-align:center; margin-bottom:28px;">
  <iframe width="840" height="472"
    src="https://www.youtube.com/embed/YOUR_VIDEO_ID"
    title="MIR3D Demo Video"
    frameborder="0"
    allowfullscreen
    style="max-width:100%; border-radius:12px; box-shadow:0 6px 18px rgba(0,0,0,0.12);">
  </iframe>
</div>