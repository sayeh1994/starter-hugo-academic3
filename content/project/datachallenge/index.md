---
title: Automatic No-Reference Image Sharpness Assessment in Infrared Images
summary: A system that automatically finds the main object in an image and evaluates its sharpness.
tags:
  - image processing
  - infrared image processing
date: '2022-05-11T00:00:00Z'

# Optional external URL for project (replaces project detail page).
external_link: ''

image:
  caption: Photo by Lynred
  focal_point: Smart

links: ''
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

The goal of this project was to automatically estimate image quality, focusing on image sharpness, while taking into account its correlation with image contrast and noise levels, and its interference with image compression and saturation. The sharpness evaluation was also focused on the object of interest, or the main object in the image, instead of a simple global sharpness evaluation. We proposed a new design by image segmentation (blocking) and saliency detection using predefined sharpness metrics implemented from the literature. In addition to the objective evaluation of image sharpness, a subjective evaluation was performed in the context of a small-scale experiment on a subset of the provided dataset.

Analysis has shown that our proposed block-based method outperforms previous methods evaluated on the entire image when the sharpness scores are compared against Lynred’s scores and the ones obtained from the subjective evaluation. While the results aren’t satisfactory enough to be applied in an industrial setting, they still show a higher correlation between our proposed image evaluation and the subjective ranking, than the correlation between the subjective ranking and Lynred’s scores. Further work could go into improving the evaluation workflow by systematically comparing scores between an image and its blurred
versions, and by testing on known datasets to compare new methods with existing literature.
