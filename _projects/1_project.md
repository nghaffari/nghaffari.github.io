---
layout: page
title: Warranty Cost Analysis 
description: Statistical analysis and predictive modeling of warranty claims for a major global automotive parts manufacturer
img: assets/img/12.jpg
importance: 3
category: work
---

This writeup covers a project for a major, global commercial vehicle manufacturer analyzing parts failures and warranty claims. The firm wanted to analyze its warranty claim data to identify current failure patterns, predict future failure patterns, and support corrective business policies. The project involved substantial elements of data collection, data cleaning and preparation, exploratory data analysis, data visualization, and predictive modeling. The end results included: (1) clarity on the sources and nature of data that the firm had available as well as an understanding of what further data are necessary for future business analytics development (2) versatile data visualization tools, including an interactive dashboard, for understanding warranty claim patterns and (3) predictive modeling frameworks for understanding and forecasting key metrics such as raw batch failure rates and cumulative failure percentages.

Here the aim is to distill major takeaways from two important steps in this project: data collection/preparation and predictive modeling of cumulative failures.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/car_line.png" title="car assembly line" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

# Data Collection & Preparation

In many data science projects, data collection and preparation are the most time-consuming steps. This project was no exception. Among the challenges encountered during this phase:

* **data fragmentation**: different parts of the data were housed in different company divisions and/or clients
* **data formatting inconsistency**: inconsistent formatting of data fields in data from different sources
* **data value inconsistency**: data values in some data sets were inconsistent with purported values in other data sets
* **data incongruency**: certain aspects of the data were incongruent with stated business practices (e.g. service times far in excess of warranty period time), raising questions of error or exceptions
* **missing data**: some data values were missing in a given data set; some values were present in one data but absent from another (where they should also appear)
* **unstandardized data**: some data fields were not standardized, resulting in multiple spellings/representations of the same values

While these issues can be worked through and resolved, this typically uses a fair amount of work. The process requires a constant back and forth between the business leaders who understand their particular domain and data and the analysts and data scientists working the data. Some foresight, planning, and data engineering can make the data collection and preparation steps far less time-consuming. Among suggestions were:

1. **standardizsation**: standardization of data (standard values, spellings, etc.), standardization of data storage formatting
2. **automation**: automated data entry to reduce errors, misspellings, missing values
3. **integrated information systems**: integrating information systems across different departments and even with clients to unify data sources

Proper implementation of these principles during data entry and storage greatly improves the ease and efficiency of data collection and the reduces the steps and resources necessary for data prep. A fourth suggestion is a critical principle that is key to the success of any analytics project:

4. **problem definition**: define the problem at hand in clear and direct terms

Good problem definition makes it clear what data is needed and what modeling frameworks might be worth exploring. Data projects are only valuable insofar as they are in line with an organizations objectives.

Although many suggestions for improvements to future data collection projects were made, the firm was already aware of some of these shortcomings. They had already implemented more automated data collection and more stringent standardization while actively working toward more data integration within the firm and with clients. 
