---
title: "AI-Based Preprocessing Technologies for JPEG Image Coding"
collection: projects
type: "Computer vision"
permalink: /projects/AI-Based-Preprocessing-Technologies-for-JPEG-Image-Coding
venue: "Funded by Anhui Students' Platform for innovation and entrepreneurship training program"
date: 2022-05-25
location: "USTC Hefei, China"
---

# Motivation

The image coding technology represented by JPEG has been extensively applied across various industries. JPEG image coding is a lossy compression technique, and when the coding rate is low , the reproduced image may exhibit noticeable artifacts. 

To address this issue, there are two main approaches: post-processing after decoding, which requires high demands on image viewers, and pre-processing before encoding, which preserves image viewers without alteration. This project aims to explore the use of artificial intelligence (AI) technologies, particularly deep learning, for pre-processing images prior to JPEG encoding. By doing so, the goal is to mitigate artifacts while maintaining compatibility with existing image viewers.

# Obstacle

- The mechanism of distortion caused by the JPEG compression process in images remains a topic that requires further research and investigation.
- Pre-processing algorithms are far less popular than post-preprocessing due to the more complex treatment the procedure induces and the weaker control it provides on the output artifacts.
- JPEG is a non-differentiable process, making it challenging to introduce into the learning stage of neural networks.

# Weakness of previous work

- The vast majority of preprocessing work relies on traditional image methods such as attribute filtering, and the performance needs further improvement.
- We believe that in the existing CNN-based preprocessing approaches, the precision of the differentiable JPEG model and the bpp(bits per pixel) estimation model needs to be improved, leading to limitations in performance.

# Method

- We have developed two separate deep neural network models with distinct functions: one accurately simulates the distortions caused by JPEG compression and decompression on images, while the other estimates the bpp (bits per pixel) of the images after undergoing JPEG compression.
- We propose an end-to-end training approach that pre-processes images before JPEG compression to minimize artifacts in the decompressed images at a given bitrate.

# Achievement(Expected)

achievement



