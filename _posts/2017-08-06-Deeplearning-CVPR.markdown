---
layout: post
comments: true
title:  "Deeplearning-CVPR"
date:   2017-08-06
---

About 5000 people with shared interest in computer vision and machine learning flocked to the beautiful shores of Honolulu to attend the CVPR 2017 conference. I was privileged to attend this week long discussion and demonstration on some of the cutting edge research in the field. In this blog post, I present some of the interesting highlights of the conference.

<img src="/assets/cvpr/honolulu.JPG" width="25%" height="25%" />

### Day 1

The main conference started its program on July 22. However, there were some really good workshops and tutorials on July 21 and 26. One could see a large number of talks from industry researchers in these workshops. Richard Newcombe from Facebook gave a nice presentation on real time AR and robotics being applied at Facebook/Oculus for applications like infoor mapping and localization.  Raquel Urtasun, head of Uber ATG Toronto, talked about their open source research on autonomous driving and showed videos of their labeling tools and usage of dummies in test tracks. I came across an interesting poster on using Generative Adversarial Networks (go to GAN to know more) to [find anomalies for a Patrolbot](http://juxi.net/workshop/deep-learning-robotic-vision-cvpr-2017/papers/18.pdf). It was really interesting to find the methods used by the competition winners at the [TuSimple Autonomous Driving Challenge](http://benchmark.tusimple.ai/#/).A team from [TU Graz](http://benchmark.tusimple.ai/static/files/poster_velocity_1.pdf) showed that in order to calculate the velocity of each moving vehicle on the road from just monocular camera image sequence, a plug and play approach using some of the pre-trained models for depth ([monodepth](https://github.com/mrharicot/monodepth)), flow ([Flow Net](https://arxiv.org/abs/1612.01925) ) and tracking estimations (MedianFlow) just works so good. Here is recreated version of their idea using a snapshot during their presentation.    
<img src="/assets/cvpr/vel_est.jpg"  />

### Day 2



