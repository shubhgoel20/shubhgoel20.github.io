---
title: DenoiseEEG
summary: 'An End-to-End Deep Learning model to remove artifacts from raw EEG signals'
tags:
  - Deep Learning
date: '2022-12-01'

# Optional external URL for project (replaces project detail page).
external_link: ''

image: 
  caption: Photo by Kanoga, Suguru & Mitsukura, Yasue. (2017).
  focal_point: Smart

links:
  - icon: github
    icon_pack: fab
    name: Code
    url: https://github.com/shubhgoel20/DenoiseEEG
url_code: ''
url_pdf: ''
url_slides: ''
url_video: ''

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: ''
---

I worked on a semester-long research project on Signal Processing and DL under Prof. Lalan Kumar
in his Multichannel Signal Processing(MSP) lab. In raw Electroencephalography (EEG) signals, unwanted
and extraneous electrical signals pose significant challenges in any downstream task or research in clinical diagnosis, neuroscience, and human-computer interaction. To address this issue, I developed a novel, simple, end-to-end DL framework to effectively map noisy EEG signals to clean EEG signals. Traditional methods to denoise EEG signals, like Independent Component Analysis (ICA), are time-consuming and offline, making them infeasible for real-time applications.

I initially created a basic MLP architecture and gradually enhanced its complexity by incorporating
1-D Convolution layers, LSTM layers, and ResNet-inspired skip connections. Our final model achieved
an impressive Pearson Correlation Coefficient (PCC) of 0.933. Unlike some existing DL approaches, I
used actual EEG data from lift and grasp tasks [2], avoiding synthetic noise and ensuring authentic signal representation. I utilized ICA using the EEGLAB toolbox in MATLAB to generate the necessary noisy
EEG-clean EEG pairs for training.
