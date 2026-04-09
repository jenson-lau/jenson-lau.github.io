---
layout: post
title: "When can we treat categorical data as continuous in SEM?"
date: 2026-04-09
tags: [SEM, Categorical, Continuous]
---

In a perfect world, everything would be measured as a continuous variable. Every dataset would be multivariate normal and would not violate any assumptions of our analytical methods. However, such “perfect” data likely only exist in introductory statistics textbooks. Let’s first clarify the difference between continuous and categorical variables.

We use numbers to measure observable quantities. For example, if we want to know the temperature in Seattle, we can check a thermometer (e.g., 61°F today). If we want to know our height, we can use a ruler (e.g., 176 cm). If we want to know our weight, we can step on a scale (e.g., 83 kg). These are quantities that we can observe and measure directly.

In psychology, organizational behavior, and industrial psychology, however, we often measure constructs that are not directly observable (e.g., leadership, creativity, mindfulness). For example, if we want to assess someone’s depression severity, we might use an instrument such as the PHQ-9.

<img src="/assets/PHQ-9.png" alt="PHQ-9 questionnaire" style="max-width:100%; margin:20px 0;">

As shown above, we cannot measure depression as a continuous quantity like “1.5 units” or “0.79 units.” Instead, responses are categorized into ordered groups (e.g., Not at all, Several days, More than half the days, Nearly every day). These are ordinal (categorical) variables.

In applied settings such as people analytics, researchers may be interested in questions like: How does employee loyalty influence organizational culture, customer perception, or evaluations of leadership? These variables are often measured using categorical (or sometimes binary) responses. When analyzing relationships among multiple variables simultaneously, structural equation modeling (SEM) is commonly used.

As noted earlier, real-world data are often messy (i.e., non-normal). However, researchers frequently apply SEM using either:

- Normal-theory maximum likelihood based on Pearson correlations (cont-ML), or  
- Least squares estimation based on polychoric correlations (cat-LS)

Both approaches are partially appropriate. The cont-ML approach treats variables as continuous and ignores their categorical nature. In contrast, cat-LS accounts for ordinal measurement but assumes an underlying multivariate normal distribution.

This leads to a key question: **When is it acceptable to treat categorical variables as continuous?**

The literature does not provide a simple, universal answer.

Based on Foldnes and Grønneberg (2022), simulation results suggest that when the data are not multivariate normal, adjusted continuous ML (cont-ML-adj) can outperform standard approaches, while categorical least squares (cat-LS) tends to produce less biased estimates under certain conditions. In practice, cat-LS may be preferred when the ordinal variables can reasonably be assumed to reflect an underlying normal distribution.

<img src="/assets/Number-categories-correlation.png" alt="Number of categories and correlation impact" style="max-width:100%; margin:20px 0;">

Overall, the decision is not binary. Treating categorical data as continuous depends on multiple factors, including the number of categories, distributional assumptions, and the underlying data-generating process.

---

**Reference**

Foldnes, N., & Grønneberg, S. (2022). The sensitivity of structural equation modeling with ordinal data to underlying non-normality and observed distributional forms. *Psychological Methods, 27*(4), 541–567. https://doi.org/10.1037/met0000385
