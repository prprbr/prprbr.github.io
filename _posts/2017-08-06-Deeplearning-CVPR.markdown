---
layout: post
comments: true
title:  "Deeplearning-CVPR"
date:   2017-08-06
---

About 5000 people with shared interest in computer vision and machine learning flocked to the beautiful shores of Honolulu to attend the CVPR 2017 conference. I was privileged to attend this week long discussion and demonstration on some of the cutting edge research in the field. In this blog post, I present some of the interesting highlights of the conference.

<img src="/assets/cvpr/honolulu.JPG" width="50%" height="50%" />

### Day 1 (Workshops and Tutorials)

The main conference started its program on July 22. However, there were some really good workshops and tutorials on July 21 and 26. One could see a large number of talks from industry researchers in these workshops. Richard Newcombe from Facebook gave a nice presentation on real time AR and robotics being applied at Facebook/Oculus for applications like infoor mapping and localization.  Raquel Urtasun, head of Uber ATG Toronto, talked about their open source research on autonomous driving and showed videos of their labeling tools and usage of dummies in test tracks. I came across an interesting poster on using Generative Adversarial Networks (go to GAN to know more) to [find anomalies for a Patrolbot](http://juxi.net/workshop/deep-learning-robotic-vision-cvpr-2017/papers/18.pdf). It was really interesting to find the methods used by the competition winners at the [TuSimple Autonomous Driving Challenge](http://benchmark.tusimple.ai/#/).A team from [TU Graz](http://benchmark.tusimple.ai/static/files/poster_velocity_1.pdf) showed that in order to calculate the velocity of each moving vehicle on the road from just monocular camera image sequence, a plug and play approach using some of the pre-trained models for depth ([monodepth](https://github.com/mrharicot/monodepth)), flow ([Flow Net](https://arxiv.org/abs/1612.01925) ) and tracking estimations (MedianFlow) just works so good. Here is recreated version of their idea using a snapshot during their presentation.    
<img src="/assets/cvpr/vel_est.jpg" width="75%" height="75%" />

### Day 2 - 5 (Main Conference)

A lot of prior research has gone into improving the image recognition using more than just the image RGB data. On similar lines, a CVPR paper from Ruslan Salakhutdinov's group used [knowledge graph for image classification](https://arxiv.org/pdf/1612.04844.pdf). Semantic knowledge was borrowed from The [Visual Genome](http://visualgenome.org/). 

Neural networks usually are memory consuming and too big to be implemented on low end embedded devices, for e.g. a mobile phone chipset. Thus, there is a need to compress these models without loss of performance. A paper on such [deep compression](http://openaccess.thecvf.com/content_cvpr_2017/papers/Yu_On_Compressing_Deep_CVPR_2017_paper.pdf) showed how an VGG 16 model trained on IMAGENET that contains about 138 million weights could be compressed to just 9.7 million without any difference in inference accuracy.

There were a lot of papers on domain adaptation (effort to transfer knowledge from one domain to another). Folks from Google presented [Unsupervised Pixel-Level Domain Adaptation with GANs](https://arxiv.org/pdf/1612.05424.pdf) where they showed how they translate images from MNIST grayscale images to color background and so on. It was interesting to note that there were several papers on the very same line, i.e. using GANs to convert an image from one style to another. In fact, Apple published its first ever research paper and it was attacking the very same problem. [That paper](https://arxiv.org/pdf/1612.07828.pdf) got them the best CVPR paper award too ;) .
<a href="https://machinelearning.apple.com/images/journals/gan/block_diag_gif.gif"><img src="https://machinelearning.apple.com/images/journals/gan/block_diag_gif.gif" title="source: Apple's machine learning journal" /></a>

GANs also found use in generating super resolution images, i.e. increasing or zooming the resolution of small images without degradation in semantic content. [Hallucinating low resolution images](http://openaccess.thecvf.com/content_cvpr_2017/papers/Yu_Hallucinating_Very_Low-Resolution_CVPR_2017_paper.pdf) is a technique that can super-resolve tiny 16x16 images upto a zoom up scale of 8x to look realistic. Similarly, [SrGAN](https://arxiv.org/pdf/1609.04802.pdf), developed by a team from Twitter, showed 4x zooms of images which were way better than just zooming using bicubic interpolation. 

If you might have noticed, most of the deep learning networks have an architecture that is fixed and only the weights change during training. However, the necessary structure to learn something is unknown and to address this, an [interpretable structure evolving LSTM](https://arxiv.org/pdf/1703.03055.pdf) was proposed in this conference where the graph architecture changes over training time.

Another best paper winner was that from Facebook AI research. The idea is as simple as it gets - connect each layer with every other layer. 
<a href="https://cloud.githubusercontent.com/assets/8370623/17981494/f838717a-6ad1-11e6-9391-f0906c80bc1d.jpg"><img src="https://cloud.githubusercontent.com/assets/8370623/17981494/f838717a-6ad1-11e6-9391-f0906c80bc1d.jpg" title="source: DenseNet by Facebook AI Research" width="50%" height="50%"  /></a>
Their paper on [Densely Connected Convolutional Networks](https://arxiv.org/pdf/1608.06993.pdf) showed how they could beat the performance of ResNet by a margin with such dense connections.

There was another interesting idea on improving fine graned image classification between images that looks very similar to each other. The idea was to recursively learns discriminative
region attention and region-based feature representation
in a mutually reinforced manner. In this perspective, the inputs to their model called [RA-CNN](http://openaccess.thecvf.com/content_cvpr_2017/papers/Fu_Look_Closer_to_CVPR_2017_paper.pdf) varies from coarse full scale image to finer zoomed in region attention. Btw, Micorosoft Research Flower app uses this technology. 
<img src="/assets/cvpr/racnn.jpg" width="90%" height="90%" />


### Day 6 (Final workshops and tutorials) 
