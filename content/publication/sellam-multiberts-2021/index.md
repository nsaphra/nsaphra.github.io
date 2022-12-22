---
title: "The MultiBERTs: BERT Reproductions for Robustness Analysis"
date: 2021-01-01
publishDate: 2021-09-32T18:43:51.338959Z
authors: ["Thibault Sellam", "Steve Yadlowsky", "Jason Wei", admin, "Alexander D'Amour", "Tal Linzen", "Jasmijn Bastings", "Iulia Turc", "Jacob Eisenstein", "Dipanjan Das", "Ian Tenney", "Ellie Pavlick"
]
publication_types: ["1"]
abstract: "Experiments with pre-trained models such as BERT are often based on a single checkpoint. While the conclusions drawn apply to the artifact tested in the experiment (i.e., the particular instance of the model), it is not always clear whether they hold for the more general procedure which includes the architecture, training data, initialization scheme, and loss function. Recent work has shown that repeating the pre-training process can lead to substantially different performance, suggesting that an alternative strategy is needed to make principled statements about procedures. To enable researchers to draw more robust conclusions, we introduce MultiBERTs, a set of 25 BERT-Base checkpoints, trained with similar hyper-parameters as the original BERT model but differing in random weight initialization and shuffling of training data. We also define the Multi-Bootstrap, a non-parametric bootstrap method for statistical inference designed for settings where there are multiple pre-trained models and limited test data. To illustrate our approach, we present a case study of gender bias in coreference resolution, in which the Multi-Bootstrap lets us measure effects that may not be detected with a single checkpoint. The models and statistical library are available online, along with an additional set of 140 intermediate checkpoints captured during pre-training to facilitate research on learning dynamics."
featured: false
publication: "*ICLR*"
url_pdf: "https://arxiv.org/pdf/2106.16163.pdf"
---
