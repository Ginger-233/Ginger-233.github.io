---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

## Education

* **Shanghai Jiao Tong University** (2023.7 – Present)
  * Notable Courses: Algorithm Design (A+), Data Structures (A+), Computer Architecture (A+), Discrete Mathematics (A+), Operating Systems (A).
  * GPA Ranking: Top Tier.

## Research & Projects

### Bi-value Chores under EFX (2025.10 – Present)
* **Topic**: Fair Division, EFX in Bi-value Chores.
* **Contribution**: Proposed a most-envy graph algorithm and function-based Envy-Cycle Elimination.
* **Result**: Submitted to top conferences (FOCS/WINE).

### RAG Teaching Assistant System (2025.9 – 2025.11)
* **Role**: Lead Developer.
* **Tech Stack**: AsyncIO, Embedding API, ChromaDB.
* **Achievements**: Optimized I/O concurrency (80% speedup), implemented Top-K retrieval, and integrated Qwen-VL for multi-modal support (PDF/Slides).
* **Outcome**: Deployed a "RAG-Base-Teaching-Assistant" system.

### Flowrank: Mining Silent Data Errors in Jupyter Notebooks (2025.8 – 2025.10)
* **Role**: Researcher.
* **Contribution**: Developed AST analysis for cell dependencies, Temporal Risk Weighting for Time-Travel bugs.
* **Method**: Used Sensitivity-Influence algorithms (HITS + Katz Centrality) to identify Root Causes.

## Skills

* **Programming**: Python, C/C++, ARM Assembly, Shell.
* **Tools**: PyTorch, Chainlit, Docker, Git, LaTeX, Markdown.
* **Other**: Mathematical Modeling, Vibe Coding.

## Publications & Manuscripts

<ul>{% for post in site.publications reversed %}
  {% include archive-single-cv.html %}
{% endfor %}</ul>
