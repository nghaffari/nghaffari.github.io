---
layout: page
title: Consensus Modeling
description: Forming a consensus model from several inputs
img: assets/img/3.jpg
importance: 1
category: work
---

This writeup is based on a project I performed for a major national laboratory. I cannot get into the details, so instead, here I cover the methods and general scope of the project: combining input distributions from several experiments into a consensus model. This consensus model represents the combined understanding of all relevant experiments.

# Averaging Probability Distributions

To begin with we examine the difference between arithmetic or probability averaging and Wasserstein or quantile averaging. Probability distributions, just like numbers, vectors, matrices, and other quantitative objects, may be averaged together. However, distributions have more 'pieces' in their definition and construction than simple numbers and arrays, so averaging them is also more complicated.

Two primary methods for averaging probability distributions are probability averaging and quantile averaging. The images below depict each case. Our averaging inputs are two Gaussian distributions with equal variance but different means. These are visualized in light yellow in each graph. The red distribution is the average; the left image depicts the probability average and the right image the quantile average.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/AAGauss.jpg" title="arithmetic average of two Gaussians" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/WAGauss.jpg" title="Wasserstein average of two Gaussian" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    A probability (left) and quantile (right) average (red distribution) over two Gaussian distributions with different means (yellow bell curves).
</div>
We may prefer one or the other, depending on the application of interest. In a nutshell, probability averaging is useful when input probability distributions represent *different* portions of the same phenomenon, and quantile averaging makes the most sense when input probability distributions are modeling the *same* portion of the same phenomenon. In the image above, assume each Gaussian input is a distribution from a sensor measuring a feature, something like equipment temperature. The following two scenarios apply to probability and quantile averaging respectively.

**Scenario 1**: Imagine one sensor is a daytime temperature sensor and the other a nighttime sensor. Then here we prefer the probability average, as each sensor is measuring a separate part of the full distribution, i.e. the full day-night distribution is truly bimodal, and each sensor catches one mode.

**Scenario 2**: Imagine each sensor runs all day, and is on average unbiased, but there is some noise in the mean value of each distribution. In this case we prefer quantile averaging as each sensor is measuring the same phenomenon but has its own noise, i.e. the full distribution is truly unimodal.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    This image can also have a caption. It's like magic.
</div>

You can also put regular text between your rows of images.
Say you wanted to write a little bit about your project before you posted the rest of the images.
You describe how you toiled, sweated, *bled* for your project, and then... you reveal its glory in the next row of images.


<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.html path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    You can also have artistically styled 2/3 + 1/3 images, like these.
</div>


The code is simple.
Just wrap your images with `<div class="col-sm">` and place them inside `<div class="row">` (read more about the <a href="https://getbootstrap.com/docs/4.4/layout/grid/">Bootstrap Grid</a> system).
To make images responsive, add `img-fluid` class to each; for rounded corners and shadows use `rounded` and `z-depth-1` classes.
Here's the code for the last row of images above:

{% raw %}
```html
<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.html path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
```
{% endraw %}
