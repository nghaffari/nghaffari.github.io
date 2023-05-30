---
layout: page
title: Product Defect Classification
description: Categorizing product defect patterns using the Chinese restaurant process and the Indian buffet process
img: assets/img/7.jpg
importance: 1
category: work
---

This overview covers a research project I completed for a major semiconductor manufacturer. The company has since merged with another major manufacturer. At the time, the firm had multibillion dollar semiconductor sales and specialized in integrated circuits. Integrated circuits are silicon wafers with embedded transistors and other electronic components. This is in contrast to discrete circuits where separate electronic components are connected together. While discrete circuits allow for more customization, integrated circuits enjoy several advantages: mass-production, cost-efficacy, lower power consumption. 

# Business Context

The motto of the real estate industry is "location, location, location," emphasizing how important location is to present and future property values. In the semiconductor industry the saying is, "faster, smaller, cheaper." Gordon Moore was an engineer and entrepeneur who founded his own semiconductor company.  In 1975 he observed that the transistor count on integrated circuits was doubling roughly every two years. He projected this trend to continue for the next decade, and indeed it has persisted until very recently; so this phenomenon has been named Moore's law. This process of doubling the transistor count on integrated circuits has largely been driven by miniaturization of components. As of recently this process is approaching its limits, and there has been increasing emphasis on 3D stacking of transistors to continue processing power gains. 

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/MooreDouble.png" title="Moore's law: doubling transistor counts 1970-2020" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/MooresMini.png" title="Moore's law: component miniaturization 1970-2017" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Moore's law visualized through the doubling of transistor (left) and the component miniaturization (right).
</div>

Some leading technologists have claimed Moore's law is dead; others argue it is still a force. If you are curious to learn more about Moore's law and associated manufacturing trends in the semiconductor industry, check out the links below:

* (<a href="https://doi.org/10.1371/journal.pone.0256245">Schepen & Wang, 2021</a>)
* (<a href="https://blog.nisshinbo-microdevices.co.jp/en/process">Yoshida, 2022</a>)
* (<a href="https://www.marketwatch.com/story/moores-laws-dead-nvidia-ceo-jensen-says-in-justifying-gaming-card-price-hike-11663798618">Huang: Moore's law is dead 2022</a>)
* (<a href="https://arstechnica.com/gadgets/2022/09/the-intel-arc-a770-gpu-launches-october-12-for-329/">Gelsinger: Moore's law is not dead 2022</a>)

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/1.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/3.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Caption photos easily. On the left, a road goes through a tunnel. Middle, leaves artistically fall in a hipster photoshoot. Right, in another hipster photoshoot, a lumberjack grasps a handful of pine needles.
</div>
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
