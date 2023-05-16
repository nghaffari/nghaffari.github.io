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

To read a bit more about probability vs quantile averaging, see the following paper (<a href="https://doi.org/10.1002/2014WR016163">Schepen & Wang, 2015).

# From Probability Distances to Probability Averaging

Closely related to the idea of averaging is the idea of distance. An average cannot be taken without some notion of distance. 

The Fisher-Rao and the Wasserstein metrics are two statistical distances between probability distributions closely related to the idea of probability and quantile averaging. The Wasserstein metric may be used to obtain barycenters; in 1D this equivalent to quantile averaging, and it generalizes the idea of quantile averaging to higher dimensions, as quantiles do not exist beyond 1D. Probability averaging minimizes the Kullback-Liebler divergence, a quantity closely related to the definition of the Fisher-Rao distance, which may also be used to construct barycenters. To see a somewhat technical comparison of Wasserstein and Fisher-Rao distances in constructing barycenters of multivariate normal distributions in the space of radar signal processing, seee the following (<a href="https://ieeexplore.ieee.org/abstract/document/6042179">Barbaresco 2011</a>).

The mathematics behind these ideas is bit advanced. However, a recent paper (<a href="https://doi.org/10.1109/SSP.2016.7551770">Marti et al 2016</a>) compared and contrasted the uses of each distance in a multidimensional setting where distributions exhibit dependencies. In this setting, the authors found that Wasserstein distance-based methods preserve geometric information in a more consistent manner than Fisher-Rao and other Kullback-Liebler-based methods. There are deep mathematical reasons for this; however the following example from their paper serves a succinct, intuitive example. Consider the following three 2D normal distributions. Each is a standard bivariate normal but with correlations of .5, .99. and .9999 respectively.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/Gauss5.jpg" title="Gaussian, 50% correlation" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/Gauss99.jpg" title="Gaussian, 99% correlation" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/Gauss9999.jpg" title="Gaussian, 99.99% correlation" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Bivariate Gaussian distributions with correlations of 50% (left), 99% (middle), and 99.99% (right).
</div>

Intuitively, by looking at these images, we can readily see that 99% and 99.99% correlation distributions should probably be closer distance-wise than 50% and 99%. Nonetheless, the authors find that Fisher-Rao and several other Kullback-Leibler-based distances all rank 99% correlation as closer to 50% than to 99.99%. Only the Wasserstein distance respects our intuition that 99% and 99.99% correlation bivariate Gaussians should be closer. This captured in the following table from their paper (Table 1, pg 4)

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/WassFItable.jpg" title="Table 1 on pg 4 from Marti et al 2016" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The table of distances between bivariate Gaussians A (50%), B (99%), and C (99.99%), showing only the Wassertein distance preserves D(A,B)>D(B,C) among metrics listed, for more see (<a href="https://doi.org/10.1109/SSP.2016.7551770">Marti et al 2016</a>) 
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
