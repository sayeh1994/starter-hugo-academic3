---
title: How far can generated data impact Neural Networks?
summary: Improving the performance of Deep Learning models using generated data.
tags:
  - Deep Learning
date: '2022-05-11T00:00:00Z'

# Optional external URL for project (replaces project detail page).
external_link: ''

image:
  caption: Photo by einfochips
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
The success of Deep Learning (DL) models depends on the size and quality of a given task dataset and its labels. In our work, we address the problem of generating data to build a DL-based Facial Expression Recognition (FER) model. Therefore, our task naturally requires first and foremost a large dataset with various Facial Expressions (FEs) and facial deformations to ensure the generation of a robust FER model. However, the generation of these facial expressions and deformations requires a careful experimental design with the intervention of at least one psychological expert to ensure the validity of the generated features and the labelling process. Clearly, data generation is a difficult task that is time consuming, expensive, and prone to human error. To partially compensate for data needs, many studies rely on standard data augmentation to increase generalizability. Standard data augmentation is routinely performed, but for some applications such as FER, it is more desirable to generate some deformations at the facial feature level rather than at the whole image level. Therefore, a novel data augmentation method that generates faces with different facial expression features could be beneficial. Generative Adversarial Networks (GANs) provide an alternative method for generating facial expressions, but the contribution of the generated facial expression features needs further validation. In this work, we explore the research question ``How far can generated data impact neural networks?"

Delving into the study, GANs has been used to generate various facial expressions, and we design different experimental settings to investigate their contribution to the improvement of FER as a DL-based model. 
We develop a state-of-the-art Convolution Neural Network (CNN) and first train it with real FEs datasets on 6 basic Ekman emotions (anger, disgust, fear, happiness, sadness, and surprise). And then we re-train the model from scratch using only GAN images.
To create a generated dataset, we use a version of GANs, which randomly generates realistic human faces. Due to the randomness of this model and the desirability of a balanced training set for the CNN classifier, we use the structure of another GAN model with different settings to artificially synthesize 6 basic emotions on a single generated image. Using a synthetic dataset, we re-train the CNN model again by augmenting the real datasets with the generated synthetic FEs so as not to suppress the influence of the real facial expressions during training due to their limited number.

The first CNN model trained with real FEs databases (RaFD and Oulu-CASIA) has a training accuracy of 78.77% and 12% less in tests, showing some overfitting effect. The training accuracy of the second model trained with only the synthetic data increased by 20%.
However, testing these two models with another real FEs dataset (MMI database) yields almost the same performance, showing that the model trained with only generated samples also exhibits overfitting.
Nonetheless, augmenting real FEs datasets with synthetic data allows us to increase the new model's accuracy by 9% when testing the MMI dataset. Thus, with the proposed process of data augmentation, we eliminate the overfitting and improve the generalization ability of the CNN model.
Finally, we are indeed not constrained by the generation of new faces. But there is a point beyond which adding new artificial faces no longer improves the results. We have observed experimentally that there is an optimal peak ratio between the number of real faces and the number of generated faces at which model performance is the highest.

We confirm that enriching the dataset with GAN images can improve the performance of a facial expression recognition model as one of the DL-based applications.
However, using our generated synthetic images alone cannot improve the model and it relies heavily on the presence of real images.
Therefore, for further studies, we are looking for a new method to achieve the same or better result by depending less on real datasets and mainly using the diversity of generated images.
