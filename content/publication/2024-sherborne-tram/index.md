---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "TRAM: Bridging Trust Regions and Sharpness Aware Minimization"
subtitle: ''
summary: ''
authors:
- Tom Sherborne
- admin
- Pradeep Dasigi
- Hao Peng
tags: []
categories: []
date: '2024-01-15'
lastmod: 2023-07-17T21:36:33-04:00
featured: false
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
publishDate: '2023-11-18T01:36:33.109294Z'
publication_types:
- '3'
abstract: 'By reducing the curvature of the loss surface in the parameter space, Sharpness-aware minimization (SAM) yields widespread robustness improvement under domain transfer. Instead of focusing on parameters, however, this work considers the transferability of representations as the optimization target for out-of-domain generalization in a fine-tuning setup. To encourage the retention of transferable representations, we consider trust region-based fine-tuning methods, which exploit task-specific skills without forgetting task-agnostic representations from pre-training. We unify parameter- and representation-space smoothing approaches by using trust region bounds to inform SAM-style regularizers on both of these optimization surfaces. We propose Trust Region Aware Minimization (TRAM), a fine-tuning algorithm that optimizes for flat minima and smooth, informative representations without forgetting pre-trained structure. We find that TRAM outperforms both sharpness-aware and trust region-based optimization methods on cross-domain language modeling and cross-lingual transfer, where robustness to domain transfer and representation generality are critical for success. TRAM establishes a new standard in training generalizable models with minimal additional computation.'
publication: '*International Conference on Learning Representations (ICLR)*'
links:
- name: URL
  url: https://arxiv.org/abs/2310.03646
---
