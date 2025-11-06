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
    content:
      title: 'My Research'
      subtitle: ''
      text: |-
        My core agenda focuses on a single goal: to completely and comprehensively understand language model training. This objective combines linguistics, optimization, learning dynamics, science of deep learning, interpretability,  and behavioral analysis. Recently, I have begun using similar approaches to study scientific discovery models and enhance broader scientific understanding.

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
---
