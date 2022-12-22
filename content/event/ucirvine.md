+++
title = "Sources of Variance in Pretraining and Finetuning"
date = 2022-06-20T13:00:00  # Schedule page publish date.
draft = false

# Talk start and end times.
#   End time can optionally be hidden by prefixing the line with `#`.
time_start = 2022-06-15T13:00:00
# time_end = 2030-06-01T15:00:00

# Abstract and optional shortened version.
abstract = "You have engaged in the very modern practice of transfer learning. You pretrained a model on a self-supervised objective, then you finetuned it on a downstream task, and you find excellent performance on the test set. 'Aha', you say. 'I found a good pretraining procedure.' Did you? You try finetuning again. The results are terrible! 'Aha', you say. 'I found a bad finetuning procedure.' Did you?\n\nThe random seeds for both pretraining and finetuning stages have a substantial influence on outcome. However, it is computationally expensive to pretrain new models, so measuring the robustness of a procedure across different seeds can be prohibitive. This talk will address, first, the influence that a pretraining seed has on both in-domain and OOD performance. Then we will address the role of the finetuning seed. Much variation in OOD generalization can be ascribed to where the finetuning seeds direct SGD trajectories. In particular, we discuss how to predict generalization behavior in a finetuned model, based on topographic properties of its region of the loss surface.  By understanding the degree of influence that random seeds have on performance, we can fairly evaluate a robust training procedure, rather than a single set of parameters. By understanding the mechanism of that influence, we can go further by developing improved training methods."
abstract_short = ""

# Name of event and optional event URL.
event = "UC Irvine"

# Location of event.
location = "Irvine, CA"

# Is this a selected talk? (true/false)
selected = false

# Projects (optional).
#   Associate this talk with one or more of your projects.
#   Simply enter your project's filename without extension.
#   E.g. `projects = ["deep-learning"]` references `content/project/deep-learning.md`.
#   Otherwise, set `projects = []`.
projects = []

# Tags (optional).
#   Set `tags = []` for no tags, or use the form `tags = ["A Tag", "Another Tag"]` for one or more tags.
tags = []

# Links (optional).
url_pdf = ""
url_slides = ""
url_video = "https://www.youtube.com/watch?v=Lni4PIlbJjI"
url_code = ""

# Does the content use math formatting?
math = true

# Does the content use source code highlighting?
highlight = true

# Featured image
# Place your image in the `static/img/` folder and reference its filename below, e.g. `image = "example.jpg"`.
[header]
# image = "headers/bubbles-wide.jpg"
# caption = "My caption :smile:"

+++
