---
title: "HUSTL"
subtitle: ""
date: 2023-06-14T13:09:28-07:00
draft: false
weight: 1
description: "Open source computer vision tool for creating hyperlapse videos"
coverImage: "" # a 5:1 image with important content in the center 1/3 zone for best effect
cardImage: "hustl.mp4" # a thin image/video featured on cards
autonumbering: false
katex:
  enable: false
  singleDollarDeliminator: true
---

![Hyperlapse processed with HUSTL](hustl.mp4 "Hyperlapse processed with HUSTL")

Links: [GitHub Repo](https://github.com/michaelmyc/hustl), [Project Writeup](hustl-writeup.pdf) \
Members: Michael Mao, Jiaju Ma, James Li \
Duration: Spring 2019

## Overview

Making good hyperlapse videos is difficult. It usually requires photographers to take photos between consistent distance intervals and keep the height of the camera and the direction of the lens steady and smooth. Alternatively, they can mount their camera on expensive steadicams or gimbals. To make creating high-quality hyperlapses easier, we present HUSTL (Hyper-Ultra-Super-Time-Lapse), an open source three-stage software pipeline based on the state of the art academic research papers. Our tool allows users to only provide rough hand-held hyperlapse frames to create a smoothed hyperlapse video. 

This is a class project for Brown University's [CS 1430 Computer Vision](https://cs.brown.edu/courses/info/csci1430/) class taught by [Prof. James Tompkin](https://jamestompkin.com/).

## Methodology

There are 3 major challenges to creating a high-quality hyperlapse video: 

1. Some frames can be sub-optimal and should be skipped
2. Frames may have different white balance, lighting conditions, and some frames may be over-exposed or under-exposed
3. Frames need to be aligned to ensure that the camera movement looks smooth

To deal with these three major issues, we propose a 3-step pipeline: frame selection[^1], color matching[^2], and video stabilization[^3].

For more details, please refer to the [project writeup](hustl-writeup.pdf).

[^1]: Neel Joshi, Wolf Kienzle, Mike Toelle, Matt Uyttendaele, and Michael F. Cohen. [Real-Time Hyperlapse Creation via Optimal Frame Selection](https://dl.acm.org/doi/10.1145/2766954) *ACM Transactions on Graphics*, 2015
[^2]: Jaesik Park, Yu-Wing Tai, Sudipta Sinha, and In So Kweon. [Efficient and Robust Color Consistency for Community Photo Collections](https://www.microsoft.com/en-us/research/publication/efficient-color-consistency-for-community-photos/) *Computer Vision and Pattern Recognition (CVPR)*, 2016
[^3]: Shuaicheng Liu, Lu Yuan, Ping Tan, and Jian Sun. [Bundled Camera Paths for Video Stabilization](https://dl.acm.org/doi/10.1145/2461912.2461995) *ACM Transactions on Graphics*, 2013

![HUSTL pipeline](hustl-pipeline.png "HUSTL pipeline")

## Demonstrations

### Faunce Arch

<script src="https://player.vimeo.com/api/player.js"></script>
<style>
@media (orientation: landscape) {
  .vimeo-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 1em;
  }
}
@media (orientation: portrait) {
  // ipad screen
  @media (min-aspect-ratio: 3/5) {
    .vimeo-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 1em;
    }
  }
  .vimeo-grid {
    display: grid;
    grid-template-rows: 1fr 1fr;
    gap: 1em;
  }
}
.vimeo-container {
  display: grid;
  text-align: center;
}
</style>
<div class="vimeo-grid">
  <div class="vimeo-container">
    <div style="padding:56.25% 0 0 0;position:relative;justify-self:none;"><iframe src="https://player.vimeo.com/video/335471326?h=a82fe09ee9&color=ffffff&title=0&byline=0&portrait=0" style="position:absolute;top:0;left:0;width:100%;height:100%;" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen></iframe></div>
    <p class="dark">Baseline</p>
  </div>

  <div class="vimeo-container">
    <div style="padding:56.25% 0 0 0;position:relative;justify-self:none;"><iframe src="https://player.vimeo.com/video/335471168?h=a82fe09ee9&color=ffffff&title=0&byline=0&portrait=0" style="position:absolute;top:0;left:0;width:100%;height:100%;" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen></iframe></div>
    <p class="dark">HUSTL</p>
  </div>
</div>

### Soldiers Memorial Gate

<div class="vimeo-grid">
  <div class="vimeo-container">
    <div style="padding:56.25% 0 0 0;position:relative;justify-self:none;"><iframe src="https://player.vimeo.com/video/335471673?h=a82fe09ee9&color=ffffff&title=0&byline=0&portrait=0" style="position:absolute;top:0;left:0;width:100%;height:100%;" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen></iframe></div>
    <p class="dark">Baseline</p>
  </div>

  <div class="vimeo-container">
    <div style="padding:56.25% 0 0 0;position:relative;justify-self:none;"><iframe src="https://player.vimeo.com/video/335471545?h=a82fe09ee9&color=ffffff&title=0&byline=0&portrait=0" style="position:absolute;top:0;left:0;width:100%;height:100%;" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen></iframe></div>
    <p class="dark">HUSTL</p>
  </div>
</div>

## Areas Needing Improvements

As shown in the demo, even though the camera movements have been smoothed, there are still a few issues degrading the hyperlapse:

1. Objects can appear to be warped unnaturally, especially in image corners and especially when the warping needed is significant.
2. HUSTL struggles in narrow environments (like hallways) where objects move out of frame relatively quickly compared to an open environment.
3. HUSTL may cause unnatural lighting effects and unintended brightness changes when transitioning between well-lit and dimly-lit environments.

We believe a better video stabilization algorithm (functioning like the "Warp Stabilizer" in Adobe Premiere) may be better equipped to resolve the first 2 issues. A potential method to resolve the 3rd issue may look like:

1. Project the color space to a logarithmic space to reduce risk of information loss when adjusting brightness
2. Adjust the images so that the brightness (average brightness) is consistent across all frames
3. Run the images through the HUSTL color consistency pipeline
4. Project the logarithmic space back to the normal linear color space