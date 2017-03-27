---
layout:     post
title:      Supervised Evaluation of Seed-Based Interactive Image Segmentation Algorithms
date:       2015-07-24 14:57:10
summary:    In this paper, we present an objective and empirical evaluation of seed-based interactive segmentation algorithms. We first compare popular metrics that are employed in image-segmentation evaluations in order to define which one reflects most accurately the performance of segmentation algorithms. Then, in the aim of presenting reproducible results, we introduce a novel seed-based user input dataset that extends the well-known GrabCut dataset. Finally, we evaluate and contrast four state-of-the-art interactive segmentation algorithms.
categories: research
tags:       [segmentation, english, research, evaluation, publication]
---

<img src="{{ site.url }}/assets/images/segmentation-01.jpg" width="49%" alt="Segmentation image"/> <img src="{{ site.url }}/assets/images/segmentation-08.jpg" width="49%" alt="Segmentation image"/>
<img src="{{ site.url }}/assets/images/segmentation-05.jpg" width="49%" alt="Segmentation image"/> <img src="{{ site.url }}/assets/images/segmentation-06.jpg" width="49%" alt="Segmentation image"/>

Extensive research has been conducted in an effort to evaluate methods and techniques for image segmentation. However, while most literature has focused on evaluating automatic and semi-automatic algorithms, works evaluating interactive segmentation algorithms are less numerous. Note that interactive segmentation can improve results by adding prior knowledge from users into the process. Although this user guidance improves segmentation results, it also makes difficult to conduct objective evaluations. For this reason, some works only present non-canonical evaluations.

In this paper, we present an objective and empirical evaluation of seed-based interactive segmentation algorithms. We first compare popular metrics that are employed in image-segmentation evaluations in order to define which one reflects most accurately the performance of segmentation algorithms. Then, in the aim of presenting reproducible results, we introduce a novel seed-based user input dataset that extends the well-known GrabCut dataset. In addition, we evaluate and contrast four state-of-the-art interactive segmentation algorithms. The analysis of the results demonstrates that Jaccard coefficient and Precision-Recall curves provide a good insight into the performance of the evaluated algorithms. Finally, the GrabCut algorithm presents the most robust and useful segmentation among all the evaluated algorithms.

## Dataset

[Dataset for Interactive Image Segmentation](https://github.com/flandrade/dataset-interactive-algorithms)

## Research Notes

* [The Problem of Evaluating Interactive Segmentation]({% post_url 2015-07-24-problem-evaluating-interactive-segmentation %})
* [Novel Dataset for Interactive Segmentation Evaluation]({% post_url 2015-07-25-interactive-segmentation-dataset %})

## Algorithm Implementations

Coming soon…

## Publication

* Andrade F., Carrera E. V., "Supervised evaluation of seed-based interactive image segmentation algorithms", In _Proceedings of the 20th Symposium on Image, Signal Processing, and Artificial Vision_, ISBN 978-1-4673-9461-1, Bogota, Colombia, pp. 225-231, September 2015. ([IEEE](http://ieeexplore.ieee.org/xpl/articleDetails.jsp?arnumber=7330447))
