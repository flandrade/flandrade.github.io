---
layout:     post
title:      The Problem of Evaluating Interactive Segmentation
date:       2015-07-24 17:50:40
summary:    Despite some significant advances and extensive research, the selection of interactive segmentation algorithms is still a challenging task because people incorporate some semantic considerations that lead to more than one acceptable solution.
categories: research
tags:       [segmentation, english, research, evaluation]
---

Image segmentation is a fundamental task in computer vision in which images are divided into meaningful segments. However, despite some significant advances and extensive research in this field, the selection of segmentation algorithms is still a challenging task because people incorporate some semantic considerations in their evaluations that lead to more than one acceptable solution.

<img src="{{ site.url }}/assets/images/segmentation-01.jpg" width="96%" alt="Segmentation image"/>

<img src="{{ site.url }}/assets/images/segmentation-02.jpg" width="32%" alt="Segmentation image"/> <img src="{{ site.url }}/assets/images/segmentation-03.jpg" width="32%" alt="Segmentation image"/> <img src="{{ site.url }}/assets/images/segmentation-04.jpg" width="32%" alt="Segmentation image"/>

In fact, interactive image segmentation improves results by adding prior knowledge from users into the process. The main task of users is to extract semantic objects from a determined image. In general, users define the object and its background by drawing bounding boxes or seeds (also known as scribbles or brush strokes).

<img src="{{ site.url }}/assets/images/segmentation-05.jpg" width="49%" alt="Segmentation image"/> <img src="{{ site.url }}/assets/images/segmentation-07.jpg" width="49%" alt="Segmentation image"/>

Although this user guidance improves segmentation results, it also makes harder to evaluate this kind of algorithms and, for this reason, some works present subjective results or use non-canonical evaluations. For example, most interactive segmentation evaluations use their own seeds, which do not allow a fair comparison of performance among segmentation algorithms.[^1]

Some approaches have been proposed to tackle this problem, but they all present drawbacks as detailed below:

### Datasets

Even though the [Berkeley segmentation dataset](http://www.eecs.berkeley.edu/Research/Projects/CS/vision/grouping/resources.html) and benchmark are the extended evaluation criteria for automatic segmentation, it is not possible to identify objects and background from its ground-truth data as the dataset does not include a semantic interpretation.[^2] Instead, there are a couple of public datasets that facilitate comparison, but they do not provide user inputs required by the algorithms in order to get reproducible results:

* __Weizmann segmentation database:__ [it](http://www.wisdom.weizmann.ac.il/~vision/Seg_Evaluation_DB/index.html) provides a suitable single object dataset for evaluation of interactive segmentation algorithms, but it does not provide user inputs.[^3]

* __Grabcut database:__ [this dataset](http://research.microsoft.com/en-us/um/cambridge/projects/visionimagevideoediting/segmentation/grabcut.htm) contains 50 images, ground-truth data and user specified _trimaps_. However, these _trimaps_ are neither optimal nor realistic inputs because they contain richer information, such as shape, and most of the pixels are previously labeled. Moreover, it would be difficult for users to create such _trimaps_.[^4]

### User-experiments

In these experiments, users were shown images with descriptions of the objects they were required to extract.[^5] Then, users marked foreground and background pixels using a platform designed for this purpose. However, these evaluations are time-consuming because they require a constant involvement of users and do not enable repeatability of results.

### Automated evaluations

Automated evaluations replace users with algorithms that emulate their behavior.[^6] [^7] These robot users emulate user interactions by generating scribbles. While robot-user evaluations measure effort by the number of required iterations for an accurate segmentation, they place the sequence of seeds according the outcome of each interaction and, therefore, generated seeds vary for different algorithms. This leads to the inability of obtaining repeatable results.

## My proposed approach

In summary, these evaluation methods should have considered user intervention to allow reproduction and comparison of results for further studies. For this reason, I introduced a novel seed-based user input dataset that extends the well-known GrabCut dataset and the [Geodesic Star convexity dataset](http://www.robots.ox.ac.uk/~vgg/research/iseg/#Dataset). For more information, check the [second note]({% post_url 2015-07-25-interactive-segmentation-dataset %}).

__NOTE:__ _This note is the first of two notes. See the [presentation entry]({% post_url 2015-07-24-evaluation-interactive-image-segmentation %}) for more information._

---

[^1]: B. J.Wu,Y.Zhao,J.-Y.Zhu,S.Luo,andZ.Tu.Milcut:A sweeping line multiple instance learning paradigm for interactive image segmentation. In _Computer Vision and Pattern Recognition (CVPR), 2014 IEEE Conference on_, pages 256–263. IEEE, 2014.

[^2]: P. Arbelaez, M. Maire, C. Fowlkes, and J. Malik. Contour detection and hierarchical image segmentation. _Pattern Analysis and Machine Intelligence, IEEE Transactions on_, 33(5):898–916, 2011.

[^3]: S. Alpert, M. Galun, R. Basri, and A. Brandt. Image segmentation by probabilistic bottom-up aggregation and cue integration. In _Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition_, June 2007.

[^4]: C. Rother, V. Kolmogorov, and A. Blake. Grabcut: Interactive foreground extraction using iterated graph cuts. _ACM Transactions on Graphics (TOG)_, 23(3):309–314, 2004.

[^5]: K. McGuinness and N. E. O’Connor. A comparative evaluation of interactive segmentation algorithms. _Pattern Recognition_, 43(2):434–444, 2010.

[^6]: K. McGuinness and N. E. OConnor. Toward automated evaluation of interactive segmentation. _Computer Vision and Image Understanding_, 115(6):868– 884, 2011.

[^7]: V. Gulshan, C. Rother, A. Criminisi, A. Blake, and A. Zisserman. Geodesic star convexity for interactive image segmentation. _In Computer Vision and Pattern Recognition (CVPR), 2010 IEEE Conference on_, pages 3129–3136. IEEE, 2010.
