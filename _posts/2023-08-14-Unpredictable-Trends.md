---
layout: distill
title: "Unpredictable Trends"
description: A survey of current chaotic trends and a discussion on managing unpredictability
tags: AI/ML business
giscus_comments: false
date: 2023-08-14

authors:
  - name: Novin Ghaffari
    url: "https://nghaffari.github.io/"

bibliography: 2023-Trends.bib

toc:
  - name: Chaotic Signals
  - name: Perplexing Labor Market Trends
  - name: Unpredictable NOT Unmanageable
---

## Chaotic Signals

"Hindsight is 20/20," as the adage goes. Foresight is almost blind. Often little can be said about the future with confidence. Predictive analytics is an attempt to bridge this gap in future understanding. Through learning patterns from past data and building models of outcomes, trends are projected forward to future time points, and a best guess for the state of the future is constructed. 

The simplest models build future predictions directly from past data. This can be highly effective when patterns of variation are consistent. When patterns change, however, these models must be updated to reflect the altered process. When patterns are volatile and constantly in flux, simple smoothing and forecasting models are unlikely to be useful. In these sorts of environments, more complex models that incorporate other variables may perform better. These new variables, covariates, should explain some or all of the volatility observed in the outcomes. These variables "co-vary" with the outcomes of interest, hence they are useful in predicting future outcome values. Effective covariates combined with past data give more accurate future predictions.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/trendline.jpg" title="trends image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

There are a few considerations when dealing with chaotic trends that this article highlights:

1. **complex etiologies**: volatile patterns typically exhibit complex causes. Disentangling a phenomenon's complicated origins enables better prediction of its future patterns. 
2. **measurement uncertainty**: data and trends are often treated as certain fact. In reality most data is collected and curated by humans and human systems. This creates a real possibility for measurement errors as well as discrepancies arising from measurement methodologies.
3. **external covariates**: this fundamental process in scientific reasoning is crucial for taming seemingly unpredictable trends: associating some variables to the outcome of others. With robust patterns of association between variables we can use information on accessible variables to predict outcomes in (potentially inaccessible) variables.

These days a plethora of unexpected, volatile patterns can be observed in everything from climate data, to real estate valuations, to financial markets. The next section looks at a few of the current wild trends, specifically relating to US labor markets. The three considerations listed above are highlighted as trends are discussed. The subsequent section turns to a discussion about quantitative analysis and general overview of some methods for handling such extreme data for purposes of prediction.

## Perplexing Labor Market Trends

Many current trends show drastic departures from past behaviors. Below several abnormal trends and patterns relating the labor markets are reviewed and discussed. These abnormalities in turn can drive other irregularities in economic data. Abnormal trends, particularly toward extreme patterns, are typical in systems with reinforcement loops. That is, feedback from prior outcomes or actions drives continued intensification of trends (e.g., in anticipation of an angry response, an individual becomes defensive, inducing an angrier response from the other party, leading to more defensiveness). After a while, excessive positive reinforcement loops can trigger negative reinforcement loops (e.g., a global pandemic kills the most vulnerable, increasing death rates; but with reduced vulnerable populations, death rates post pandemic may decrease).

The labor data from the United States appears to show a mass disabling event occurring from 2020 through 2023. This data is collected by the US Bureau of Labor Statistics and aggregated and published by the Federal Reserve of St. Louis' economic data research unit (FRED)<d-cite key="FRED2023"></d-cite>.

From July 2010 to July 2020, the total disabled population increased from about 26 million to 29 million. That is an increase of about 11.5% over 10 years, or an annual increase of about 1.1%. From July 2020 to July 2023, the disabled population increased from 29 million to about 34 million. That translates to an increase of 17.2% over 3 years, or an annual growth of 5.4%.

<div class="embed-container">
  <iframe src="https://fred.stlouisfed.org/graph/graph-landing.php?g=17QX9&width=670&height=475" scrolling="no" frameborder="0" style="overflow:hidden;" allowTransparency="true" loading="lazy"></iframe>
</div>
<div class="caption">
    Reprinted from the St. Louis FED's FRED web page found in <d-cite key="FRED2023"></d-cite>.
</div>
<script src="https://fred.stlouisfed.org/graph/js/embed.js" type="text/javascript"></script>

The causes of this sudden rise in the disabled population are contested. Some theories tie the increased disabling to long covid. While some studies have shown most long covid symptoms abate within a year, others contend that certain effects, such as chronic fatigue, may persist<d-cite key="bonuck2023"></d-cite>. Others think environmental toxins, the legacy of pandemic era policies (e.g. reduced general medical visits), climate change, and host of other factors many driving the increased disabling. Still others think changes in reporting standards may be contributing. In all likelihood, there is a convergence of different factors driving an increase of this magnitude.

Another troubling labor trend is the recent plummeting of labor productivity. The year 2022 saw severe drops in labor productivity, as measured by the Bureau of Labor Statistics. Declines were the fastest observed since 1947. Similar declines have been observed in other parts of the world, such as Europe. These declines are all the more perplexing in the context that worker productivity rose by record levels during the start of the pandemic in 2020 and maintained modest growth in 2021 (Q1 4.3%, Q3 2.3%). Proponents and opponents of remote work variously attribute the work from home trend to the productivity surge in 2020-21 and the productivity decline in 2022. There are many other possible explanations. Some attribute the initial rise of labor productivity to pandemic era layoffs removing the most unproductive employees and raising productivity averages. Others attribute the 2022 decline in productivity to the 'great resignation,' the mass quitting of many workers after the pandemic period, which creates a costly need for hiring and training. Mentions of 'burnout' and 'overworking' have increased, which some point to as another possible cause for the productivity declines. Still others question the measurement methodology and wonder whether some degree of measurment error may be driving the observed volatility <d-cite key="telford2022"></d-cite>.

Labor productivity declines continued in Q1 of 2023 with 1.2% decline <d-cite key="BLS2023"></d-cite>. In a positive reversal of this trend, early data indicates Q2 of 2023 saw a sharp rebound in the labor productivity rate with a 3.7% increase<d-cite key="mutikani2023"></d-cite>.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/labor-productivity-outpu.png" title="labor productivity" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Reprinted from the US Bureau of Labor Statistics' recent nonfarm labor productivity data here in <d-cite key="BLS2023"></d-cite>.
</div>

Mental health trends can be indicative of the overall health of a society and directly impact labor productivity. Current US mental health trends present a bleak picture. One study aggregated data from the National Health Interview Survey from 1997 to 2016 to assess ADHD diagnoses in the US. The study found an increase in diagnoses from 6.1% in 1997-1998 to 10.2% in 2015-2016<d-cite key="xuetal2018"></d-cite>. Recent Gallup polling indicates that the rates of those ever having a depression diagnosis (29%) and those with a current depression diagnonsis (17.8%) both hit all-time highs<d-cite key="witters2023"></d-cite>. An astounding 18% of Americans 18-54 will suffer from an anxiety-related disorder in a given year<d-cite key="hopkins2023"></d-cite>. Causation has been variously attributed to overdiagnosis, overmedication, pandemic era social effects, poor diet, environmental pollution, and an increasingly materialistic perspective in society. There are strong arguments for many of these individual causes, and the macro patterns are likely the result of a combination of various causes coinciding.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/g_depress.png" title="labor productivity" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Reprinted from recent Gallup polling depicted in the article by Dan Witters here in <d-cite key="witters2023"></d-cite>.
</div>

## Unpredictable NOT Unmanageable

Volatile patterns make prediction difficult. This does not mean nothing can be done. It simply requires a more sophisticated organizational structure and expanded data sources. Here several tools and tactics for dealing with volatile and shifting data patterns are mentioned. The discussion is high level and general; to learn more do some reading on each of these topics.

To deal with shifting patterns in data, we must identify shifting patterns in data. This is the idea of *change point detection*. It is closely related to outlier or anomaly detection. Both methods seek to detect large deviations from an established pattern. Outlier detection seeks to identify individual points that deviate beyond some threshold, whereas change point detection seeks to identify a wholesale shift in the underlying pattern. Hence change point detection is looking for a sustained departure from normal.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/mean_shift.png" title="mean change point" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/var_shift.png" title="variance change point" class="img-fluid rounded z-depth-1" %}
    </div>
  <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/trend_shift.png" title="trend change point" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Three toy examples of simple change point detection scenarios: mean shift, variance shift, and trend line shift.
</div>

Volatility present in data may be partially explained by variables in other data sets. Then these variables may be used as *covariate predictors* to enhance accuracy in predictions of the original outcome. There are many models that can accommodate covariate variables to improve predictions. Common AR, ARMA, and ARIMA models have vectorized versions that incorporate several variables. Panel regression models from econometrics provide a statistical framework for modeling trends in panel-formatted data. Bayesian dynamic forecasting models provide a convenient methodology for continual model updating. Modern machine learning frameworks like neural networks and decision trees have also been applied to complex prediction problems.

Faced with volatile conditions and changing patterns, *sensitivity analysis* provides a means for assessing the impacts. Sensitivity analysis is fundamentally about analyzing how changes in certain input variables affect the values of output variables. Different ranges of inputs are used and different operating scenarios are built to wargame possible outcomes. This gives the enterprise some idea of how sensitive outcomes are to different magnitudes of fluctations in inputs. An example of a computational approach to sensitivity analysis is using simulation (e.g., simulating calls to a call center, simulating arrivals and departures at a hospital, etc.) to model different scenarios. 

Simulation outputs are analyzed via statistics. Statistical methods are used to reveal patterns of variation in the data and quantify uncertainty. One subdomain of statistics that may be useful when dealing with volatile data is *extreme value theory*, a branch of statistics that analyzes how the most extreme observations in a data set behave. Instead of using variance-based methods typically used when dealing with normally distributed data, a common extreme value approach is to examine peaks over a threshold. The distribution of these extreme values tends to follow an extreme value distribution. This can be used to analyze extreme deviations in a data set and make predictions about the magnitude and quantity of extreme deviations in the future. Such extreme value approaches are common used in risk modeling.

In short, there are an array of different techniques and frameworks for analyzing changing patterns in volatile data. Leveraging sophisticated approaches and covariate data can help overcome data complexities. Any successful application will be rooted in familiarity with the core data sets and an understanding of the underlying trends.


