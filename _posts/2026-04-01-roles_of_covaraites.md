---
layout: post
title: "Roles of covariates in mediation models"
date: 2026-04-01
tags: [Simulation, Causal inference, Study design]
---

After finding that many organizational behavior and industrial psychology studies are underpowered ([link](https://jenson-lau.github.io/2026/04/01/underpowered-mediation.html)), I turned to a related question: what is the impact of covariates in mediation models?

Covariates are additional variables—such as age, gender, race, or tenure—that are included to control for potential confounds and reduce unexplained variance. The conventional assumption is straightforward: adding covariates should improve statistical precision and, in turn, increase statistical power.

### Evidence from the literature

The literature presents mixed views on this issue.

For example:

- Becker (2005, p. 274) suggests that control variables can reduce error variance and increase statistical power.  
- Bernerth and Aguinis (2016, p. 231) note that including control variables can also reduce available degrees of freedom and statistical power.  
- Mändli and Rönkkö (2023, p. 114) argue that control variables can improve precision in some settings, particularly in experimental research.

Some papers suggest that covariates increase power, while others suggest the opposite. However, when tracing these claims, it is often unclear whether they are supported by systematic evidence (e.g., Monte Carlo simulations under clearly defined conditions). Instead, many conclusions are generalized across models and contexts.

This generalization is common in organizational research, but it is less appropriate from a statistical perspective. The impact of covariates depends on underlying assumptions—such as effect size, distributional properties, and measurement scale—and therefore cannot be assumed to be universal.

As someone working on mediation models, I found it difficult to directly apply this literature. Much of the methodological guidance is based on non-mediation models, even though mediation is a central focus in organizational research.

### What I examine

In my dissertation, I focus on two key dimensions:

1. The impact of covariates across research designs (survey vs. experimental/RCT)  
2. The role of variable type (continuous vs. binary)

### Key insight

Covariates only improve power when they are meaningfully related to the variables in the model. When covariates are weakly related—or included by default rather than by design—they can actually reduce statistical power, making it harder to detect real effects.

In other words, including covariates is not always a “safe” choice.

More importantly, the role of covariates depends on the research design.

- In survey studies, where predictors are typically continuous and not randomized, covariates correlated with predictors can meaningfully affect statistical power.  
- In experimental designs with randomized (often dichotomous) treatments, the treatment is independent of other variables. In these cases, the covariate’s relationship with the mediator becomes more consequential.

### Approach

In my work, I use Monte Carlo simulations to systematically examine how covariates affect statistical power in mediation models. The simulations vary the relationship between covariates and key variables across different contexts, including simple mediation, serial mediation, and moderated mediation.

I also compare continuous covariates (e.g., age, income) and binary covariates (e.g., gender), as their measurement properties can lead to different outcomes.

### Takeaway

The results challenge a common assumption in applied research: covariates do not universally improve statistical power. In some cases, their inclusion has little effect; in others, it can meaningfully reduce power.

Overall, these findings suggest that covariates should be treated as a design decision rather than a default choice. Researchers should consider when and how covariates contribute to inference—and incorporate them explicitly into power analysis—rather than assuming they will always improve model performance.

---

### References

Becker, T. E. (2005). Potential problems in the statistical control of variables in organizational research. *Organizational Research Methods, 8*(3), 274–289.  

Bernerth, J. B., & Aguinis, H. (2016). A critical review and best-practice recommendations for control variable usage. *Personnel Psychology, 69*(1), 229–283.  

Mändli, F., & Rönkkö, M. (2025). To omit or to include? Integrating the frugal and prolific perspectives on control variable use. *Organizational Research Methods, 28*(1), 114–137.
