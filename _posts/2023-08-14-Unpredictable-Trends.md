---
layout: distill
title: "Unpredictable Trends"
description: A survey of current chaotic trends and a discussion on managing unpredictability
tags: AI/ML, business
giscus_comments: false
date: 2023-08-14

authors:
  - name: Novin Ghaffari
    url: "https://nghaffari.github.io/"

bibliography: 2023-Trends.bib

toc:
  - name: Chaotic Signals
  - name: The World's Gone Mad
  - name: Unpredictable NOT Unmanageable
---

## Chaotic Signals

"Hindsight is 20/20," as the adage goes. Foresight is almost blind. Often little can be said about the future with confidence. Predictive analytics attempts to mitigate this gap in understanding the future. By learning patterns of association from past data and building quantitative models of outcomes, a best guess for the state of the future can be constructed. Trends are projected forward to future time points. The simplest models build future predictions directly from past data. This can be highly effective when patterns of variation are consistent. When patterns change, however, these models must be updated to reflect the changed process. When patterns are volatile and constantly in flux, simple smoothing and forecasting models are unlikely to be useful. In these sorts of environments, more complex models that incorporate other variables may perform better. These new variables, covariates, should explain some or all of the volatility observed in the outcome variable. These variables "co-vary" with the outcome of interest hence are useful in predicting future values of the outcome. Effective covariates combined with past data give more accurate future predictions.



There are a few considerations when dealing with chaotic trends that this article highlights:

1. **complex etiologies**: volatile patterns typically exhibit complex causes. Disentangling a phenomenon's complicated origins enables better prediction of its future patterns. 
2. **measurement uncertainty**: data and trends are often treated as certain fact. In reality most data is collected and curated by humans and human systems. This creates a real possibility for measurement errors as well as discrepancies arising from measurement methodologies.
3. **external covariates**: the fundamental process behind scientific reasoning is crucial for taming seemingly unpredictable trends: associating some variables to the outcome of others. With robust patterns of association between variables we can use information on accessible variables to predict outcomes in (potentially inaccessible) variables.

## The World's Gone Mad

The labor data from the United States appears to show a mass disabling event occurring from 2020 through 2023. This data is collected by the US Bureau of Labor Statistics and aggregated and published by the Federal Reserve of St. Louis' economic data research unit (FRED)<d-cite key="FRED2023"></d-cite>.

From July 2010 to July 2020, the total disabled population increased from about 26 million to 29 million. That is an increase of about 11.5% over 10 years, or an annual increase of about 1.1%. From July 2020 to July 2023, the disabled population increased from 29 million to about 34 million. That translates to an increase of 17.2% over 3 years, or an annual growth of 5.4%.

<div class="embed-container">
  <iframe src="https://fred.stlouisfed.org/graph/graph-landing.php?g=17QX9&width=670&height=475" scrolling="no" frameborder="0" style="overflow:hidden;" allowTransparency="true" loading="lazy"></iframe>
</div>

<script src="https://fred.stlouisfed.org/graph/js/embed.js" type="text/javascript"></script>

The causes of this sudden rise in the disabled population are contested. Some theories tie the increased disabling to long covid. While some studies have shown most long covid symptoms abate within a year, others contend that certain effects, such as chronic fatigue, may persist<d-cite key="bonuck2023"></d-cite>. Others think environmental toxins, the legacy of pandemic era policies (e.g. reduced general medical visits), climate change, and host of other factors many driving the increased disabling. Still others think changes in reporting standards may be contributing. In all likelihood, there is a convergence of different factors driving an increase of this magnitude.

## Unpredictable NOT Unmanageable
