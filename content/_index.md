---
# Leave the homepage title empty to use the site title
title: ""
date: 2025-02-24
type: landing

design:
  # Default section spacing
  spacing: "6rem"

sections:
  - block: resume-biography-3
    content:
      # Choose a user profile to display (a folder name within `content/authors/`)
      username: admin
      text: ""
      # Show a call-to-action button under your biography? (optional)
      button:
        text: Download CV
        url: uploads/academic_cv.pdf
  - block: markdown
    id: research
    content:
      title: 'My Research'
      subtitle: ''
      text: |-
        I want to completely and comprehensively understand language model training. This objective combines linguistics, optimization, learning dynamics, science of deep learning, interpretability,  and behavioral analysis. Recently, I have begun using similar approaches to study scientific discovery models and enhance broader scientific understanding.

        My top three current research goals are:
        - Leveraging training trajectories and variation between runs to identify what concepts are significant and distinct to a model. How do these concepts relate to each other?
        - Predicting model behavior on edge cases by holistically understanding models on a computational and algorithmic level. 
        - Expanding human understanding of the world by studying how models learn to simulate it. To achieve this interdisciplinary objective, my current collaborations aim to deeply understand fish, stars, and weather as well as language.

        My current publication list is available on my [Google Scholar](https://scholar.google.com/citations?user=TPhVfX8AAAAJ&hl=en).
    design:
      columns: '1'
  - block: collection
    id: posts
    content:
      title: Recent Posts
      subtitle: ''
      text: ''
      # Page type to display. E.g. post, talk, publication...
      page_type: post
      # Choose how many pages you would like to display (0 = all pages)
      count: 4
      # Filter on criteria
      filters:
        author: ""
        category: ""
        tag: ""
        exclude_featured: false
        exclude_future: false
        exclude_past: false
        publication_type: ""
      # Choose how many pages you would like to offset by
      offset: 0
      # Page order: descending (desc) or ascending (asc) date.
      order: desc
    design:
      # Choose a layout view
      view: date-title-summary
      # Reduce spacing
      spacing:
        padding: [0, 0, 0, 0]
  - block: markdown
    id: contact
    content:
      title: 'Potential Mentees'
      subtitle: 'Read before emailing me'
      text: |-
        You do not need to email me to apply to my lab and it will offer most applicants no advantage to do so. One exception for applicants with existing work to share: If your work is *highly* relevant to me, feel free to reach out to discuss it. I am not currently hiring interns or looking for remote junior collaborators. I welcome any specific connections and questions about my research, though I may direct you towards my coauthors who did the real work related to your inquiry. 

        I welcome any messages from fellow disabled researchers looking to connect—I have [direct personal experience in this arena](post/hands/). 

        ## Am I a good advisor for you?

        If you like my papers, you may be a good fit! However, note that I am primarily interested in *understanding* systems, not *creating* them. Occasionally, my collaborators and I discover a new way to improve models; **this is entirely by accident and should not be expected.** If you are trying to build exciting new models or fix current ones, you may want to look for a different advisor.
    design:
      columns: '1'
---
