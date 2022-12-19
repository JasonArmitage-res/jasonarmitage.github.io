---
layout: page
title: priority map
description: a priority map module for vision-and-language navigation #a project with a background image
img: assets/img/pri_nav.png
importance: 1
category: papers
---
{% raw %}
```
Paper: https://arxiv.org/abs/2207.11717
Code: https://github.com/JasonArmitage-res/PM-VLN
Data: https://zenodo.org/record/6891965#.YtwoS3ZBxD8
Citation: see end of page.
```
{% endraw %}

<a href="https://arxiv.org/abs/2207.11717">Our research</a> addresses transformer-based approaches in vision-and-language navigation (VLN). We propose improving current systems with a computational implementation of a mechanism
described in neurobiological studies called a priority map. 

As agents move through an urban environment, they are surrounded by signs, moving traffic, and other people. A priority map,
is a cortical loop that mediates over high-level goals and 
lower level cues on salient features to identify relevant information:

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/pri_nav_crop.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/timeline_resize.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Prioritisation of cues updates as an agent navigates through an environment towards its end-goal. 
</div>

Our priority map module consists of two submodules. The first takes a new type of input called a path trace and forms a topdown trajectory plan. In the second step, a series of operations on visual and linguistic inputs localises corresponding information on prominent features. 

The overall result is that the cross-modal inputs are both synchronised to each other and to the current point in the trajectory.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/priority_map_website.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    A priority map module combines high-level trajectory estimation and low-level feature localisation.
</div>

The priority map module is a component in a novel framework that takes the input of a transformer-based main model and combines this with the output of the prioritisation process:

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/flpm.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Our feature-location framework combines outputs from a transformer and the priority map.
</div>

On the Touchdown task for VLN, our best performing variant more than doubles the Task Completion rate of the previous benchmark system based on transformers (<a href="https://aclanthology.org/2021.eacl-main.103/">Zhu et al., (2021)</a>).

A comparison of the purple and grey bars also demonstrates how our framework adds major gains to the performance of both general vision-and-language models and purpose-built architectures for VLN. 

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/touch_results.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Performance of transformer-based systems on the Touchdown task for VLN.
</div>

Please use <a href="https://github.com/JasonArmitage-res/PM-VLN">our code</a> and add a citation if you find it interesting:

Armitage, Jason, Leonardo Impett, and Rico Sennrich. "A Priority Map for Vision-and-Language Navigation with Trajectory Plans and Feature-Location Cues." arXiv preprint arXiv:2207.11717 (2022).
Link: <a href="https://arxiv.org/abs/2207.11717">https://arxiv.org/abs/2207.11717</a>

BibTeX:
{% raw %}
```
@article{armitage2022priority,
  title={A Priority Map for Vision-and-Language Navigation with Trajectory Plans and Feature-Location Cues},
  author={Armitage, Jason and Impett, Leonardo and Sennrich, Rico},
  journal={arXiv preprint arXiv:2207.11717},
  year={2022}
}
```
{% endraw %}
