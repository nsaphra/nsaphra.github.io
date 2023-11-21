---


# Documentation: https://wowchemy.com/docs/managing-content/

title: Latent State Transitions in Training Dynamics
subtitle: ''
summary: ''
authors:
- "Michael Hu"
- "Angelica Chen"
- admin
- "Kyunghyun Cho"

tags: []
categories: []
date: '2023-08-01'
lastmod: 2023-07-17T21:36:33-04:00
featured: true
draft: false

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ''
  focal_point: ''
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
publishDate: '2023-07-18T01:39:14.003172Z'
publication_types:
- '2'
abstract: "The impact of randomness on model training is poorly understood. How do differences in data order and initialization actually manifest in the model, such that some training runs outperform others or converge faster? Furthermore, how can we interpret the resulting training dynamics and the phase transitions that characterize different trajectories? To understand the effect of randomness on the dynamics and outcomes of neural network training, we train models multiple times with different random seeds and compute a variety of metrics throughout training, such as the L2 norm, mean, and variance of the neural network's weights. We then fit a hidden Markov model (HMM) over the resulting sequences of metrics. The HMM represents training as a stochastic process of transitions between latent states, providing an intuitive overview of significant changes during training. Using our method, we produce a low-dimensional, discrete representation of training dynamics on grokking tasks, image classification, and masked language modeling. We use the HMM representation to study phase transitions and identify latent 'detour' states that slow down convergence."
publication: '*Transactions of Machine Learning Research (TMLR)*'
links:
- name: URL
  url: https://arxiv.org/abs/2308.09543
---
