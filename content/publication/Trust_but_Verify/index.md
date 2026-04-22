---
title: 'Trust but verify: Image-aware evaluation of radiology report generators'

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here
# and it will be replaced with their full name and linked to their profile.
authors:
  - admin
  - Dawood Al Chanti
  - Alice Caplier

# Author notes (optional)
author_notes:
  - ''

date: '2026-03-01T00:00:00Z'
doi: '10.1016/j.mlwa.2026.100851'

# Schedule page publish date (NOT publication's date).
publishDate: '2026-03-01T00:00:00Z'

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ['2']

# Publication name and optional abbreviated publication name.
publication: Machine Learning with Applications Volume 23
publication_short: In *MLWA*

abstract: Large language and vision-language models have greatly advanced automated chest X-ray report generation (RRG),. yet current evaluation practices remain largely text-based and detached from image evidence. Traditional machine translation metrics fail to determine whether generated findings are clinically correct or visually grounded, limiting their suitability for medical applications. This study introduces a comprehensive, image-aware evaluation framework that integrates the VICCA (Visual Interpretation and Comprehension of Chest X-ray Anomalies) protocol with the domain-specific semantic metric MCSE (Medical Corpus Similarity Evaluation). VICCA combines visual grounding and text-guided image generation to assess visual-textual consistency, while MCSE measures semantic and factual fidelity through clinically meaningful entities, negations, and modifiers. Together, they provide a unified, semi-reference-free assessment of pathology-level accuracy, semantic coherence, and visual consistency. Five representative RRG models, R2Gen, M2Trans, CXR-RePaiR, RGRG, and MedGemma, are benchmarked on 2461 MIMIC-CXR studies using a standardized pipeline. Results reveal systematic trade-offs: models with high pathology agreement often generate semantically weak or visually inconsistent reports, whereas textually fluent models may lack proper image grounding. By integrating clinical semantics and visual reliability within a single multimodal framework, VICCA establishes a robust paradigm for evaluating the trustworthiness and interpretability of AI-generated radiology reports.

# Summary. An optional shortened abstract.
# summary: Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis posuere tellus ac convallis placerat. Proin tincidunt magna sed ex sollicitudin condimentum.

tags:
  - Radiology report generation
  - Chest X-ray
  - Image-aware evaluation
  - Interpretability Multimodal AI

# Display this page in the Featured widget?
featured: false

# Custom links (uncomment lines below)
# links:
# - name: Custom Link
#   url: http://example.org

url_pdf: 'https://doi.org/10.1016/j.mlwa.2026.100851'
url_code: 'https://github.com/sayeh1994/vicca'
url_dataset: ''
url_poster: ''
url_project: ''
url_slides: ''
url_source: ''
url_video: ''

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
# projects:
#   - Master2Project

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
# slides: example
---
