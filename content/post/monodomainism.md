+++
title = "Against Monodomainism"

date = 2021-04-28T00:00:00
draft = false

# Authors. Comma separated list, e.g. `["Bob Smith", "David Jones"]`.
authors = []

# Tags and categories
# For example, use `tags = []` for no tags, or the form `tags = ["A Tag", "Another Tag"]` for one or more tags.
tags = []
categories = []

summary = "A petty rant on the exceptional treatment of computer vision applications, directed at the machine learning community."

# Featured image
# Place your image in the `static/img/` folder and reference its filename below, e.g. `image = "example.jpg"`.
# Use `caption` to display an image caption.
#   Markdown linking is allowed, e.g. `caption = "[Image credit](http://example.org)"`.
# Set `preview` to `false` to disable the thumbnail in listings.
[header]
image = ""
caption = ""
preview = true

+++

Reaching the endpoint of a PhD studying how language models learn, I have spent several years telling people that I study "machine learning and natural language processing". However, my colleagues who tried to understand or augment image classifiers would describe themselves only as working in "machine learning". I argue that this pattern reflects thinking about what it means to be "application" work or "core" machine learning that damages our understanding of statistical modeling and deep learning as a whole.

Why do we know so little about how language models learn? This gap is in part because consideration of NLP as a domain is historically rare in venues that publish most training dynamics research, or analytic work in learning theory. A current search[^1] of ICML 2020 publications returned 169 papers with citations to “Association for Computational Linguistics” or “ACL”, even including citations to many potential sister conferences: NAACL, AACL, or EACL. A search for citations to a single vision conference, “Computer Vision and Pattern Recognition” or “CVPR”, turned up 541 papers. In COLT publications since 2017, the same searches turned up 13 and 23 papers, respectively. In ICML 2020, Wikitext-* or PTB references found only 16 results, while the most popular small corpus for image classification, MNIST, found 264 ICML publications[^2].

Linguistics provides us with the salient concept of *markedness* [(Andersen, 1989)](https://www.degruyter.com/document/doi/10.1515/9783110862010.11/html). In language, some forms of a word are the default form, while others are explicitly marked by some additional inflection. An example would be contrast between the word “marked”, which is an *unmarked* form compared to “unmarked”, which is *marked* by the prefix “un-”. In machine learning, we might call CV an unmarked domain by convention, in contrast to the *marked* NLP. This convention means that certain tasks and architectures are considered the default environments to understand. Such a convention privileges understanding continuous data over discrete; ConvNets over LSTMs; ResNets over Transformers; geometric tasks over structured prediction.

Understanding one machine learning domain will always extend analysis of others. For example, latent tree structure is inherent to both domains, but in CV, it is obscured by the image data from which we must compose eyes and mouth into a face—and subsequently, body and face into a cow [(Vedaldi et al., 2014)](https://ieeexplore.ieee.org/document/6909858). Image classification is also a language task, because it is our language that provides the intuitions which we use to construct ontologies that turn into image classes; English does not provide us with common distinctions for different packs of wolves, but it names every dog breed, and so the image labels are chosen according to available terminology.

Many researchers think of text data as arcane, but the unmarked domain of CV displays many idiosyncrasies on which to overfit our understanding of statistical modeling. CV provides us with many interesting geometric phenomena, but the underlying structure of language *without* the added noisy channel of an image can provide a clear and simple domain worth analyzing, as well. A true understanding of statistical models must be a multi-domain understanding, not a mono-domain view focused on one task and its peculiarities.

[^1]: Searches were performed with Google Scholar.
[^2]: *CL venues have also become distanced from work in computational linguistics [(Reiter, 2007)](https://www.aclweb.org/anthology/J07-2013.pdf), leaving NLP as a field deprived of new scientific work in its data domain as well as new scientific work in its methodologies.
