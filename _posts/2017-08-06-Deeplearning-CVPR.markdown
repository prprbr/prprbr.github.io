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


