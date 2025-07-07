---
layout: default
title: Few-shot transfer of tool-use skills using human demonstrations with proximity and tactile sensing
---

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

# Few-shot transfer of tool-use skills using human demonstrations with proximity and tactile sensing

Marina Y. Aoyama<sup>1</sup>, Sethu Vijayakumar<sup>1</sup>, Tetsuya Narita <sup>2</sup>

<sup>1</sup>The University of Edinburgh, <sup>2</sup>Sony Group Corporation 

IEEE Robotics and Automation Letters (RA-L) 2025 

<div class="button-container">
  <a href="https://ieeexplore.ieee.org/abstract/document/11053701" target="_blank" class="my-button">
    <span class="icon"><i class="fas fa-file-alt"></i></span>
    <span>Paper</span>
  </a>

  <a href="https://www.youtube.com/embed/zP4JvHaCWHk?start=11" target="_blank" class="my-button">
    <span class="icon"><i class="fas fa-video"></i></span>
    <span>Video</span>
  </a>
</div>

Our few-shot approach learns to manipulate new tools with few demonstrations! 

<video width="800" height="450" controls muted>
  <source src="assets/videos/fourtask_short_video_compressed.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

## Abstract 
Tools extend the manipulation abilities of robots, much like they do for humans. Despite human expertise in tool manipulation, teaching robots these skills faces challenges. The complexity arises from the interplay of two points of contact: one between the robot and the tool, and another between the tool and the environment. Tactile and proximity sensors play a crucial role in identifying these complex contacts. However, learning tool manipulation with a small amount of real-world data using these sensors remains challenging due to the large sim-to-real gap and sensor noise. To address this, we propose a few-shot tool-use skill transfer framework using multimodal sensing. The framework involves pre-training the base policy to capture contact states common in tool-use skills in simulation and fine-tuning it with human demonstrations collected in the real-world target domain to bridge the domain gap. We validate that this framework enables teaching surface-following tasks using tools with diverse physical and geometric properties with a small number of demonstrations on the Franka Emika robot arm. Our analysis suggests that the robot acquires new tool-use skills by transferring the ability to recognise tool-environment contact relationships from pre-trained to fine-tuned policies. Additionally, integrating proximity and tactile sensors enhances the identification of contact states and environmental geometry. 

## Summary Video 

<!--
<iframe width="800" height="450" src="https://www.youtube.com/embed/zP4JvHaCWHk?start=11" frameborder="0" allowfullscreen></iframe>
-->

## Method

Our method integrates tactile sensing...

## Results

### Four surface following tasks 

<div style="display: grid; grid-template-columns: repeat(2, 1fr); gap: 2rem 1rem; max-width: 900px; margin: auto;">

  <div style="text-align: center;">
    <video width="400" controls>
      <source src="assets/videos/smallbrush_short_compressed.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <div style="font-size: 0.85rem; color: #555; margin-top: 0.25rem;">Small brush</div>
  </div>

  <div style="text-align: center;">
    <video width="400" controls>
      <source src="assets/videos/widebrush_short_compressed.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <div style="font-size: 0.85rem; color: #555; margin-top: 0.25rem;">Wide brush</div>
  </div>

  <div style="text-align: center;">
    <video width="400" controls>
      <source src="assets/videos/broom_short_compressed.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <div style="font-size: 0.85rem; color: #555; margin-top: 0.25rem;">Broom</div>
  </div>

  <div style="text-align: center;">
    <video width="400" controls>
      <source src="assets/videos/sponge_short_compressed.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <div style="font-size: 0.85rem; color: #555; margin-top: 0.25rem;">Sponge</div>
  </div>

</div>

### Online adaptation 

<div style="display: grid; grid-template-columns: repeat(2, 1fr); gap: 1rem; max-width: 900px; margin: auto;">

  <div style="text-align: center;">
    <video width="400" controls>
      <source src="assets/videos/real_online_inclination_compressed.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <div style="font-size: 0.85rem; color: #555; margin-top: 0.25rem;">Changing inclination</div>
  </div>

  <div style="text-align: center;">
    <video width="400" controls>
      <source src="assets/videos/real_online_deformable_short_compressed.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <div style="font-size: 0.85rem; color: #555; margin-top: 0.25rem;">Deformable surface</div>
  </div>

</div>

<div style="display: flex; justify-content: center; gap: 1rem; max-width: 800px; margin: 2rem auto 0 auto;">

  <div style="text-align: center;">
    <video width="400" controls>
      <source src="assets/videos/smallbrush_step_short_compressed.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <div style="font-size: 0.85rem; color: #555; margin-top: 0.25rem;">Step painting</div>
  </div>

</div>


### Demo only (baseline) vs. Pre-train+Demo (proposed) 

<div style="display: grid; grid-template-columns: repeat(2, 1fr); gap: 1rem; max-width: 900px; margin: auto;">

  <div style="text-align: center;">
    <video width="400" controls>
      <source src="assets/videos/smallbrush_demoonly_short_compressed.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <div style="font-size: 0.85rem; color: #555; margin-top: 0.25rem;">Demo only (baseline)<br>Pressing too much! Tool slippage. </div>
  </div>

  <div style="text-align: center;">
    <video width="400" controls>
      <source src="assets/videos/smallbrush_short_compressed.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <div style="font-size: 0.85rem; color: #555; margin-top: 0.25rem;">Pre-train+Demo (proposed) </div>
  </div>

</div>

### Robustness to external disturbances 

<div style="display: grid; grid-template-columns: repeat(2, 1fr); gap: 1rem; max-width: 900px; margin: auto;">

  <div style="text-align: center;">
    <video width="400" controls>
      <source src="assets/videos/real_disturbances_short_compressed.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <div style="font-size: 0.85rem; color: #555; margin-top: 0.25rem;">Sim</div>
  </div>

  <div style="text-align: center;">
    <video width="400" controls>
      <source src="assets/videos/real_disturbances_short_compressed.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <div style="font-size: 0.85rem; color: #555; margin-top: 0.25rem;">Real</div>
  </div>

</div>


### Citation 
<div style="margin: 2rem auto; max-width: 800px; width: 100%; text-align: center;">
  <textarea readonly rows="9" style="
    font-family: monospace;
    font-size: 0.85rem;
    background: #f5f5f5;
    border: 1px solid #ccc;
    border-radius: 6px;
    padding: 0.5rem;
    width: auto;
    min-width: 300px;
    max-width: 100%;
    resize: none;
    box-sizing: border-box;
  ">@article{aoyama2025few,
  title={Few-shot transfer of tool-use skills using human demonstrations with proximity and tactile sensing},
  author={Aoyama, Marina Y and Vijayakumar, Sethu and Narita, Tetsuya},
  journal={IEEE Robotics and Automation Letters},
  year={2025},
  publisher={IEEE}
}</textarea>
</div>

