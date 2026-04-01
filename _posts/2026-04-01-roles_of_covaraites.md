---
layout: post
title: "Roles of covariates in mediation models"
date: 2026-04-01
tags: [Simulation, Causal inference, Study design]
---
After finding that many organizational behavior/industrial psychology studies are underpowered, I moved on to another issue: impact of covairate on medaition model. 

These are additional variables—such as age, gender, racial group, or tenure—that are included to control for potential confounds and reduce unexplained variance. The conventional assumption is straightforward: adding covariates should improve statistical precision and, in turn, increase statistical power.

Evidence from the literature. 
Here are some examples fromo the literture
Becker, 2005; p.274 (control varaibles are factors that researchers include... or to reduce error terms and increase statistical power [e.g., Schwab, 1999])
Bernerth & Aguinis, 2016; p. 231 (For example, the inclusion of control variables...not only reduces avaiable degrees of freedom and statistical power...)
Mändli & Rönkkö, 2023; p.114 (Control variables are critically important for making causal claims in non-experimental management research and can be useful for increasing the precision and statistical power of experimental studies (Deaton & Cartwright, 2018; Hernández et al., 2004)

Some research articles suggest that it could increase the power, some suggested the opposite. To me, I had a hard time to imply the literature in my work, and I had no time to "argue" with others whether our theories suggest it or not.

Instead, we can use Monte Carlo Simulation, _some magic mathatics_



Covariates only improve power when they are meaningfully related to the variables in the model. When covariates are weakly related—or included by default rather than by design—they can actually reduce statistical power, making it harder to detect real effects. In other words, including covariates is not always a “safe” choice.

More importantly, the role of covariates depends on the research design.

In survey studies, where predictors are typically continuous and not randomized, covariates that are correlated with predictors can meaningfully affect statistical power. In contrast, in experimental designs with randomized (often dichotomous) treatments, the treatment is independent of other variables. In these settings, the covariate’s relationship with the mediator becomes more consequential.

In my work, I use Monte Carlo simulations to systematically examine how covariates affect statistical power in mediation models. The simulations vary the relationship between covariates and key variables across different contexts, including simple mediation, serial mediation, and moderated mediation. I also compare continuous covariates (e.g., age, income) and binary covariates (e.g., gender), as their measurement properties can lead to different outcomes.

The results challenge a common assumption in applied research: covariates do not universally improve statistical power. In some cases, their inclusion has little effect; in others, it can meaningfully reduce power.

Overall, these findings suggest that covariates should be treated as a design decision rather than a default choice. Researchers should consider when and how covariates contribute to inference—and incorporate them explicitly into power analysis—rather than assuming they will always improve model performance.



Becker, T. E. (2005). Potential Problems in the Statistical Control of Variables in Organizational Research: A Qualitative Analysis With Recommendations. Organizational Research Methods, 8(3), 274–289. https://doi.org/10.1177/1094428105278021
Bernerth, J. B., & Aguinis, H. (2016). A Critical Review and Best-Practice Recommendations for Control Variable Usage. Personnel Psychology, 69(1), 229–283. https://doi.org/10.1111/peps.12103
Mändli, F., & Rönkkö, M. (2025). To omit or to include? Integrating the frugal and prolific perspectives on control variable use. Organizational Research Methods, 28(1), 114-137.
